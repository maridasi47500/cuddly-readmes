dans le readme : tu as des image de super heros qui se passe "nulel part"
qui sont tres different avec le lieu/l'endroit /job que t'as, tu dois
rapprocher lesd deux. 🎯 Objectif

    Rapprocher une perception héroïque (idéalisée) de soi avec une réalité
locale (âge, ville, mobilité, métier).

🔄 Comment ça marche

Chaque image est générée ou sélectionnée selon deux axes :
Élément Source Exemple
🧠 Perception de soi super_hero_mode.py "Je me sens comme Spider-Man :
agile, débrouillard, discret."
📍 Réalité terrain age_tracker.py, transport_mode.py, GPS "J’ai 22 ans, je
suis à Cayenne, je me déplace à vélo."

Ces deux dimensions sont croisées pour activer un rôle via le système
become :if user.age >= 18 and user.in_city("Cayenne") and
user.transport_mode in ["vélo", "métro"]:
    user.become("développeur")
je suis dans un gare? je suis dans un cafe. je transporte des cv a velo
dans la rue. je suis dans une salle d’attente pour un CDD en comptabilité🧠
