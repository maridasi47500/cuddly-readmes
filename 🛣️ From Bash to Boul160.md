🛣️ From Bash to Boulevard Avenue

*A journey from simple login to social publishing, from dusk till dawn.*
Overview

This project lets users post time-bound sessions — “from dawn till dusk” or
“dusk till dawn” — tied to real-world places. Starting with a simple login,
users can upgrade to social login and publish sessions enriched with GPS,
address, apartment, floor, and transportation details. Optional publishing
via LinkedIn or Facebook UUIDs lets users share their journey from
boulevard to natural gem.
✨ Features

   -

   *Simple login*: Start with email/password or magic link.
   -

   *Social login*: Upgrade to Google, Facebook, LinkedIn, or Apple.
   -

   *Time-based sessions*: Choose between *dawn → dusk* or *dusk → dawn*.
   -

   *Place metadata*:
   -

      GPS coordinates
      -

      Full address
      -

      Apartment & floor
      -

      Nearby transportation (bus, metro, etc.)
      -

   *Publishing options*:
   -

      With or without LinkedIn/Facebook UUID
      -

      Local-only or cross-platform
      -

   *Place types*: Boulevard, Avenue, Natural Gem, or Custom

🚀 Quick Start
bash

# Clone the repo
git clone https://github.com/your-org/boulevard-avenue.git
cd boulevard-avenue

# Install dependencies
npm install

# Start the app
npm run dev

🗺️ Session Example
json

{
  "timeframe": "DUSK_TO_DAWN",
  "place": {
    "label": "Boulevard Haussmann",
    "type": "BOULEVARD",
    "gps": { "lat": 48.8742, "lng": 2.3301 },
    "address": {
      "line1": "102 Boulevard Haussmann",
      "city": "Paris",
      "postal_code": "75008",
      "country": "FR"
    },
    "apartment": "B12",
    "floor": "3",
    "transportation": ["Metro M9 Saint-Augustin", "Bus 22"]
  },
  "content": "Evening walk through the city lights.",
  "publish": {
    "linkedin_uuid": "abc-123",
    "facebook_uuid": null
  }
}

🔐 Authentication Flow
Step Description
Bash login Email/password or magic link
Social upgrade OAuth with Google, Facebook, etc.
UUID binding Link LinkedIn/Facebook UUIDs
Privacy control Choose visibility per session
🌍 Place Types
Type Description
BOULEVARD Urban street with cultural flair
AVENUE Wide road, often tree-lined
NATURAL_GEM Parks, forests, beaches, etc.
CUSTOM User-defined location type
📝 Publishing Modes

   -

   *Local only*: Save session without external sharing.
   -

   *LinkedIn*: Publish using linked UUID.
   -

   *Facebook*: Publish using linked UUID.
   -

   *Hybrid*: Share to one or both platforms.

🛤️ From Boulevard to Natural Gem

Users can trace a path from urban spaces to nature by tagging sessions with
place types. This creates a narrative arc — a digital journey through time
and space.
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

   *Maps*: Google Maps API

📄 License

MIT — free to use, modify, and share.
