# 🏋️‍♀️🏈 That Sportsperson — Galerie de Perspectives Urbaines

> _"Tu marches dans ton quartier, mais dans l’application, tu explores des
villes entières.
Tu vois des visages, des âges, des humeurs. Tu es ce sportsperson — celui
qui traverse les données comme on traverse les rues."_

---

## 🖼️ Concept

**That Sportsperson** est une application hybride entre galerie, carte
interactive et moteur IA.
Elle te permet de te promener dans un **carousel de perspectives**, une
**collection de photos**, ou un **quartier virtuel**, où chaque donnée est
une histoire, chaque image une intention, chaque coordonnée GPS une
possibilité.

---

## 📦 Fonctionnalités

- **🗺️ Galerie de plans** : chaque "plan" est une vue — une ville, un
visage, une humeur, une trajectoire.
- **📸 Photos du sportsperson** : parfois floues, parfois nettes, parfois
absentes — mais toujours porteuses de sens.
- **📅 Données de voyage** : lieux visités, dates, météo, ambiance,
interactions.
- **🧠 Paramètres IA** : coordonnées GPS de magasins, jobs potentiels,
lieux d’intérêt — utilisés pour générer des suggestions et des croisements.
- **🔄 Croisement de données** : une base unique, des tables multiples —
les données se rencontrent, se répondent, se transforment.

---

## 🗃️ Structure des données

| Table             | Contenu
   |
|-------------------|-----------------------------------------------------------|
| `users`           | Identité du sportsperson — âge, mood, style, énergie
     |
| `photos`          | Galerie personnelle ou collective — avec ou sans
visages |
| `trips`           | Données de voyage — dates, lieux, ambiance
     |
| `locations`       | Coordonnées GPS — magasins, jobs, repères IA
     |
| `perspectives`    | Plans urbains, vues mentales, projections IA
     |
| `interactions`    | Liens entre utilisateur et suggestions IA
    |

---

## 🚀 Lancer l'application

```bash
git clone https://github.com/ton-utilisateur/that-sportsperson.git
cd that-sportsperson
npm install # ou lein deps / clojure -M
npm run dev # ou lein run / clojure -M:run
