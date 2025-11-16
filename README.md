# 🎬 StreamDB: A SQL Project for a Fictional Streaming Service

[![SQL](https://img.shields.io/badge/SQL-PostgreSQL-blue.svg)](https://www.postgresql.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A complete SQL project that models the backend database for a fictional movie and TV streaming service. This project demonstrates database schema design, data population, and complex analytical queries.

## 📊 Project Overview

StreamDB is designed to store and manage data for a streaming platform. It tracks users, their subscriptions, available movies, and detailed watch history, including user ratings. This structure allows for powerful business intelligence queries, such as identifying popular content, understanding user behavior, and generating personalized recommendations.

## 🚀 Features

-   **Relational Schema:** A well-normalized database with five core tables (`users`, `subscriptions`, `genres`, `movies`, `watch_history`).
-   **Sample Data:** Pre-populated with realistic data to make the project immediately runnable.
-   **Complex Queries:** A collection of SQL queries ranging from simple `JOIN`s to advanced analytics using Common Table Expressions (CTEs) and Window Functions.
-   **Performance Tuning:** Includes an `indexes.sql` file to demonstrate best practices for query optimization.
-   **Clear Documentation:** A detailed `README.md` explaining the project structure and setup.

## 📂 Database Schema

The database consists of the following tables:

| Table              | Description                                         |
| ------------------ | --------------------------------------------------- |
| `users`            | Stores information about registered users.          |
| `subscriptions`    | Defines available subscription plans (e.g., Basic). |
| `user_subscriptions` | A linking table connecting users to their subscription history. |
| `genres`           | A lookup table for movie genres.                     |
| `movies`           | Contains details about each movie title.            |
| `watch_history`    | The core analytical table, tracking every view and rating. |

## 🛠️ Tech Stack

-   **Database:** PostgreSQL (compatible with MySQL with minor syntax changes)
-   **Language:** SQL

## 📋 Setup Instructions

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/stream-db-project.git
    cd stream-db-project
    ```

2.  **Set up your database:**
    -   Install PostgreSQL on your local machine.
    -   Create a new database: `CREATE DATABASE streamdb;`
    -   Connect to your new database using your preferred SQL client (like `psql`, DBeaver, or pgAdmin).

3.  **Run the SQL scripts in order:**
    -   Execute `sql/01_schema.sql` to create the tables.
    -   Execute `sql/02_data.sql` to populate the tables with sample data.
    -   (Optional) Execute `sql/04_indexes.sql` to add performance indexes.

4.  **Explore the data:**
    -   Open `sql/03_queries.sql` in your SQL client and run the queries to see the results!

## 🌟 Sample Query Highlights

-   **Find the top 5 most-watched movies:** Uses `GROUP BY` and `ORDER BY`.
-   **Calculate average movie ratings:** Uses `LEFT JOIN` and aggregate functions.
-   **Generate personalized recommendations:** A complex query using a CTE to suggest movies based on a user's viewing history.
-   **Rank movies by genre:** Uses a window function (`RANK()`) to create rankings within partitions.

## 🔮 Future Enhancements

-   Add a `series` table and a `series_episodes` table to model TV shows.
-   Create an `actors` table and a `movie_actors` linking table for many-to-many relationships.
-   Implement stored procedures for common tasks like user sign-up.
-   Add triggers to automatically update a `total_watches` count on the `movies` table.

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
