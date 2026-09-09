# pixar-box-office-analysis
Power BI dashboard analyzing Pixar's budget vs. box office, awards, and sequel performance

# Pixar Box Office & Awards Analysis

A $200M budget doesn't guarantee a billion-dollar movie. Some of Pixar's most expensive films made a fraction of what cheaper ones pulled in.

This project analyzes Pixar's full filmography (*Toy Story*, 1995 → *Inside Out 2*, 2024) to answer:
- Do bigger budgets mean bigger box office?
- Do award winners actually rate best with critics?
- How do sequels stack up against the originals?

## Dashboard



![Power BI Dashboard](images/Power%20BI%20Dashboard.png)



*Full interactive version available by opening the `.pbix` file in [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free) — filters and cross-highlighting are fully functional.*

### Excel Prototype



![Excel Dashboard](images/Excel%20Dashboard.png)




![Excel Dashboard - first half](images/First%20half%20of%20Excel%20Dashboard.jpg)




![Excel Dashboard - second half](images/Second%20Half%20of%20Excel%20Dashboard.jpg)



## Data

Six linked tables — films, box office, Academy Awards, genre, people, and critic/public response — sourced via [Maven Analytics](https://mavenanalytics.io). Only a subset of fields made it into the final visuals.

Raw dataset: [`data/pixar-films-raw.zip`](data/pixar-films-raw.zip)

## Process

1. Prototyped all four charts as Excel pivot tables before building anything in Power BI — see [`excel/pixar-pivot-analysis.xlsx`](excel/pixar-pivot-analysis.xlsx)
2. Rebuilt the logic in Power BI:
   - Top-N filters (top 10 films by worldwide box office; top award-winners filtered to "Won" / "Won Special Achievement" only, excluding nominations)
   - A native Power BI field-grouping to pair sequels with their originals, without a manual mapping table
   - A genre-category filter to avoid double-counting a table that mixed genre and subgenre rows
3. Result: a 4-visual dashboard covering budget vs. box office, awards vs. Rotten Tomatoes score, sequel performance, and genre trends over time

Power BI file: [`powerbi/Pixar.pbix`](powerbi/Pixar.pbix)

## Key Findings

- Budget and box office aren't tightly linked — several $175–200M films landed anywhere from ~$630M to ~$1.7B worldwide
- Award-winning films cluster in a narrow, high critic-score band (79–99 on Rotten Tomatoes)
- Franchises like Toy Story and Inside Out show just how differently sequels can perform vs. their originals

## Tools

Excel · Power BI

---
Dataset via Maven Analytics.
