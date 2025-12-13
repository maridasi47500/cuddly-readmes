🏙 Bus Ambiance Controller

Une application Python pour personnaliser l'ambiance lumineuse et musicale
dans un bus selon la ville et le nom du bus.
🚀 Fonctionnalités

   -

   Choisir une *ville* et un *nom de bus*
   -

   Programmer les *lumières extérieures* du bus
   -

   Contrôler les *lumières intérieures* via une *lampe Wi-Fi*
   -

   Diffuser de la *musique* dans le bus
   -

   Intégration avec *Google Home* pour lancer des radios ou des playlists

🛠️ Installation
🏙 Exemple d'utilisation
from bus_controller import BusAmbiance

bus = BusAmbiance(ville="Paris", nom_bus="Bus Lumière")
bus.programmer_lumieres_exterieures(couleur="bleu", heure="18:00")
bus.activer_lampe_wifi(intensite=70)
bus.lancer_musique(radio="FIP", duree_minutes=30)

Commandes Google Home

Voici quelques commandes vocales compatibles :

   -

   *"Hey Google, lance FIP dans le bus Lumière"*
   -

   *"Hey Google, éteins les lumières du bus à 22h"*
   -

   *"Hey Google, joue de la musique jazz pendant 45 minutes dans le bus
   Paris"*
   -

   *"Hey Google, change la couleur des lumières extérieures en rouge"*

📦 Dépendances

   -

   phue pour les lampes Philips Hue
   -

   pychromecast pour diffuser la musique
   -

   schedule pour la programmation horaire
