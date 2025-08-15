# FIFA-World-Cup-Analysis
This project contains a PostgreSQL-based analysis of FIFA World Cup data from 2002 to 2018. The SQL queries analyze team performance metrics across five World Cup tournaments, answering key questions about participating countries, games played, wins, losses, goals scored, goals conceded, goal differences, and points earned.  

# FIFA World Cup Analysis

## Overview
This project contains a PostgreSQL-based analysis of FIFA World Cup data from 2002 to 2018. The SQL queries analyze team performance metrics across five World Cup tournaments, answering key questions about participating countries, games played, wins, losses, goals scored, goals conceded, goal differences, and points earned.

## Project Description
The `FIFA WORLD CUP ANALYSIS.sql` script uses PostgreSQL to query and aggregate data from five tables (`fifa_2002`, `fifa_2006`, `fifa_2010`, `fifa_2014`, `fifa_2018`), each representing team statistics for a specific World Cup year. The script employs `UNION ALL` to combine data across years and answers the following questions:

1. **Total Countries**: Counts the number of unique countries that participated in the World Cups from 2002 to 2018.
2. **Overall Statistics**: Calculates the total games played, wins, losses, goals scored, and goals conceded across all tournaments.
3. **Country Appearances**: Identifies the countries with the highest and lowest appearances (Note: The original query for this may need revision for accuracy).
4. **Games Played**: Determines the countries with the highest and lowest number of games played.
5. **Games Won**: Finds the countries with the highest (Brazil) and lowest (Serbia & Montenegro) number of wins.
6. **Games Lost**: Identifies the countries with the highest (Togo) and lowest (New Zealand) number of losses.
7. **Goals Scored**: Determines the countries with the highest (Germany) and lowest (Saudi Arabia) goals scored.
8. **Goals Conceded**: Finds the countries with the highest (Brazil) and lowest (Switzerland) goals conceded.
9. **Goal Difference**: Attempts to identify the countries with the highest and lowest goal differences (Note: The query references a non-existent `goal_differences` column, which may require correction to `goals_for - goals_against`).
10. **Points Earned**: Identifies the countries with the highest (Brazil) and lowest (Serbia & Montenegro) points.

## Files
- **FIFA WORLD CUP ANALYSIS.sql**: The main SQL script containing all queries for the analysis.

## Prerequisites
- **PostgreSQL**: Ensure a PostgreSQL database is set up with the necessary tables (`fifa_2002`, `fifa_2006`, `fifa_2010`, `fifa_2014`, `fifa_2018`) containing columns: `team`, `points`, `game_played`, `win`, `loss`, `goals_for`, and `goals_against`.

## Notes
- The query for Q3 (highest and lowest country appearances) may not accurately reflect appearances, as it uses `MAX(DISTINCT team)` and `MIN(DISTINCT team)`, which sorts teams alphabetically rather than by appearance count. Consider revising to use `COUNT` and `GROUP BY` for accurate results.
- The query for Q9 (goal difference) references a non-existent `goal_differences` column. Update the query to calculate `goals_for - goals_against` for accurate goal difference analysis.

## Contributing
Contributions are welcome! Please submit a pull request or open an issue to suggest improvements, such as query optimizations, additional analyses, or corrections to existing queries.
