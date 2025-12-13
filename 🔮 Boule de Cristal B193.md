🔮 Boule de Cristal Boule de Cristal est une application qui aide chacun à
devenir ce qu’il rêve d’être — un métier, une activité, une entreprise — en
fonction de sa localisation, de son âge, de ses moyens de transport et de
ses perceptions personnelles. Elle agit comme une interface magique entre
ton CV, les offres disponibles, et ta capacité à bouger en ville pour
saisir les opportunités. ✨ Philosophie "Become" Le système become est
inspiré de Rails et de l’internationalisation i18n. Il permet à un
utilisateur de changer d’état ou de rôle dans l’application, à condition de
remplir certains critères : 🎂 Avoir 18 ans minimum pour accéder aux rôles
professionnels 📍 Être géolocalisé dans une zone compatible 🚲 Disposer
d’un mode de transport adapté 🧠 Avoir une perception réaliste ou idéalisée
de soi (via super_hero_mode.py)if user.age >= 18 and
user.in_city("Cayenne") and user.transport_mode in ["vélo", "métro"]:
user.become("développeur") Localisation & Mobilité L’application utilise le
GPS pour : Détecter ta position actuelle Proposer des activités locales
Évaluer ta capacité à te déplacer (réel ou fictif) 🔧 Modules associés
transport_mode.py : Choix et suivi des moyens de transport (vélo, métro,
dragon, téléportation…) age_tracker.py : Calcule ton âge, date tes actions,
affiche le temps écoulé depuis chaque étape voir une voyante du langage
ruby qui utilise les fonction de temps, time ago in words, de compter avec
i18n, de hasard, et la fonction become avec un objet, avec un script (des
entrees texte) 🏢 Nos entreprises, nos métiers Chaque entreprise dans
l’application propose : Une liste de métiers disponibles Les types de
contrat : CDI, CDD, freelance, stage, alternance Les conditions d’accès :
âge, localisation, mobilité 📄 CV & eCandidature Tu peux : 📤 Importer ton
CV 🔍 Consulter les offres disponibles 📨 Postuler via une eCandidature
intégrée 🌍 i18n & Bougies qui brillent Ton âge évolue, et avec lui, ton
parcours. L’application adapte ses messages et rôles selon ton nombre de
bougies 🎂 :fr: age: under_18: "Tu explores encore le monde. Rêve,
découvre, prépare-toi." 18: "Bienvenue dans le monde professionnel. Tu peux
devenir ce que tu veux." 30: "Tu affirmes ton parcours. Tu peux guider ou
te réinventer."✨ Voici un script Ruby façon “voyante numérique” pour Boule
de Cristal, combinant les modules i18n, time_ago_in_words, rand, et la
logique magique du become. Il prend des entrées texte et prédit ton avenir
professionnel selon ton profil :r# Modèle parent
class Utilisateur < ApplicationRecord
  def eligible?
    age >= 18 && ville.downcase == "cayenne" && ["vélo",
"métro"].include?(transport)
  end

  def prédiction
    rôles = [Développeur, Designer, Entrepreneur]
    rôle_choisi = rôles.sample
    if eligible?
      nouveau_rôle = self.becomes(rôle_choisi)
      puts "#{nom}, tu deviens #{rôle_choisi.name
<http://xn--rle_choisi-rbb.name>} ✨"
      nouveau_rôle.message_de_rôle
    else
      puts "#{nom}, ton destin est encore en gestation… 🌠"
    end
  end
end

# Modèles enfants STI
class Développeur < Utilisateur
  def message_de_rôle
    puts "Tu codes l’avenir avec Ruby et Rails 💻"
  end
end

class Designer < Utilisateur
  def message_de_rôle
    puts "Tu dessines des interfaces qui enchantent ✨"
  end
end

class Entrepreneur < Utilisateur
  def message_de_rôle
    puts "Tu bâtis ton empire depuis Cayenne 🚀"
  end
end
