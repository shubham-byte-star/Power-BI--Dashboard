 🏅 Olympic Games Analysis — Power BI Dashboard

An interactive Power BI dashboard analyzing over a century of Olympic Games data (Summer & Winter, 1896–2020s), covering participation trends, medal distribution, host cities, and country/sport-level breakdowns.

 📊 Dashboard Overview

The report consists of 4 pages:

 1. Olympic Games Analysis (Overview)
- KPI cards for Summer and Winter Games editions held
- Distribution of Games by decade (treemap, color-graded by frequency)
- Most times held host cities (Athens, London, Innsbruck, and more)

 2. Sports & Participation Trends
- Total sports, total events, and total host cities at a glance
- Distribution of Games by season across decades
- Interactive toggle: Evolution of Participation vs. No. of Events over time
- Top events by number of editions held (Athletics, Fencing, Gymnastics)

 3. Participants & Medals
- Male vs. female participation totals
- Medal count trend across Olympic history (1896–present)
- Top countries by number of participants, with a toggle for age distribution
- Gender split of event participation (donut chart)

 4. Medals & Regional Breakdown
- Distribution of medals by sport
- Distribution of medals by country
- Top countries by gold medal count
- Total participants by country

 🛠️ Tools & Techniques Used

- Power BI Desktop — data modeling, DAX measures, and report design
- DAX — custom measures for distinct game editions, medal counts, and season-based aggregations, e.g.:
  dax
  Summer_games_editions = 
  CALCULATE(
      DISTINCTCOUNT(consolidated_fact[games_year]),
      consolidated_fact[games_season] = "Summer"
  )
  
- Data visualization best practices — replaced a multi-slice pie chart with a treemap for better readability, applied a blue gradient color scale for visual consistency, and consolidated a unified color theme across all report pages
- Interactive elements — bookmark-based toggle buttons for switching between related visuals (e.g., Evolution of Participation vs. No. of Events)

 📈 Key Insights

- Summer Olympics have been held 3 more editions than Winter Olympics historically, with cancellations in 1916, 1940, and 1944 due to World Wars
- The USA leads all countries in both total participants and gold medals won
- Male participation has historically outpaced female participation, though the gap has narrowed significantly in recent decades
- Athletics events account for the highest share of medals awarded across all Olympic history

 🚀 What I'd Improve Next

- Aggregate country-level medal and participation data into continent/region-level views for higher-level comparisons
- Add a Top-N filter with an "Other" bucket on the country-heavy bar charts to reduce visual clutter
- Extend the treemap to break out Summer vs. Winter within each decade for a more granular view

 👤 Author

Shubham Vedivelli
BBA Graduate, KL University, Hyderabad
Skills: Power BI · Advanced Excel · SQL Server · Data Analysis · Dashboard Design
