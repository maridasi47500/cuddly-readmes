# 🌍 DataNomad — Le programme qui voyage dans les fragments

Bienvenue dans un projet qui **refuse de tout voir**.
Ici, on interroge une base de données comme on interroge la vie :
avec des filtres, des angles, des instants.
On ne lit jamais toutes les colonnes. On ne veut pas toutes les réponses.
On veut juste **voir des gens**, **des visages**, **des moments**,
dans une **template CSS** qui raconte une histoire.

---

## 🧠 Manifeste

> “Je vois ce que j’ai programmé… mais seulement après.”
> — Le programme

Ce projet est une ode à la **subjectivité volontaire**.
Comme dans `sqlite3`, tu peux faire une requête, mais tu ne verras que ce
que tu as demandé.
Et ce que tu as demandé, tu ne le comprends qu’après l’avoir vu.

---

## 📸 Ce que le programme affiche

- 👤 Des gens (nom, humeur, photo)
- 🕰️ Des timestamps (quand la photo a été prise, quand tu l’as vue)
- 🌍 Des lieux (où tu es, où tu veux aller)
- 🎨 Une mise en forme CSS qui donne du sens à l’instant

---

## 🧳 Ton ticket de voyage

Chaque requête est un **ticket tamponné**.
Elle te dit où tu es, quand tu es, ou où tu veux que le programme t’amène.
Et ton **nouveau post** — ton fragment affiché — peut être modifié selon :
- 🌐 La langue du lieu
- 📅 La date du moment
- 📍 L’endroit où tu te trouves

---

## 🗂️ Structure du projet

| Dossier/Fichier     | Description                                      |
|---------------------|--------------------------------------------------|
| `templates/`        | Fichiers HTML/CSS pour afficher les données      |
| `data.db`           | Base SQLite contenant les fragments humains      |
| `queries/`          | Requêtes SQL filtrées, jamais complètes          |
| `logger.py`         | Script pour enregistrer ton lieu et ton moment   |
| `README.md`         | Ce manifeste                                     |

---

## 🛠️ Exemple de requête

```sql
SELECT nom, photo, timestamp
FROM personnes
WHERE humeur IS NOT NULL
LIMIT 5;
