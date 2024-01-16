# Animal-Vehicle Collision Analysis

## Overview

This repository contains code for predicting the species involved in animal-vehicle collisions using machine learning techniques. The analysis includes loading data from a PostgreSQL database, training a species prediction model using scikit-learn, and visualizing collision regions on a geographical map.

## Requirements

Before running the code, make sure you have the following installed:

- PostgreSQL (for database setup)
- Python 3.x
- Required Python packages (install via `pip install -r requirements.txt`)

## Setup

### 1. PostgreSQL Database Setup

1. Create a PostgreSQL database and import the provided CSV data into relevant tables.

    ```sql
    -- Example SQL commands to create tables and import data
    CREATE TABLE collisions (
        month VARCHAR(9),
        year INTEGER,
        species VARCHAR(25),
        longitude FLOAT,
        latitude FLOAT
    );

    COPY collisions FROM '/path/to/collisions_data.csv' DELIMITER ',' CSV HEADER;
    ```

2. Update `db_params` in the Python code with your PostgreSQL database credentials.

### 2. Python Environment Setup

1. Create a virtual environment:

    ```bash
    python -m venv venv
    ```

2. Activate the virtual environment:

    - Windows: `venv\Scripts\activate`
    - Linux/Mac: `source venv/bin/activate`

3. Install required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. Run the species prediction script:

    ```bash
    python AlbertaWildlifeCollisionPredictionProgram.py
    ```




## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

