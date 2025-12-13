Meetup
ruby

t.references :user
t.string :location_city
t.string :location_country
t.datetime :met_on
t.text :notes

📸 PhotoMoment
ruby

t.references :user
t.string :title
t.string :location_city
t.string :location_country
t.string :image_url
t.datetime :taken_at
t.text :caption

🍽️ SharedMeal
ruby

t.references :user
t.string :dish_name
t.string :restaurant_name
t.string :location_city
t.string :location_country
t.integer :people_count
t.datetime :date
t.text :conversation_notes

🎨 LocalArtEncounter
ruby

t.references :user
t.string :art_type
t.string :artist_name
t.string :location_city
t.string :location_country
t.datetime :date
t.text :reaction
