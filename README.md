# Zillow Scraper

Zillow Scraper gets you 🎯 accurate, 🔍 detailed Zillow data as clean JSON in **Real-Time**.

No selectors, no proxies, no data cleaning. Just the data.

[**Try it now in the playground**](https://www.omkar.cloud/tools/zillow-scraper/playground) - See the data quality for yourself in one click, **No sign-up required**.

**Build on it free:** 1,000 calls every month, no credit card ❤️

## What can I get

- 🏠 **Full details on 110M+ US homes** — Zestimate, price & tax history, schools, photos, agent phone
- 🔍 **Search for-sale, for-rent & sold homes** — by city, ZIP, coordinates or URL; filter & sort
- 📈 **Valuation context** — Zestimate history charts, comparable homes, nearby homes, Walk Score
- 🧑‍💼 **Agent directory** — search agents by city; full profiles with email, phones, licenses & reviews

## Why Zillow Scraper

Most other Zillow APIs fail you in one of four ways:

- 🗄️ **Inaccurate, cached, stale data**
- 🧩 **Low-detail endpoints** — a few fields per call, never the full picture
- 💸 **Pay more to get the same data**
- 🪦 **Works today, breaks next month** — nobody maintains it

Zillow Scraper is scraped live on every call, priced honestly, and actively maintained.

## Example: A Full Zillow Property

```json
{
  "zpid": "20521904",
  "status": "FOR_SALE",
  "home_type": "SINGLE_FAMILY",
  "address": { "street": "927 N Whittier Dr", "city": "Beverly Hills", "state": "CA", "zipcode": "90210", "county": "Los Angeles County" },
  "latitude": 34.07979,
  "longitude": -118.421936,
  "price": 35995000,
  "currency": "USD",
  "zestimate": 32742200,
  "rent_zestimate": 50671,
  "tax_rate": 1.18,
  "last_sold_price": 8800000,
  "date_sold": "2020-07-01",
  "bedrooms": 9,
  "bathrooms": 10,
  "living_area": 13000,
  "living_area_units": "sqft",
  "lot_size": 0.5767,
  "lot_size_units": "Acres",
  "year_built": 2025,
  "days_on_zillow": 57,
  "page_view_count": 4238,
  "favorite_count": 196,
  "description": "Nestled in one of Beverly Hills' most prestigious enclaves, on just over half an acre, this breathtaking modern estate seamlessly blends timeless elegance with contemporary luxury. The striking white facade, framed by lush greenery and mature trees, sets the stage for an exceptional living experience...",
  "listing_type": { "is_for_sale_by_agent": true, "is_new_construction": false, "is_foreclosure": false, "is_pending": false },
  "facts": {
    "appliances": ["Barbeque", "Dishwasher", "Dryer", "Washer", "Refrigerator"],
    "architectural_style": "Modern",
    "cooling": ["Central Air"],
    "heating": ["Central"],
    "flooring": ["Wood", "Stone", "Marble"],
    "has_garage": true,
    "garage_spaces": 4,
    "stories": 2,
    "price_per_sqft": 2769
  },
  "agent": {
    "agent_name": "Branden Williams",
    "agent_phone": "310-776-0737",
    "agent_license": "DRE # 01774287",
    "broker_name": "The Beverly Hills Estates",
    "broker_phone": "310-626-4248",
    "mls_id": "26854793",
    "mls_name": "CLAW"
  },
  "photos": [
    "https://photos.zillowstatic.com/fp/fc1d1f30edfc0cb06ac5cc1940423db6-uncropped_scaled_within_1536_1152.jpg",
    "https://photos.zillowstatic.com/fp/bb122c30d6a0cce496d813761f2cf768-uncropped_scaled_within_1536_1152.jpg"
  ],
  "photo_count": 55,
  "price_history": [
    { "date": "2026-07-02", "event": "Listed for sale", "price": 35995000, "price_per_sqft": 2769, "source": "CLAW" },
    { "date": "2025-03-24", "event": "Listed for sale", "price": 37500000, "price_per_sqft": 2885, "source": "CLAW" }
  ],
  "tax_history": [
    { "date": "2025-08-29", "tax_paid": 115084.16, "assessed_value": 9525402 },
    { "date": "2024-08-29", "tax_paid": 112577.08, "assessed_value": 9338630 }
  ],
  "schools": [
    { "name": "El Rodeo Elementary School", "rating": 10, "grades": "K-5", "distance": 0.9 },
    { "name": "Beverly Hills High School", "rating": 9, "grades": "9-12", "distance": 1.4 }
  ],
  "nearby_neighborhoods": [
    { "name": "Beverly Hills Gateway", "link": "https://www.zillow.com/beverly-hills-gateway-beverly-hills-ca/" }
  ],
  "link": "https://www.zillow.com/homedetails/927-N-Whittier-Dr-Beverly-Hills-CA-90210/20521904_zpid/"
}
```

*Trimmed for readability.*

## Get Started with 1,000 Free Calls

Start in the [playground](https://www.omkar.cloud/tools/zillow-scraper/playground) — try any endpoint with one click, no sign-up required.

Once you're happy with the data, start with the free plan for 1,000 free calls every month:

1. [Sign up on Omkar Cloud](https://www.omkar.cloud/auth/sign-up?redirect=/tools/zillow-scraper/playground) — free, no credit card.
2. Open the [Zillow Scraper playground](https://www.omkar.cloud/tools/zillow-scraper/playground) and enter any city or address you like. Click **Get Live Data**.
3. Enjoy your data 😎.

## Endpoints

13 endpoints cover everything you need.

| Endpoint | Path | Returns |
|---|---|---|
| Location Autocomplete | `/locations/auto-complete` | Turns any city, ZIP or address into a region id or zpid |
| Search For Sale / Rent / Sold | `/properties/search-sale`, `/properties/search-rent`, `/properties/search-sold` | ~40 listings per page; filter by price, beds, baths, sqft, home type; sortable |
| Search By Coordinates | `/properties/search-coordinates` | Listings within N miles of a lat/lng point |
| Search By URL | `/properties/search-url` | Paste any zillow.com search URL, keep its filters |
| Property Details | `/properties/detail` | Everything about one home in a single call |
| Property Value History | `/properties/value-history` | Zestimate, rent and tax charts over 1, 5 or 10 years |
| Comparable Homes | `/properties/comps` | Zillow's own comps for a home |
| Nearby Homes | `/properties/nearby` | Homes around a listing with price and coordinates |
| Walk, Transit & Bike Score | `/properties/walk-transit-score` | All three scores with descriptions |
| Search Agents | `/agents/search` | Agents covering a city, with reviews and sales stats |
| Agent Details | `/agents/detail` | Email, phones, licenses, service areas, reviews, listings and sales |

## Pricing

High value, Low price.

| Plan | Price | Calls / month | Per 1,000 |
|---|---|---|---|
| **Free** | **Free** | **1,000** — the most generous free plan | $0 |
| **Starter** | $16/mo | 20,000 | $0.80 |
| **Grow** | $48/mo | 100,000 | $0.48 |
| **Scale** | $148/mo | 400,000 | $0.37 |

Need a bigger plan? Ask on [WhatsApp](https://api.whatsapp.com/send?phone=918178804274&text=I%20need%20a%20custom%20plan%20for%20the%20Zillow%20Scraper%20API.) or [Email](mailto:happy.to.help@omkar.cloud?subject=Custom%20plan%20for%20Zillow%20Scraper%20API&body=I%20need%20a%20custom%20plan%20for%20the%20Zillow%20Scraper%20API.).

👉 [Start with Free Plan](https://www.omkar.cloud/auth/sign-up?redirect=/tools/zillow-scraper/playground) — 1,000 free calls/month

## 💬 Have Questions? We Have Answers.

You're a developer — we know how hard completing a project can be. So we offer full support: just message us and we'll reply ✅ with a solution within 1 working day.

[![Message Us on WhatsApp about Zillow Scraper](https://raw.githubusercontent.com/omkarcloud/assets/master/images/whatsapp-us.png)](https://api.whatsapp.com/send?phone=918178804274&text=I%20need%20help%20using%20the%20Zillow%20Scraper%20API.)

[![Ask Us by Email about Zillow Scraper](https://raw.githubusercontent.com/omkarcloud/assets/master/images/ask-on-email.png)](mailto:happy.to.help@omkar.cloud?subject=Help%20with%20Zillow%20Scraper%20API&body=I%20need%20help%20using%20the%20Zillow%20Scraper%20API.)

## Popular Scrapers by Omkar Cloud

- **[Google Maps Scraper (3,100+ GitHub Stars)](https://github.com/omkarcloud/google-maps-scraper)** — type "realtors in Miami", get every business as a ready-to-call lead list: phones, emails, websites & reviews. Up to 100K free leads/month.
- [**Rightmove Scraper**](https://www.omkar.cloud/tools/rightmove-scraper) — UK homes for sale & to rent, sold prices & estate agents
- [**Zoopla Scraper**](https://www.omkar.cloud/tools/zoopla-scraper) — UK property search, details, house prices & agents
- [**Airbnb Scraper**](https://www.omkar.cloud/tools/airbnb-scraper) — Airbnb listings: prices, ratings, amenities & hosts
- [**Booking Scraper**](https://www.omkar.cloud/tools/booking-scraper) — Booking.com hotels: prices, ratings, rooms & amenities
- [**Website Email Contact Scraper**](https://www.omkar.cloud/tools/website-email-contact-scraper) — emails, phones & socials from any website

👉 [Start with Free Plan](https://www.omkar.cloud/auth/sign-up?redirect=/tools/zillow-scraper/playground) — 1,000 free calls/month
