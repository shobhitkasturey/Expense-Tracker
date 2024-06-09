# Expense Tracker

## Overview

This project provides a simple expense tracking tool using a MySQL database. Users can add expenses, view expense reports, and manage their expenses efficiently.

## Features

1. **Add Expense**: Record a new expense with amount, category, and description.
2. **View Expense Report**: Display all recorded expenses.

## Prerequisites

- Python 3.x
- MySQL Server
- MySQL Connector for Python

## Installation

1. **Clone the repository** or download the source code.

2. **Install the required packages** using pip:

    ```sh
    pip install mysql-connector-python
    ```

3. **Set up the MySQL database**:
   
   - Create a MySQL database named `expense`.
   - Ensure you have a MySQL user with the appropriate privileges.

## Usage

### Setting Up the Database Connection

The `ExpenseTracker` class requires database connection parameters (host, user, password, and database name) to connect to the MySQL server. Ensure the credentials provided in the `main` function are correct:

```python
host = "127.0.0.1"
user = "root"
password = "yourpassword"
database = "expense"
```

### Running the Application

To use the expense tracker, run the `main` function:

```sh
python main.py
```

This will present the following options:

1. **Add Expense**: Prompt for amount, category, and description to log a new expense.
2. **View Expense Report**: Display all recorded expenses.
3. **Exit**: Exit the application.

## File Descriptions

- `main.py`: Contains the main program logic for the expense tracker.
- `ExpenseTracker` class:
  - **__init__**: Initializes the database connection and creates the expenses table if it doesn't exist.
  - **create_table**: Creates the expenses table in the database.
  - **add_expense**: Adds a new expense record to the database.
  - **view_expense_report**: Retrieves and displays all expenses from the database.

## Example

1. **Add Expense**:

    Run the main program:

    ```sh
    python main.py
    ```

    Choose option 1 to add an expense:

    ```
    Enter your choice: 1
    Enter the amount: 50.75
    Enter the category: Food
    Enter the description: Lunch
    Expense added successfully!
    ```

2. **View Expense Report**:

    Choose option 2 to view the expense report:

    ```
    Enter your choice: 2
    Expense Report:
    ID: 1
    Amount: 50.75
    Category: Food
    Description: Lunch
    --------------------
    ```

## Notes

- Ensure the MySQL server is running and accessible with the provided credentials.
- Modify the database connection parameters in the `main` function as needed.
- The table `expenses` will be created automatically if it does not exist.

