
# Project Statement: The Python ATM Simulator

# The Core Problem: Making Data Stick

Every time you use a real bank or ATM, you expect your money to be exactly where you left it. The core challenge this project addresses is: **How do we make financial changes permanent in a simple computer program?**

We needed a realistic, yet easy-to-understand, training ground to demonstrate key concepts:
* **Persistent Data Management:** Ensuring changes to a user's balance or PIN **survive** when the program closes and reopens.
* **User Authentication:** Implementing a basic security gate (Account ID and PIN) for sensitive actions.
* **Transaction Processing:** Handling the logic for depositing and withdrawing funds accurately.

Our solution tackles this by using a standard **CSV file** as the "bank database," proving that persistent data can be managed effectively using only Python's built-in tools.

# Project Scope: What Can It Do?

Our primary goal was to build a fully functional, command-line ATM experience driven by a local CSV file.

# High-Level Features

* **Secure Authentication:** Checks the Account ID and PIN for all sensitive operations.
* **Core Transactions:** Seamlessly handle **Cash Withdrawal**, **Cash Deposit**, and **PIN Updates**.
* **Account Profile Check:** Instantly view the current balance and account details.
* **Data Persistence:** This is critical! Account data is **loaded** at startup and **saved back** to the file after every successful transaction, guaranteeing permanence.
* **Safety Checks:** Includes validation for inputs (ensuring they are positive numbers) and an **Insufficient Balance** check during withdrawals.

# Current Limitations (What's Out of Scope for Now)

To keep the project simple and focused on persistence, we deliberately excluded more complex features:
* **Security Beyond Basics:** PINs and balances are not hashed or encrypted.
* **Advanced System Handling:** No logic for handling multiple users accessing the file at the same time (concurrent access).
* **Fancy Interface:** This is a command-line application only; there is no Graphic User Interface (GUI).
* **New Accounts:** You can only use the accounts that are pre-loaded in the CSV file.

# Target Users

This project is primarily designed for:

* **Beginner to Intermediate Python Developers:** Anyone learning about file I/O, error handling (`try/except`), and data structure manipulation (lists of dictionaries).
* **Students of Computer Science:** Those needing a clear, practical example of how to implement **persistent state** in an application using standard libraries.
* **Code Reviewers & Instructors:** A simple, well-modularized codebase to easily demonstrate concepts like data loading/saving logic and separation of concerns.

# Design Philosophy: Simple and Structured

We structured the code with maintainability and clarity in mind:

# The Database: CSV + List of Dictionaries

We chose the **CSV file (`dataset.csv`)** for its simplicity—it's easy for anyone to open and read. Inside the program, we use a **list of dictionaries** because it gives us the best of both worlds:
1.  **Easy Searching:** The list structure lets us loop through and find a specific account.
2.  **Clear Data Access:** Dictionaries allow us to access account fields using clear names like `account['BALANCE']` or `account['PIN']`.

# Transaction Flow

All our key functions (`withdraw`, `deposit`, `change_pin`) follow a predictable and reliable pattern:

1.  **Convert & Calculate:** Convert the stored string data (balance/PIN) into the correct format (float for math, integer for PIN check).
2.  **Execute Logic:** Perform the math or update the value.
3.  **Format & Save:** Convert the new value back into a clean string (like `123.45`) and immediately call the `save_data()` function to **write the entire updated dataset back to the CSV file.**

This standardized flow is the core mechanism that ensures our application state is always persistent!
