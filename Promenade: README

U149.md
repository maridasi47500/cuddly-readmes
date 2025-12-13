Promenade: README

Un micro-projet pour “se promener” IRL ou virtuellement, poster des
messages et photos du crépuscule à l’aube, avec ou sans GPS, et garder une
trace en base de données. Bash pour l’outillage, HTML pour un petit menu de
navigation, et une API simple pour publier/consulter.
Présentation

   -

   *Idée:* Une appli légère où tu peux te balader, publier des messages et
   photos “from dusk till dawn”, enrichir une base de connaissances des gens
   que tu connais, et enregistrer (optionnel) ta position GPS.
   -

   *Philosophie:* Tu n’as pas besoin de coordonnées GPS pour publier. La
   liberté d’errance d’abord; les métadonnées ensuite.
   -

   *Stack:* Bash (scripts), Node.js/Express  (API), SQLite (ou Postgres),
   HTML/CSS vanilla (menu minimal).

Fonctionnalités

   -

   *Promenade libre:* Poste des messages à toute heure, avec ou sans
   localisation.
   -

   *Crépuscule → Aube:* Fenêtre “nocturne” configurable pour tagger
   automatiquement tes posts.
   -

   *Photos et messages:* Upload d’images + légendes; stockage de timestamps.
   -

   *Carnet de connaissances:* Base “people” pour noter les personnes que tu
   connais et les lier à des lieux/rencontres.
   -

   *Navigation HTML:* Petit menu statique pour explorer tes posts,
   personnes, lieux.
   -

   *GPS optionnel:* Si fourni, on enregistre; sinon, on publie quand même.
   -

   *Export:* Dump de la base et export JSON des posts.

Installation et démarrage

   -

   *Prérequis:* Node.js  ≥ 18, Git, SQLite3 (ou Postgres), Bash.
   -

   *Clonage:*
   Code

   git clone https://github.com/ton-org/promenade.git
   cd promenade

   -

   *Configuration:* Crée un fichier .env:
   Code

   PORT=8080
   DB_URL=sqlite://./data/promenade.db
   NIGHT_START=18:30
   NIGHT_END=05:30
   UPLOAD_DIR=./uploads

   -

   *Initialisation DB:*
   Code

   bash scripts/db_init.sh

   -

   *Lancement:*
   Code

   npm install
   npm run dev
   # Ouvre http://localhost:8080


UtilisationAPI essentielle

   -

   *Créer un post:*
   Code

   curl -X POST http://localhost:8080/api/posts \
     -F "text=Balade sur le boulevard, lumière orangée." \
     -F "photo=@/chemin/photo.jpg" \
     -F "lat=5.158" \
     -F "lng=-52.643"

   -

      *Sans GPS:* omets lat/lng.
      -

   *Lister les posts:*
   Code

   curl http://localhost:8080/api/posts?from=2025-09-09&to=2025-09-10&night=true

   -

   *Ajouter une personne:*
   Code

   curl -X POST http://localhost:8080/api/people \
     -H "Content-Type: application/json" \
     -d '{"name":"Awa","notes":"Rencontrée à Kourou, café indépendant."}'

   -

   *Associer une rencontre:*
   Code

   curl -X POST http://localhost:8080/api/encounters \
     -H "Content-Type: application/json" \
     -d '{"personId":1,"postId":42,"context":"Discussion sur les
tortues luth."}'


Menu HTML minimal

Ajoute un lien dans le menu pour créer un nouveau post.
html

<nav class="menu">
  <a href="/">Flux</a>
  <a href="/people">Personnes</a>
  <a href="/map">Carte</a>
  <a href="/new">Nouveau post</a>
</nav>

Formulaire simple pour publier sans GPS obligatoire:
html

<form action="/api/posts" method="post" enctype="multipart/form-data">
  <label>Message</label>
  <textarea name="text" required></textarea>

  <label>Photo (optionnel)</label>
  <input type="file" name="photo" accept="image/*" />

  <details>
    <summary>Position (optionnel)</summary>
    <input name="lat" placeholder="Latitude" />
    <input name="lng" placeholder="Longitude" />
  </details>

  <button type="submit">Publier</button>
</form>

Scripts Bash utiles

   -

   *Backup DB:*
   bash

   #!/usr/bin/env bash
   set -euo pipefail
   ts="$(date +%Y%m%d-%H%M%S)"
   mkdir -p backups
   cp data/promenade.db "backups/promenade-$ts.db"
   echo "Backup -> backups/promenade-$ts.db"

   -

   *Export JSON:*
   bash

   #!/usr/bin/env bash
   node scripts/export_json.mjs > exports/posts.json


Structure des données

   -

   *Table posts:* id, text, photo_path, created_at (UTC), is_night, lat,
   lng, place_hint.
   -

   *Table people:* id, name, notes, created_at.
   -

   *Table encounters:* id, person_id, post_id, context.
   -

   *Vues suggérées:*
   -

      vue_night_posts: posts entre NIGHT_START et NIGHT_END.
      -

      vue_places: agrégats par place_hint ou grille géo (si GPS).

Exemple SQL minimal (SQLite):
sql

CREATE TABLE posts (
  id INTEGER PRIMARY KEY,
  text TEXT NOT NULL,
  photo_path TEXT,
  created_at TEXT NOT NULL DEFAULT (datetime('now')),
  is_night INTEGER NOT NULL DEFAULT 0,
  lat REAL, lng REAL,
  place_hint TEXT
);

CREATE TABLE people (
  id INTEGER PRIMARY KEY,
  name TEXT NOT NULL,
  notes TEXT,
  created_at TEXT NOT NULL DEFAULT (datetime('now'))
);

CREATE TABLE encounters (
  id INTEGER PRIMARY KEY,
  person_id INTEGER NOT NULL,
  post_id INTEGER NOT NULL,
  context TEXT,
  FOREIGN KEY (person_id) REFERENCES people(id),
  FOREIGN KEY (post_id) REFERENCES posts(id)
);

Personnalisation et roadmap

   -

   *Fenêtre nocturne:* Ajuste NIGHT_START/NIGHT_END dans .env. L’API
   taggera is_night.
   -

   *GPS facultatif:* Le backend ne rejette pas l’absence de lat/lng. Ajoute
   une “carte” qui fonctionne avec place_hint si pas de coordonnées.
   -

   *Exploration nature:* Ajoute un champ habitat (mangrove, plage, forêt)
   pour filtrer.
   -

   *Boulevards et magasins:* Ajoute poi_type (boulevard, boutique, marché)
   pour tes scènes urbaines.
   -

   *Vie privée:* Active le floutage EXIF et une option pour ne jamais
   stocker GPS par défaut.
   -

   *À venir:*
   -

      Upload direct depuis mobile (PWA).
      -

      Mosaïque photo “dusk→dawn”.
      -

      Import/Export people en CSV.
      -

      Étiquetage automatique “nuit” selon fuseau et position si disponible.
