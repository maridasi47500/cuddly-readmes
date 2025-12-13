🕰️ Jeu de Cartes Prédictif — Timestamp Oracle🔮 Présentation

Ce projet est une plateforme interactive qui combine :

   -

   Des *cartes photo* (réelles ou générées par IA) représentant des
   moments, des lieux, ou des personnes
   -

   Un système de *timestamp* pour chaque interaction, affiché en "time ago"
   ou via un *tampon CSS dessiné*
   -

   Une interface multilingue (*i18n*) pour compter, traduire et filtrer les
   contenus
   -

   Un serveur IA capable de *modifier dynamiquement le contenu* selon la
   date, le lieu et le contexte
   -

   Des *prompts générés automatiquement* pour simuler des dialogues dans
   des situations spécifiques
   -

   Des technologies d’*accessibilité* pour rendre l’expérience inclusive

🧩 Fonctionnalités

   -

   📸 *Cartes temporelles* : Chaque carte est liée à un timestamp et peut
   être utilisée pour prédire ou raconter un futur possible.
   -

   🗣️ *Dialogue IA* : L’IA propose des rôles et des dialogues selon le
   contexte spatio-temporel.
   -

   🌐 *i18n & Traduction* : Comptage des utilisateurs, posts, items, et
   traduction dynamique des liens.
   -

   🧠 *Serveur IA* : Modifie les posts selon le lieu, la date et l’heure,
   avec des suggestions de contenu.
   -

   🧭 *Accessibilité* : Navigation optimisée, prompts vocaux, et
   compatibilité avec lecteurs d’écran.
   -

   🧱 *Architecture* : Utilise des media queries, templates, partials et
   requêtes base de données pour afficher les profils et contenus.

🛠️ Technologies
Composant Technologie utilisée
Frontend HTML, CSS (tampons dessinés), JS, Media Queries
Backend Node.js  / Express / Django (au choix)
IA API GPT / modèle local
Base de données PostgreSQL / MongoDB
i18n i18next / vue-i18n / react-intl
Accessibilité ARIA, VoiceOver, prompts vocaux
📦 Installation
bash

git clone https://github.com/ton-utilisateur/timestamp-oracle.git
cd timestamp-oracle
npm install
npm start

🗺️ Exemple d’usage

Une carte générée montre une ruelle à Tokyo, datée du 7 septembre 2025 à
12h49. L’IA propose : “Imagine que tu croises un inconnu ici. Que dirais-tu
?” Le post est modifié selon le fuseau horaire et les interactions passées.
