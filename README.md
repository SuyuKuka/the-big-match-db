# The Big Match Database

## About

The Big Match Database is a comprehensive relational database project developed as a third-year Bachelor's (L3) project at Université Paris Cité. Built entirely from scratch, this project implements a modern matchmaking, event organization, and social interaction platform. 

The system features a robust normalized relational architecture handling complex user profiles, multi-criteria filtering, geolocation, tiered subscriptions (Silver, Gold, Diamond), swipe-like mechanics (`LIKE`, `NOPE`, `EN_ATTENTE`) with mutual match detection, automated chat creation, and event management.

*Note: The codebase and SQL scripts emphasize strict relational integrity, database constraints, and clear schema organization. As this was an academic project, the codebase and docs are primarily in French*

## Tech Stack

- **Language / System:** SQL / Relational DBMS
- **Modeling:** Entity-Relationship Model (ER Model)
- **Architecture:** Normalized relational model with database and application-level constraints

## Key Features

- **Profile & Subscription Management:** Tracking of personal attributes, geographic data, physical criteria, sexual orientation, and tiered subscriptions.
- **Matchmaking Engine:** Management of swipe-style interactions (`LIKE`, `NOPE`, `EN_ATTENTE`) and mutual matches.
- **Chat and Messaging System:** Automatic creation of a unique conversation between two matched users and secure messaging.
- **Event and Venue Management:** Event creation, pricing, status tracking (`TERMINE`, `EN_COURS`, `FUTUR`), venue association, and user participation.
- **Multimedia & Leisure Integration:** Specialized relations for music streaming habits (`Spotify`), video streaming ratings (`Netflix`), and genre categorization.
- **Rigorous Integrity Constraints:** Strict validation of ages (minimum 18 years), date ranges, unique usernames, and business management rules.

## Project Structure

```text
📁 the-big-match-db
│
├── 📁 docs
│   ├── 🖼️ ER_diagram.png           # Entity-Relationship diagram
│   ├── 📄 Rapport.pdf              # Database architecture report
│   └── 🖼️ RELATIONNEL.png          # Relational schema diagram
|
├── 📁 src/                         # SQL scripts & source files
│   ├── 📁 data/                    # Data sources and input assets
│   ├── create.sql                  # Database creation and table schemas (DDL)
│   ├── insert.sql                  # Initial data insertion / seed script (DML)
│   └── select.sql                  # Queries, views, and data retrieval scripts
│
├── 📄 LICENSE                      # Project license
└── 📄 README.md                    # Project documentation
```

## Getting Started

### Prerequisites

- A compatible relational DBMS (PostgreSQL, MySQL, etc.)

### Installation

1. **Clone the repository:**
```bash
git clone [https://github.com/your-username/the-big-match-db.git](https://github.com/your-username/the-big-match-db.git)
cd the-big-match-db/src
```

2. **Connect to your PostgreSQL session:**
* If it's your first time launching and the database doesn't exist yet:
```bash
psql -U username
```
* Otherwise, connect directly to the database:
```bash
psql -U username -d chen_chiv
```

3. **Execute SQL scripts:**
```sql
\pset pager off
\i create.sql
\i insert.sql
\i select.sql
```

4. **Cleaning:**  
* Disconnect from chen_chiv and connect to the default postgres database:
```bash
psql -U username -d postgres
```

* Drop the database:
```SQL
DROP DATABASE chen_chiv;
```

*(Or simply run `dropdb -U username chen_chiv` from your terminal)*

## Team

This project was developed collaboratively as 5-person team:

- **CHEN Michel** - SQL Development & Database Architecture
  [![GitHub](https://img.shields.io/badge/GitHub-Profile-181717?logo=github)](https://github.com/SuyuKuka)
  [![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-0A66C2?logo=linkedin)](https://linkedin.com/in/chen-michel)

- **CHIV Henri** - SQL Development & Database Architecture
  [![GitHub](https://img.shields.io/badge/GitHub-Profile-181717?logo=github)](https://github.com/H-flamme)

## License

This project is licensed under the MIT License — see [LICENSE](LICENSE) for details.