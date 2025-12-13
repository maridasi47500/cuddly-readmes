🌇 Promenade Stack Voyageur

Un micro-projet interactif pour choisir ta propre stack (front-end,
back-end, base de données) et vivre une session “dusk till dawn” dans un
environnement urbain ou naturel. Chaque promenade devient une exploration
technique, sensible et sociale.
🧭 Présentation

   -

   *Idée* : Une appli légère pour se balader, publier des messages et
   photos “from dusk till dawn”, enrichir une base de connaissances des gens
   croisés, et enregistrer (optionnellement) ta position GPS.
   -

   *Philosophie* : La liberté d’errance d’abord ; les métadonnées ensuite.
   Tu peux publier sans GPS, sans identifiant, juste pour le plaisir de la
   trace.
   -

   *Technologie comme voyage* : Tu choisis une stack comme on choisit un
   moyen de transport ou un itinéraire. Elle influence ton expérience, ton
   interface, et ton récit.

🧰 Stack Selector

Avant chaque session, tu choisis :
Catégorie Options ville Options nature
Front-end React, Vue, Leaflet Svelte, Vanilla JS, Web Audio API
Back-end Node.js, Django, Fastify Express, Flask, low-power server
Base de données MongoDB, Postgres SQLite, JSON flat file
Capteurs GPS, caméra, social login micro, accéléromètre, météo

Chaque stack est affichée dans le front-end, avec ses composants, ses
usages, et les profils associés.
✨ Fonctionnalités

   -

   *Promenade libre* : Poste des messages à toute heure, avec ou sans
   localisation.
   -

   *Crépuscule → Aube* : Fenêtre “nocturne” configurable pour tagger
   automatiquement les posts.
   -

   *Photos et messages* : Upload d’images avec légendes, stockage des
   timestamps.
   -

   *Carnet de connaissances* : Base “people” pour noter les personnes
   rencontrées et les lier à des lieux.
   -

   *Navigation HTML* : Menu statique pour explorer les posts, personnes,
   lieux.
   -

   *Export* : Dump SQL et export JSON des posts.

🧅 Anonymous Posting Engine

   -

   Publication sans identité
   -

   Masquage de métadonnées :
   -

      Précision GPS (exacte, quartier, ville)
      -

      Adresse (appartement, étage, rue)
      -

      Indices de transport (bus, métro, zone piétonne)
      -

      Consentement dynamique pour le partage

🧪 Simulated Conversations & Posts

   -

   Génère des posts réalistes selon le lieu et l’heure
   -

   Social login optionnel pour publier des données personnelles
   -

   Backend : envoi de SMS, e-mails, messages vocaux
   -

   Frontend : infos sur les gens (âge, aire d’activité, style de
   publication)

🧑‍💻 Interface exploratoire

   -

   Menu pour choisir une stack complète
   -

   Ajout de profils liés à la tech :
   -

      Nom, avatar
      -

      Localisation GPS fictive
      -

      Intérêts, style de post
      -

      Adresse (apt, étage, rue)
      -

   Visualisation de la stack utilisée pendant la session

🗃️ API sociale

   -

   Base de données inspirée de Twitter ou Facebook
   -

   L’API reflète la stack utilisée pour “voyager”
   -

   Chaque post est une empreinte technologique et humaine

📦 Structure du dépôt
Code

promenade-stack-voyageur/
├── stacks/
│   ├── frontend/
│   ├── backend/
│   ├── database/
│   ├── sensors/
│   └── presets/
├── sessions/
│   ├── ville/
│   └── nature/
├── scripts/
├── api/
├── frontend/
├── docs/
└── README.md
