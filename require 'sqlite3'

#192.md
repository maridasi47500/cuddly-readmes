require 'sqlite3'

# Connexion ou création de la base
DB = SQLite3::Database.new "voyance_people.db"

# Création de la table si elle n'existe pas
DB.execute <<-SQL
  CREATE TABLE IF NOT EXISTS people (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT,
    age INTEGER,
    email TEXT,
    address TEXT,
    phone TEXT,
    gender TEXT,
    occupation TEXT
  );
SQL

# Liste complète des attributs
ALL_ATTRIBUTES = [:name, :age, :email, :address, :phone, :gender,
:occupation]

# Modèle Person dynamique
class Person
  def self.define_accessors(attrs)
    attrs.each do |attr|
      attr_reader attr
      attr_writer attr
    end
  end

  define_accessors(ALL_ATTRIBUTES)

  def initialize(attrs = {})
    attrs.each do |key, value|
      instance_variable_set("@#{key}", value)
    end
  end

  def save_to_db
    columns = ALL_ATTRIBUTES.select { |attr|
instance_variable_get("@#{attr}") }
    values = columns.map { |attr| instance_variable_get("@#{attr}") }

    placeholders = (["?"] * columns.size).join(", ")
    DB.execute("INSERT INTO people (#{columns.join(", ")}) VALUES
(#{placeholders})", values)
  end
end

# 🔮 Génération de plusieurs personnes
people_data = [
  { name: "Luna", age: 28, email: "luna@example.com", occupation: "Voyante"
},
  { name: "Sol", age: 35, email: "sol@example.com", address: "Rue des
Étoiles", gender: "Homme" },
  { name: "Orion", age: 42, phone: "0594-987654", occupation: "Astrologue" }
]

# Insertion dans la base
people_data.each do |data|
  person = Person.new(data)
  person.save_to_db
end

# 📋 Affichage des personnes insérées
puts "\n✨ Liste des personnes dans la base :"
DB.execute("SELECT * FROM people") do |row|
  puts row.inspect
end
