# بيتك أنظف — Saudi Cleaning Brush Landing Page V2

## Current
- DTC-style landing page structure inspired by modern product pages: hero, clear price/offer, benefits, how it works, usage shots, review section, FAQ, and one-step order flow.
- Price: 80 SAR, crossed-out original 100 SAR.
- Free shipping inside Saudi Arabia.
- Max quantity: 3 pieces per order.
- Required: full name, Saudi phone, city, district, building number, detailed address.
- Optional browser geolocation sends latitude/longitude with the order.
- Formspree endpoint: https://formspree.io/f/xjykgvyo
- Success redirect: /thank-you.html
- Favicon included in PNG + SVG.
- Supabase intentionally not connected yet.

## Saudi cities
The city field loads a public bilingual Saudi geography dataset at runtime. The referenced dataset contains 4,581 cities/places across 13 regions and states that it uses reference IDs aligned with Saudi National Address data.

Source:
https://github.com/homaily/Saudi-Arabia-Regions-Cities-and-Districts

A smaller fallback list is included so the form is still usable when the remote dataset is unavailable.

## Reviews / Supabase
The page has a review section reserved for the next step. The eventual Supabase flow should support:
- rating
- text
- image
- voice/audio
- approval
- timestamp

No Supabase credentials are included in this version.

## Deployment
Static site. Push this folder to GitHub and deploy on Vercel. No build command required.

## Note
The current maximum-3 rule is enforced per submitted order. A strict cross-order limit of 3 units per customer/phone number requires server-side storage and validation, which can be added in the Supabase step.
