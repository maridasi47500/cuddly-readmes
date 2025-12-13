🌐 EchoVoyageStreet x TravelBuddy — Ton monde, résonnant de souvenirs

*EchoVoyage x TravelBuddy* est une plateforme immersive qui transforme
chaque ville en expérience vivante, chaque voyage en quête sensorielle, et
chaque retour chez soi en redécouverte intime. C’est une invitation à
explorer le monde à travers les sons, les paysages, les émotions et les
récits — et à faire de ta propre ville un miroir vibrant de tes aventures
passées.
🧠 Vision du projet

Revenir chez soi, c’est redécouvrir sa ville à travers les sons, les
odeurs, les émotions du voyage. Chaque rue devient une mélodie. Chaque
boutique, un musée de souvenirs sensoriels. *Mais avant de partir, tu dois
créer.* Une application, un poème, un jeu, une chanson — quelque chose qui
te servira de boussole intérieure.

🔁 Cycle d’expérience

   1.

   *Tu crées* : avant le départ, tu fabriques une œuvre, un outil, une
   capsule personnelle
   2.

   *Tu voyages* : tu enregistres des sons, des ambiances, des émotions
   3.

   *Tu explores* : tu vis des quêtes, tu découvres des paysages et des
   lieux secrets
   4.

   *Tu reviens* : ta ville devient un miroir de ce que tu as vécu ailleurs
   5.

   *Tu revisites* : les lieux familiers résonnent de souvenirs lointains
   6.

   *Tu repars* : enrichi, prêt pour une nouvelle aventure

📱 Fonctionnalités clés
Fonction Description
🧳 Carnet de voyage sonore Chaque destination génère une capsule
sensorielle (sons, photos, émotions)
🎧 Rue musicale L’app joue des sons liés à tes voyages pendant tes balades
locales
🏪 Souvenir vivant Les magasins deviennent des points de mémoire sensorielle
💎 Ruby GPS émotionnel Te guide dans ta ville selon ton mood, l’heure, et
tes souvenirs
🚀 Prêt au départ Avant de partir, tu crées quelque chose de nouveau
🧱 Limite de carte Zones floues où la réalité se dissout et l’imaginaire
prend le relais
🧱 Limite de Map — Le bord du connu

*“C’est là où la ville s’arrête… ou commence à rêver.”*

La *limite de carte* devient :

   -

   Un *déclencheur sensoriel* : sons, odeurs, souvenirs se mélangent
   -

   Une *zone floue* : les repères se dissolvent, l’imaginaire prend le
   relais
   -

   Un *défi personnel* : pour bouger, tu dois créer quelque chose
   -

   Un *événement JavaScript* : déclenche des effets visuels et sonores à
   l’approche

🎛 Exemple d’événement JavaScript
javascript
document.addEventListener('mapLimitReached', () => {
  playInstrumentSound(userProfile.instrument);
  showMemoryOverlay();
  triggerLimitMoodText();
});

   -

   playInstrumentSound() : joue le son associé à l’instrument du voyageur
   (ex. synthé rétro, tambour tribal)
   -

   showMemoryOverlay() : affiche une couche visuelle avec photos et
   souvenirs
   -

   triggerLimitMoodText() : affiche un texte introspectif depuis
   limit_mood.md

🎼 Instrument du voyageur

Chaque profil contient un *instrument de voyage* :
yaml
instrument: "violon rêveur"

Cet instrument :

   -

   Influence les sons joués à l’approche des limites
   -

   Modifie l’ambiance musicale des playlists
   -

   Peut être utilisé comme déclencheur narratif dans les quêtes

📁 Structure du dépôt

EchoVoyage/
│
├── profiles/                    # Profils personnalisés (.yaml/.json)
├── cities/                      # Dossiers par ville avec photos,
playlists, quêtes
├── envyage/                     # Milieux naturels et ambiances sonores
├── quests/                      # Quêtes interactives et récits immersifs
├── playlists/                   # Génération dynamique via API musicale
├── gallery/                     # Galerie de cartes postales sonores
├── map/                         # Carte du monde interactive
├── memories/                    # Carnet de voyage collaboratif
├── map_limits/                  # Zones de bascule et déclencheurs
│   ├── villeurbanne_limit.json
│   ├── limit_sounds/
│   ├── limit_mood.md
│   ├── limit_trigger.py
│   └── creations_before_departure/
└── README.md
