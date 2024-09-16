# 🏏 Pakistan Super League (PSL) Database Project

Welcome to the **Pakistan Super League (PSL) Database Project**! 🎉 This project is designed to create a structured and comprehensive database for managing various aspects of the PSL, including teams, players, stadiums, matches, and statistics. It provides an efficient way to store, manage, and query information regarding PSL matches, teams, players, officials, and their respective statistics.

## 📚 Table of Contents
- [Introduction](#introduction)
- [Database Structure](#database-structure)
- [Schema Design](#schema-design)
  - [Teams Table](#teams-table)
  - [Players Table](#players-table)
  - [Matches Table](#matches-table)
  - [Stadiums Table](#stadiums-table)
  - [Seasons Table](#seasons-table)
  - [Officials Table](#officials-table)
  - [Teams Stats Table](#teams-stats-table)
  - [Players Stats Table](#players-stats-table)
- [Key Features](#key-features)
- [Usage](#usage)
- [Contributions](#contributions)
- [License](#license)

## 📥 Introduction

The **Pakistan Super League Database Project** is aimed at storing vital information about the PSL, such as team details, player information, match results, and season data, in a well-structured format. This project utilizes SQL to create tables that hold data regarding PSL’s history, teams, players, stadiums, and officials.

### 🎯 Key Objectives:
- Provide an efficient relational structure for PSL data.
- Enable querying and reporting on PSL statistics such as team performance, player stats, match outcomes, etc.
- Support future enhancements for analytics and data visualization.

## 🏗️ Database Structure

The database structure is designed using **relational tables** to store and manage the various entities of the PSL. Relationships between teams, players, matches, and stadiums are established using **foreign keys** to ensure data integrity.

### ⚙️ Schema Design

Here is a brief description of the schema design and the tables used in this project.

### 🏏 Teams Table
The `Teams` table contains information about the PSL teams, including the team name, city, coach, captain, number of titles won, and the year of foundation.

**Columns:**
- `team_id`: Unique identifier for each team.
- `team_name`: Name of the team.
- `city`: City where the team is based.
- `coach_name`: Name of the coach.
- `captain_name`: Name of the team captain.
- `title_won`: Number of PSL titles won.
- `founded_year`: Year the team was founded.

### 👥 Players Table
The `Players` table stores data about each player, including their name, nationality, playing position, and date of birth.

**Columns:**
- `player_id`: Unique identifier for each player.
- `player_name`: Name of the player.
- `nationality`: Player's nationality.
- `position`: Player's role (e.g., All-rounder, Bowler, Batsman).
- `date_of_birth`: Player's birth date.
- `team_id`: Foreign key referencing the team they belong to.

### 🏟️ Stadiums Table
The `Stadiums` table provides information about the various stadiums used for PSL matches.

**Columns:**
- `stadium_id`: Unique identifier for each stadium.
- `stadium_name`: Name of the stadium.
- `city`: City where the stadium is located.
- `capacity`: Seating capacity of the stadium.

### 📅 Seasons Table
The `Seasons` table stores the season information, including the start and end year of each PSL season.

**Columns:**
- `season_id`: Unique identifier for each season.
- `start_year`: Start year of the PSL season.
- `end_year`: End year of the PSL season.

### 🏏 Matches Table
The `Matches` table contains details about each PSL match, including the date, venue, result, winning and losing teams, and the stadium.

**Columns:**
- `match_id`: Unique identifier for each match.
- `date`: Date of the match.
- `venue`: Venue of the match.
- `result`: Outcome of the match.
- `winning_team_id`: Foreign key referencing the winning team.
- `losing_team_id`: Foreign key referencing the losing team.
- `stadium_id`: Foreign key referencing the stadium.
- `season_id`: Foreign key referencing the season.

### 🧑‍⚖️ Officials Table
The `Officials` table stores data about the match officials, including umpires and referees.

**Columns:**
- `official_id`: Unique identifier for each official.
- `official_name`: Name of the official.
- `role`: Role of the official (e.g., Umpire, Referee).
- `match_id`: Foreign key referencing the match they officiated.
- `nationality`: Official's nationality.

### 📊 Teams Stats Table
The `Teams_Stats` table tracks the performance of each team across seasons.

**Columns:**
- `team_stats_id`: Unique identifier for team stats.
- `team_id`: Foreign key referencing the team.
- `season_id`: Foreign key referencing the season.
- `wins`: Number of matches won by the team.
- `losses`: Number of matches lost.
- `points`: Total points earned by the team.

### 🏅 Players Stats Table
The `Players_Stats` table records the individual player performance for each season.

**Columns:**
- `player_stats_id`: Unique identifier for player stats.
- `player_id`: Foreign key referencing the player.
- `season_id`: Foreign key referencing the season.
- `runs`: Number of runs scored by the player.
- `wickets`: Number of wickets taken by the player.
- `catches`: Number of catches taken by the player.
- `runouts`: Number of runouts effected by the player.

## ✨ Key Features
- **Relational Database Design**: Ensures that teams, players, and matches are interconnected.
- **Comprehensive Data**: Information about teams, players, officials, stadiums, and matches for different PSL seasons.
- **Flexibility**: Can be easily extended with more tables, queries, and relationships for advanced PSL analytics.
- **Data Integrity**: Use of foreign keys ensures data consistency across tables.

## 🚀 Usage

1. **Create the Database**: Run the SQL script to set up the `pakistan_super_league` database.
2. **Insert Data**: Insert the sample PSL data into the respective tables.
3. **Query the Data**: Perform queries to extract insights, such as player stats, match results, and team performance.
4. **Analyze**: Use SQL queries to analyze team stats, player performances, and match outcomes.

## 🤝 Contributions

Contributions to this project are welcome! Feel free to fork the repository, submit issues, or create pull requests. Together we can make this database more detailed and powerful! 

## 📜 License

This project is licensed under the **MIT License**. You are free to use, modify, and distribute this project as long as you provide attribution.

---

💡 Feel free to reach out with any questions, suggestions, or improvements. Let’s keep the cricket spirit alive! 🏏✨
