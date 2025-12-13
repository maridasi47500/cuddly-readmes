🔮 Boule de Cristal

*Boule de Cristal* est une application qui aide chacun à *devenir* ce qu’il
rêve d’être — un métier, une activité, une entreprise — en fonction de sa
*localisation*, de son *âge*, de ses *moyens de transport* et de ses
*perceptions
personnelles*.

Elle agit comme une interface magique entre ton *CV*, les *offres
disponibles*, et ta *capacité à bouger en ville* pour saisir les
opportunités.
✨ Philosophie "Become"

Le système become est inspiré de *Rails* et de l’internationalisation *i18n*.
Il permet à un utilisateur de *changer d’état ou de rôle* dans
l’application, à condition de remplir certains critères :

   -

   🎂 Avoir *18 ans minimum* pour accéder aux rôles professionnels
   -

   📍 Être *géolocalisé* dans une zone compatible
   -

   🚲 Disposer d’un *mode de transport* adapté
   -

   🧠 Avoir une *perception réaliste ou idéalisée* de soi (via
   super_hero_mode.py)if user.age >= 18 and user.in_city("Cayenne") and
   user.transport_mode in ["vélo", "métro"]:
       user.become("développeur")

 Localisation & Mobilité

L’application utilise le *GPS* pour :

   -

   Détecter ta *position actuelle*
   -

   Proposer des *activités locales*
   -

   Évaluer ta *capacité à te déplacer* (réel ou fictif)

🔧 Modules associés

   -

   transport_mode.py : Choix et suivi des moyens de transport (vélo, métro,
   dragon, téléportation…)
   -

   age_tracker.py : Calcule ton âge, date tes actions, affiche le temps
   écoulé depuis chaque étape

🧠 Perception de soi

Le module super_hero_mode.py évalue tes *perceptions personnelles* :

   -

   *Réalistes* : basées sur ton CV, ton expérience
   -

   *Idéalisées* : aspirations, rêves, projections

🎯 Objectif : ne *pas se sous-estimer*, ne *pas se surestimer*, mais
trouver un *équilibre juste* pour accéder aux rôles via become.
🏢 Nos entreprises, nos métiers

Chaque entreprise dans l’application propose :

   -

   Une liste de *métiers disponibles*
   -

   Les *types de contrat* : CDI, CDD, freelance, stage, alternance
   -

   Les *conditions d’accès* : âge, localisation, mobilité

📄 CV & eCandidature

Tu peux :

   -

   📤 Importer ton *CV*
   -

   🔍 Consulter les *offres disponibles*
   -

   📨 Postuler via une *eCandidature intégrée*

🌍 i18n & Bougies qui brillent

Ton *âge* évolue, et avec lui, ton parcours. L’application adapte ses
messages et rôles selon ton nombre de *bougies* 🎂 :fr:
  age:
    under_18: "Tu explores encore le monde. Rêve, découvre, prépare-toi."
    18: "Bienvenue dans le monde professionnel. Tu peux devenir ce que tu
veux."
    30: "Tu affirmes ton parcours. Tu peux guider ou te réinventer."
