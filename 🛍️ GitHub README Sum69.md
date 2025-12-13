🛍️ GitHub README Summary – *Centro Commerciale Rails App*

*Purpose*: The app models a shopping center's infrastructure, showcasing
store layouts, features, and celebratory milestones.
🧩 Key Features

   -

   Dynamic HTML showcase for interactive views (e.g. “nest opening” design)
   -

   CSS styling field for customizing the visual presentation
   -

   Relational database for tracking shop types, tenants, and events
   -

   Anniversary modules for commemorative content (10, 20-year milestones)

🧱 Data Structure Overview🔹 First Table: showcases
Field Type Description
css_style String Custom CSS for visual layout
html_page Text HTML content for nest showcase
nest_opening Boolean/Text Flags or details for nest opening view
🔹 Second Table Group: Relational Shop Entities

These are used to model different stores and their types within the mall.
🏪 shops
Field Type Description
name String Name of the shop
type_id Integer Foreign key for shop type
opened_on Date Opening date
🗂️ shop_types
Field Type Description
category String Type of shop (e.g. fashion, tech)
description Text Extra info
🎉 anniversaries
Field Type Description
shop_id Integer Linked shop
year Integer Anniversary milestone (10, 20...)
message Text Celebratory message or event description
