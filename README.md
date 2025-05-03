# 🏏 IPL Excel Dashboard Project

This project is a comprehensive Excel-based dashboard that analyzes Indian Premier League (IPL) data using interactive pivot tables, slicers, and calculated KPIs.

## 📂 Project Contents

- `matches.csv`: Contains match-level data such as season, venue, teams, winner, toss, etc.
- `deliveries.csv`: Ball-by-ball data with detailed statistics on each delivery.
- `IPL_Dashboard.xlsx`: Main Excel dashboard with pivot tables, slicers, and visualizations.
- `README.md`: Documentation for understanding and reproducing the dashboard.
- "Match Analysis Snap" - Image file having my match analysis output
- "Team wise analysis snap" -Image file having team wise analysis output image

## 📊 Features

- Interactive **Season Slicer** to filter dashboards by year
- **Team-wise performance analysis**
- **Points Table** generation for each season
- Matchups using dynamic labels (e.g., `Team A VS Team B`)
- Calculated KPIs:
  - Total Matches
  - Wins by each team
  - Boundaries hit (using helper columns like `=IF(batsman_runs=4,1,0)`)
- Pivot Tables created from both `matches` and `deliveries` sheets
- Helper columns to manage complex logic (e.g., count only wickets, boundaries, or custom filters)

## 💡 Technical Details

- Built using **Microsoft Excel** (compatible with older versions with no slicer support workaround)
- Data cleaning and calculations performed using:
  - `VLOOKUP()` to connect deliveries with matches
  - `IF()` formulas for flags like boundaries, wickets
  - Custom columns for text combinations like `=CONCAT(Team1, " VS ", Team2)`
- PivotTables linked to the season slicer using a unified `Season` column with `VLOOKUP`

## 🛠️ Setup Instructions

1. Clone the repository or download the Excel and CSV files.
2. Open `IPL_Dashboard.xlsx`.
3. If slicers don’t work, ensure:
   - You’ve added data to the model for `Distinct Count`
   - PivotTables are refreshed after editing data
4. Modify formulas as needed for your Excel version.

## 📈 To-Do / Future Improvements

- Add Power BI version of the dashboard
- Automate CSV import and dashboard refresh using VBA
- Create season summary report using Power Query

## 🙋‍♂️ Contact

If you find a bug or want to contribute:
- Raise an issue or
- Connect via GitHub discussions
