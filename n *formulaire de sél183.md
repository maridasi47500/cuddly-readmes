n *formulaire de sélection de stack* qui génère automatiquement une
*application
avec un front-end inspiré de l’IA de la région de Kourou* 🌴🚀. Et pour
couronner le tout, un *script Bash* qui installe et lance le projet en un
clin d’œil.
🧠 Étape 1 : Formulaire de sélection de stack (HTML + JS)

Ce formulaire permet à l’utilisateur de choisir les technologies pour le
front-end, back-end et base de données.
html

<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Créateur d'App IA Régionale</title>
</head>
<body>
  <h1>🛠️ Sélectionne ta stack</h1>
  <form id="stackForm">
    <label>Front-end :
      <select name="frontend">
        <option value="react">React</option>
        <option value="vue">Vue.js</option>
      </select>
    </label><br>

    <label>Back-end :
      <select name="backend">
        <option value="express">Node.js + Express</option>
        <option value="flask">Python + Flask</option>
      </select>
    </label><br>

    <label>Base de données :
      <select name="database">
        <option value="postgres">PostgreSQL</option>
        <option value="mongodb">MongoDB</option>
      </select>
    </label><br>

    <button type="submit">Générer le script</button>
  </form>

  <pre id="bashScript"></pre>

  <script>
    document.getElementById('stackForm').addEventListener('submit',
function(e) {
      e.preventDefault();
      const frontend = e.target.frontend.value;
      const backend = e.target.backend.value;
      const database = e.target.database.value;

      let script = `#!/bin/bash
echo "🚀 Création de ton app IA régionale..."
mkdir ai-region-app && cd ai-region-app
`;

      if (frontend === 'react') {
        script += `npx create-react-app frontend\n`;
      } else {
        script += `npm install -g @vue/cli && vue create frontend\n`;
      }

      if (backend === 'express') {
        script += `mkdir backend && cd backend && npm init -y && npm
install express cors\n`;
      } else {
        script += `mkdir backend && cd backend && python3 -m venv env
&& source env/bin/activate && pip install flask\n`;
      }

      if (database === 'postgres') {
        script += `echo "📦 PostgreSQL recommandé. Assure-toi qu'il
est installé."\n`;
      } else {
        script += `npm install mongodb\n`;
      }

      script += `echo "🌴 Ton app est prête à être personnalisée avec
une ambiance Kourou : jungle, fusée, créole et soleil."\n`;

      document.getElementById('bashScript').textContent = script;
    });
  </script>
</body>
</html>

🖼️ Front-end inspiré de Kourou

Une fois le projet généré, tu peux personnaliser le front-end avec :

   -

   *Couleurs* : vert forêt, bleu spatial, jaune soleil
   -

   *Typo* : Poppins + Amatic SC
   -

   *Composants* : avatars synthétiques, fond animé selon l’heure locale
   -

   *Messages IA* : en français avec des touches de créole guyanais

🧪 Exemple de composant React stylisé
jsx

function AILocale() {
  return (
    <div className="bg-gradient-to-br from-yellow-100 to-green-300 p-6
rounded shadow">
      <h2 className="text-2xl font-bold text-green-900">AI de Kourou</h2>
      <p className="text-gray-700">Mo ka palé avè zot pou nou kodé ansanm !</p>
      <img src="/avatar_kourou.png" alt="Avatar IA régionale" />
    </div>
  );
}
