# Manhattan Vacation Rentals-Investment Analysis Airbnb


**Project Background:** A client evaluating the Manhattan short-term rental market requested guidance on which property types and neighnborhoods to prioritize for investment.
Analysis focused on attractiveness  through rental frequency via reviews and revenue potential using Airbnb listings and 30-day calendar data. The outcome informs property 
selection, sizing, and pricing for the next investment cycle.

**Data Structure Overview:**

- **Data Model:**  Two primary tables with a one-to-many relationship
  - listings (id, neighborhood, bedrooms, number of reviews, etc.)
  - calendar (date, listing_id, available, adjusted_price, etc.)
- **Cleaning & Engineered Fields**:
  - neighborhood_clean -standardized neighborhood names 
  - bedrooms_clean -empty cells treated as 0 (studios)
  - revenue_earned (calendar) -adjusted price when available = "f", else 0
  - revenue_earned (listings) -30-day SUMIF of calendar revenue_earned
  - top_listing -1 if listing is in a top 10 neighborhood and matches neighborhood's most popular bd size; otherwise 0
- **Analysis Tools:** Pivot tables, bar chart of top 10 neighborhoods by reviews

**Executive Summary:** 

- Lower East Side, Hell's Kitchen, and Harlem ranked among the top neighborhoods by review volume.
- Manhattan's Popular size bedroom in order: 1 BR, 2 BR, and studios, with Harlem renter's choosing 1 BR by demand and Midtown leaning towards studios
- Revenue analysis of the 30-day window showed Listing ID 49946551 as the top earner at $29,940; $359K annual estimate (not adjusted by season)
- **These results indicate that concentrating on the leading neighborhoods with their preferred unit size offers the strongest balance of
occupancy and revenue potential.

**Recommendations:**

- Prioritize acquisition in these neighborhoods where review activity and rental is high: Lower East Side, Hell's Kitchen, and Harlem
- Purchase 1 BR units in top neighborhoods and studios in Midtown
- Use the revenue_earned benchmark to set pricing; top listings must use a dynamic pricing strategy tied to observed booking frequency
- Allocate capital toward 1 BR units first, then supplement with 2 BR units where demand supports higher ADRs (average daily rate), and put a 
limit on studio outside Midtown
- **Refresh the 30-day revenue rollup monthly; monitor shifts and changes in rankings and bedroom popularity
  

<img width="663" height="709" alt="image" src="https://github.com/user-attachments/assets/1f34b809-81f5-4593-bd92-a975a0ce2c4a" />
<img width="663" height="255" alt="image" src="https://github.com/user-attachments/assets/9330d004-84d2-4708-b1f7-a2976c156edf" />





