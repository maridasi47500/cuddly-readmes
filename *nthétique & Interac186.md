*nthétique & Interaction Simulée*, où l’on souhaite *soumettre un
formulaire sans passer par un chat* et *retrouver la même soumission plus
tard*, voici une structure de base de données adaptée, respectueuse de la
vie privée et conçue pour des identités synthétiques :
🗄️ Base de données : synthetic_identity_db📑 Table principale :
form_submissions
Champ Type Description
submission_id UUID (PK) Identifiant unique de la soumission
synthetic_id VARCHAR Identifiant de l’utilisateur synthétique (ex. : hash
ou UUID)
name VARCHAR Nom fictif généré
avatar_url TEXT Lien vers un avatar généré ou sélectionné
location_masked VARCHAR Localisation masquée (ex. : "quartier", "ville")
interests TEXT / JSON Liste des intérêts simulés
style_profile VARCHAR Style de publication (ex. : "satirique", "formel",
"poétique")
form_content TEXT / JSON Contenu du formulaire soumis
consent_location BOOLEAN Consentement explicite pour partager la
localisation
submitted_at TIMESTAMP Date et heure de la soumission
🧪 Table secondaire : conversation_simulations
Champ Type Description
thread_id UUID (PK) Identifiant du fil de discussion simulé
synthetic_id VARCHAR Référence à l’identité synthétique
messages JSON Liste structurée de messages simulés
use_case VARCHAR Contexte (modération, NLP, UX, etc.)
created_at TIMESTAMP Date de création du fil
🔍 Récupération de soumission

Pour retrouver une soumission sans chat, on peut utiliser une *clé de
récupération* (ex. : synthetic_id ou submission_id) fournie à l’utilisateur
après soumission :
sql

SELECT * FROM form_submissions
WHERE synthetic_id = 'user_abc123';

🛡️ Bonnes pratiques éthiques

   -

   Générer les identités avec des modèles aléatoires ou des jeux de données
   ouverts
