🌇 From Bash to Boulevard

*“From dusk till dawn” or “dawn till dusk” — a journey through login modes,
places, and stories.*
🧭 Overview

This project is a time-aware, place-rich platform that starts with simple
login and evolves into social login with popular views. Users post sessions
tied to real-world places — from bustling boulevards to serene natural gems
— enriched with GPS, address, apartment, floor, and transportation
metadata. AI prompts guide the journey, while itinerary sharing spans
radio, TV, SMS, email, and phone.
🔐 Login Modes
Mode Description
Bash Login Command-line or basic email/password
Social Login Google, Facebook, LinkedIn, Apple
Timeframe Login Choose “Dawn → Dusk” or “Dusk → Dawn”
Popular Views See trending sessions and places
🗺️ Place Metadata

   -

   *GPS Coordinates*: Latitude & longitude
   -

   *Address*: Full formatted address
   -

   *Apartment & Floor*: Optional details for precision
   -

   *Transportation*: Nearby metro, bus, bike stations
   -

   *Place Type*: Boulevard, Avenue, City, Natural Gem

📝 Session Example
json

{
  "timeframe": "DUSK_TO_DAWN",
  "place": {
    "label": "Boulevard Saint-Michel",
    "type": "BOULEVARD",
    "gps": { "lat": 48.8462, "lng": 2.3430 },
    "address": {
      "line1": "12 Boulevard Saint-Michel",
      "city": "Paris",
      "postal_code": "75006",
      "country": "FR"
    },
    "apartment": "A3",
    "floor": "5",
    "transportation": ["Metro M4 Odéon", "Bus 38"]
  },
  "content": "Late-night poetry reading under the street lamps.",
  "ai_prompt": "Suggest a caption for a moody urban night.",
  "publish": {
    "linkedin_uuid": "abc-123",
    "facebook_uuid": null
  },
  "itinerary": {
    "share_via": ["SMS", "Email", "Phone", "Radio", "TV"],
    "gps_route": "https://maps.example.com/route/xyz"
  }
}

🤖 AI Prompts

   -

   *Caption suggestions*: Based on place, time, and mood
   -

   *Route planning*: GPS-based itinerary generation
   -

   *Gossip filter*: Detect and flag spicy anonymous posts
   -

   *Ambience tagging*: Urban, natural, romantic, mysterious

📡 Communication Channels
Channel Use Case
SMS Share session or itinerary
Email Notify friends or followers
Phone Voice itinerary or updates
Radio Broadcast trending sessions
TV Feature popular places or stories
🛤️ Journey Flow
text

Bash → Database → Boulevard → Avenue → GPS → Transportation → City →
Natural Gem → AI → Communication

Each step is a layer of experience — from raw data to rich storytelling.
📦 Tech Stack

   -

   *Frontend*: React + Tailwind
   -

   *Backend*: Node.js  + Express
   -

   *Database*: PostgreSQL
   -

   *Auth*: JWT + OAuth
   -

   *AI*: Prompt engine with NLP
   -

   *Maps*: Google Maps API
   -

   *Comms*: Twilio, SendGrid, Broadcast APIs

📄 License

MIT — open to remix, reuse, and reimagine.
