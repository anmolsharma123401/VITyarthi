Python ATM Simulator: Your Command-Line Bank 

Welcome to the **Python ATM Simulator** This is a simple, yet robust command-line application designed to mimic the core functions of a real ATM, using a local **CSV file** for data storage.

Key Features

**Persistent Data Storage:** Your account details (ID, Name, PIN, and Balance) are safely stored in an `dataset.csv` file. Any changes—deposits, withdrawals, or PIN updates—are **immediately saved**, so your data is right where you left it for the next session.
  * **Essential ATM Services:**
      * **Cash Withdrawal:** Smartly deducts the amount after checking that you have enough funds.
      * **Cash Deposit:** Instantly increases your account balance.
      * **Change PIN:** Update your secure 4-digit PIN with ease.
      * **Account Profile:** Quick check of your current details and balance.
  * **Built-in Security & Validation:** We keep things safe and sound\!
    1.  **Strict Authentication:** Your Account ID and PIN are required for all sensitive transactions (Withdrawal, Profile Check).
    2.  **Insufficient Funds Check:** Prevents you from overdrawing your account.
    3.  **Input Integrity:** All money-related inputs are validated to ensure they are positive, numerical values.

 Component
**Language: ** **Python 3.x**
**Libraries Used: ** `csv` (Standard library for file handling) and `sys` (For controlled program exit) 
**Data Storage: **  **CSV File** (Simple, human-readable Comma Separated Values) 


Get Started

1. Setup

The initial run of the script handles the file setup for you—no manual work needed!

1.  **Save the Code:** Save the entire provided code block into a single file named **`atm_simulator.py`**.
2.  **First Run Magic:** The very first time you execute the file, it will **automatically create** the required **`dataset.csv`** file with sample data in the same directory.

2. Execution

Open your terminal or command prompt, navigate to the directory where you saved `atm_simulator.py`, and run the following command:

**python atm_simulator.py**

3.  Sample Account Data

Use the following details to jump right into testing the system:

['ACC_ID', 'NAME', 'ACC_NUMBER', 'PIN', 'BALANCE']
{'ACC_ID': '1001', 'NAME': 'KARAN', 'ACC_NUMBER': '10196', 'PIN': '1204', 'BALANCE': '56880.00'},


## How to Use

1.  **Main Menu:** Upon execution, the main menu will appear, asking you to select a service (1-4).
2.  **Enter Account ID:** Provide the Account ID you wish to use (e.g., `1001`).
3.  **PIN Validation:** If you select a service that requires security (like Withdrawal or Profile Check), you'll be prompted to enter your 4-digit PIN.
4.  **Complete Transaction:** Follow the prompts to finalize your action.
**SCREENSHOTS**
![WhatsApp Image 2025-11-23 at 15 09 30_1a05fd71](https://github.com/user-attachments/assets/0e6f10b7-0bf5-4aa6-835e-9aea3a9abfe5)
![WhatsApp Image 2025-11-23 at 15 10 12_11f51b82](https://github.com/user-attachments/assets/4d033cb0-926e-4a5b-abfe-46b75640ec2d)
![WhatsApp Image 2025-11-23 at 15 08 31_6c9405f7](https://github.com/user-attachments/assets/7a4836cd-58c0-4218-a15b-3864f1f741ef)
![WhatsApp Image 2025-11-23 at 15 10 52_fca85283](https://github.com/user-attachments/assets/db04ee54-8ad4-4e0a-9da4-f38f6e99d497)

**Remember:** Your financial actions are instantly saved\! Any changes to your **balance** or **PIN** are immediately written back to the `dataset.csv` file, preserving your progress for the next time you run the simulator.
