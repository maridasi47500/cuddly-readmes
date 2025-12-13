🛣️ From Bash to Boulevard

*A journey from simple login to social publishing, from dusk till dawn —
with a dash of anonymous gossip.*
🧭 Overview

This project lets users post time-bound sessions — “from dawn till dusk” or
“dusk till dawn” — tied to real-world places. Starting with a simple login,
users can upgrade to social login and publish sessions enriched with GPS,
address, apartment, floor, and transportation details. And yes — they can
post gossip using a fake profile, because sometimes the tea is best served
anonymously.
✨ Features

   -

   *Simple login*: Email/password or magic link.
   -

   *Social login*: Google, Facebook, LinkedIn, Apple.
   -

   *Anonymous mode*: Post as a fake profile (gossip-friendly).
   -

   *Time-based sessions*: Choose *dawn → dusk* or *dusk → dawn*.
   -

   *Place metadata*:
   -

      GPS coordinates
      -

      Full address
      -

      Apartment & floor
      -

      Nearby transportation
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
git clone https://github.com/your-org/boulevard-gossip.git
cd boulevard-gossip

# Install dependencies
npm install

# Start the app
npm run dev

🗺️ Session Example
json

{
  "timeframe": "DAWN_TO_DUSK",
  "place": {
    "label": "Avenue Montaigne",
    "type": "AVENUE",
    "gps": { "lat": 48.866, "lng": 2.304 },
    "address": {
      "line1": "22 Avenue Montaigne",
      "city": "Paris",
      "postal_code": "75008",
      "country": "FR"
    },
    "apartment": "C5",
    "floor": "2",
    "transportation": ["Metro M1 Franklin D. Roosevelt"]
  },
  "content": "Rumor has it the gallery owner is secretly dating the
florist next door. 🌸🤫",
  "profile": {
    "type": "FAKE",
    "alias": "MidnightWhisper"
  },
  "publish": {
    "linkedin_uuid": null,
    "facebook_uuid": null
  }
}

🔐 Authentication Flow
Step Description
Bash login Email/password or magic link
Social upgrade OAuth with Google, Facebook, etc.
UUID binding Link LinkedIn/Facebook UUIDs
Anonymous mode Create fake profile with alias
Privacy control Choose visibility per session
🧃 Gossip Mode

   -

   *Alias creation*: Choose a pseudonym (e.g., “BoulevardBabe” or
   “GemSnitch”)
   -

   *No UUID binding*: Posts are detached from real identity
   -

   *Visibility*: Gossip posts default to “Public” or “Friends-only”
   -

   *Moderation*: Optional filters for sensitive content

🛤️ From Boulevard to Natural Gem

Users can trace a path from urban spaces to nature by tagging sessions with
place types. This creates a narrative arc — a digital journey through time,
space, and secrets.
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

Want help building the fake profile system or moderation logic? I can
sketch out the schema or write the API
