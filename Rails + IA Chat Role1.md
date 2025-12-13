Rails + IA Chat Role Logger

Une application Ruby on Rails intégrant une IA qui joue des rôles dans des
dialogues simulés (boulanger, coiffeuse, etc.), enregistre les
conversations avec des métadonnées précises, et peut générer un faux profil
visuel lié au lieu et au contexte.
🎯 Objectif

Capturer et stocker des *interactions simulées* entre l’utilisateur et une
IA jouant un rôle, avec :

   -

   🕒 Horodatage précis (jusqu’à la milliseconde)
   -

   📍 Lieu (nom, GPS)
   -

   🧑‍🎤 Rôle joué par l’IA (ex. : boulanger, coiffeuse)
   -

   🌞 Moment de la journée (jour/nuit)
   -

   📅 Granularité temporelle variable : année seule, année+mois, date sans
   heure, datetime complet
   -

   🖼️ Image de profil simulée selon le lieu et le rôle

class Post < ApplicationRecord
  t.text     :dialogue           # Contenu de la conversation
  t.string   :role               # Rôle joué par l’IA
  t.string   :location_name      # Nom du lieu (ex. "Boulangerie du coin")
  t.string   :location_gps       # Coordonnées GPS
  t.datetime :timestamp          # Date et heure complète
  t.date     :date_only          # Date sans heure
  t.integer  :year               # Année seule
  t.string   :year_month         # Format "YYYY-MM"
  t.string   :daytime            # "day" ou "night"
  t.string   :context            # Type de lieu (ex. "boulangerie")
  t.string   :profile_image_url  # URL d’une image simulée
end

<%= form_with model: @post do |f| %>
  <%= f.label :role %>
  <%= f.select :role, ["boulanger", "coiffeuse", "serveur"] %>

  <%= f.label :dialogue %>
  <%= f.text_area :dialogue %>

  <%= f.label :location_name %>
  <%= f.text_field :location_name %>

  <%= f.label :location_gps %>
  <%= f.text_field :location_gps %>

  <%= f.label :timestamp %>
  <%= f.datetime_select :timestamp %>

  <%= f.label :daytime %>
  <%= f.select :daytime, ["day", "night"] %>

  <%= f.label :context %>
  <%= f.select :context, ["boulangerie", "coiffeur", "pharmacie"] %>

  <%= f.submit "Enregistrer" %>
<% end %>


GET    /posts                          # Tous les posts
GET    /posts/:id                      # Détail d’un post
POST   /posts                          # Création
GET    /posts?year=2025                # Filtrer par année
GET    /posts?year_month=2025-10       # Filtrer par année et mois
GET    /posts?daytime=night            # Filtrer par moment de la journée
GET    /posts?context=boulangerie      # Filtrer par contexte
GET    /posts?location_gps=5.0,52.0    # Filtrer par coordonnées GPS
📸 Faux profil visuel

L’IA peut générer ou rechercher une image de profil simulée selon le rôle
et le lieu. Exemples :

   -

   Images de faux profils masculins sur Pikwizard
   -

   Photos de faux profils sur Unsplash
   -

   Images de profils fictifs sur Vecteezy

📊 Pourquoi plus de données = meilleur rôle

   -

   Une IA qui connaît l’heure exacte, le lieu, le type de commerce et le
   moment de la journée peut adapter son ton, ses suggestions et son
   vocabulaire.
   -

   Cela permet de *rejouer* ou *analyser* les interactions selon des
   critères temporels ou géographiques.
   -

   Plus le post est riche, plus le rôle joué est *réaliste* et *immersif*.

Souhaites-tu que je t’aide à générer ce fichier README.md ou à créer les
modèles et contrôleurs Rails correspondants ?
