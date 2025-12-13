🌌 Promenade

Un micro-projet pour “se promener” IRL ou virtuellement, publier des
messages et photos du crépuscule à l’aube, avec ou sans GPS, et garder une
trace en base de données. Pensé comme une errance libre, augmentée par la
technologie mais jamais dictée par elle.
🧭 Présentation

   -

   *Idée* : Une appli légère pour se balader, publier des messages et
   photos “from dusk till dawn”, enrichir une base de connaissances des gens
   que tu croises, et enregistrer (optionnellement) ta position GPS.
   -

   *Philosophie* : La liberté d’errance d’abord ; les métadonnées ensuite.
   Tu peux publier sans GPS, sans identifiant, juste pour le plaisir de la
   trace.
   -

   *Stack* :
   -

      Bash (scripts)
      -

      Node.js  + Express (API)
      -

      SQLite ou Postgres (base de données)
      -

      HTML/CSS vanilla (interface minimale)

✨ Fonctionnalités principales

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

   *GPS optionnel* : Si fourni, on enregistre ; sinon, on publie quand même.
   -

   *Export* : Dump SQL et export JSON des posts.

🧅 Moteur de publication anonyme

Les utilisateurs peuvent publier sans révéler leur identité, avec des
options de masquage :

   -

   Contrôle de précision GPS : exact, quartier, ville
   -

   Masquage d’adresse : appartement, étage, rue
   -

   Indices de transport : bus, métro, zone piétonne
   -

   Partage de localisation basé sur consentement

🧪 Génération de posts simulés

   -

   Génère ou rédige des posts réalistes selon le contexte : urbain ou
   naturel
   -

   Utilise un *social login* pour publier des données personnelles
   (optionnel)
   -

   Le backend permet l’envoi de SMS, e-mails ou messages vocaux
   -

   Le frontend affiche des infos sur les gens : âge, aire d’activité, style
   de publication

🧰 Interface et exploration technique

   -

   Menu pour choisir une stack complète (frontend, backend, base)
   -

   Ajout de profils liés à la tech : nom, avatar, localisation GPS fictive,
   intérêts, style de post, adresse (apt, étage, rue)
   -

   Affichage de la stack utilisée pendant la durée de la promenade (dusk
   till dawn ou dawn till dusk)

🗃️ API sociale

   -

   Base de données inspirée de Twitter ou Facebook
   -

   L’API reflète la stack utilisée pour “voyager”
   -

   Chaque post est une empreinte technologique et humaine
