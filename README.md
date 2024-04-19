# Custom ELT Project

This repository contains a custom Extract, Load, Transform (ELT) project that utilizes Docker and PostgreSQL to demonstrate a simple ELT process. This project was created based on insights from the following tutorial video: [Database engineering for beginners](https://www.youtube.com/watch?v=PHsC_t0j1dU&t=599s).

## Repository Structure

- **docker-compose.yaml:** Configuration for Docker Compose, orchestrating multiple Docker containers:
  - **source_postgres:** Source PostgreSQL database.
  - **destination_postgres:** Destination PostgreSQL database.
  - **elt_script:** Service that runs the ELT script.

- **elt_script/Dockerfile:** Sets up a Python environment, installs the PostgreSQL client, and includes the ELT script as the default command.

- **elt_script/elt_script.py:** Python script for the ELT process. It waits for the source PostgreSQL database to become available, then dumps its data to a SQL file and loads this data into the destination PostgreSQL database.

- **source_db_init/init.sql:** SQL script initializing the source database with sample data. It creates tables for users, films, film categories, actors, and film actors, and inserts sample data into these tables.

## Usage

1. Clone this repository to your local machine.
2. Make sure you have Docker installed.
3. Navigate to the project directory.
4. Run `docker-compose up` to start the ELT process.

## Tutorial Video

For detailed guidance and insights into ELT processes, refer to the tutorial video: [Tutorial Video](https://www.youtube.com/watch?v=PHsC_t0j1dU&t=599s).

