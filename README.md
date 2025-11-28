**ATM Management System**

**Python (CSV-Based CLI Application)**

**ATM Management System – Command-Line Python Application**

**Overview of the Project**

This project is a command-line ATM simulator built in Python. It allows users to perform essential banking transactions such as cash withdrawal, cash deposit, PIN change, and profile viewing.
The system uses CSV (Comma Separated Values) files for persistent storage, meaning all account updates—balance changes, PIN updates—are saved permanently and reflected in future sessions.
The purpose of the project is to demonstrate:

**A. Python file handling**

**B. Data persistence**

**C. Input validation**

**D. Modular programming with functions**

**E. Error-handling and user interaction**

**Features:**

**1. Cash Withdrawal**
   
    A. Requires valid Account ID and PIN
    B. Checks for sufficient balance
    C. Deducts the requested amount
    D. Updates balance in dataset.csv
    
**2. Cash Deposit**
   
    A. Accepts only positive numeric values
    B. Updates account balance immediately
    C. Saves changes to CSV in real-time
   
   
**3. PIN Change**

    A. Ensures new PIN is exactly 4 digits
    B. Updates account’s PIN
    C. Saves securely in CSV
   
**4. Account Profile**

    A. Displays Name, Account Number, PIN, and Balance
    B. Access protected by PIN validation
   
**5. Input Validation**

    A. Handles non-numeric service input
    B. Rejects invalid or negative amounts
    C. Validates PIN format
    D. Detects missing/incorrect account IDs

**Security & Validation**

To ensure safe and reliable usage, the system includes:

    Account ID verification
  
    PIN authentication for sensitive actions
  
    Insufficient balance check during withdrawals
  
    Positive numeric validation for deposit/withdrawal
  
    Strict 4-digit format check for PIN changes
  
    Error-handling for invalid input, unrecognized accounts, or corrupted data files
  
**These validations prevent accidental errors and unauthorized access.**

**Technologies / Tools Used**

  **Language:**
  
        Python 3.x
  
  **Libraries:**
  
    csv → for reading/writing account data
    sys → for controlled program exits
  **Data Storage:**
  
    dataset.csv file storing:
      ACC_ID
      NAME
      ACC_NUMBER
      PIN
      BALANCE
  No external dependencies are required.

**Steps to Install & Run the Project**
  1. Install Python
    Make sure Python 3.x is installed:

  3. Prepare the Accounts CSV File
     
     Create a file named dataset.csv in the same folder as your script.
    
      Use this structure:
     
            [ACC_ID 	NAME	 ACC_NUMBER	 PIN	  BALANCE]
            [1001  	 KARAN       10196	1204	 56880.00]
        You may add or modify entries as needed.
  4. Save the Python File
     Save your ATM program as:

         atm.py
  5. Run the Program
     
     Navigate to the folder and execute:
     
          python atm.py

**Instructions for Testing**

When the script runs, you will see:

Welcome to our ATM

1.Cash Withdrawal

2.Change PIN
   
3.Account Profile
 
4.Cash Deposit

Steps to Test: 

    1.Choose a service (1–4)
    2.Enter a valid Account ID (e.g., 1001)
    3.Enter PIN (required for Withdrawal & Profile Check)
    4.Follow the on-screen instructions to complete the transaction
Sample Testing Accounts

    ACC_ID  NAME     ACC_NUMBER	            PIN	          BALANCE
  
    1001   	KARAN	  10196                 1204	      56880.00
    1002   	RAM	      19567                 1946	      28400.00
    1003    ANMOL     78546                 1256          17000.00

Screenshots
Below are example screenshots from the ATM CLI:

1.Cash Withdrawal

![WhatsApp Image 2025-11-28 at 12 06 11_e91b3d90](https://github.com/user-attachments/assets/7db9b138-4724-4029-ad09-6298a3041544)

 

2. Change PIN

 ![WhatsApp Image 2025-11-28 at 12 06 11_ca14c785](https://github.com/user-attachments/assets/236b51a0-8820-43c2-afd1-d7330e5824fb)

 

4. Account Profile

![WhatsApp Image 2025-11-28 at 12 06 11_618002f1](https://github.com/user-attachments/assets/56b9df53-6372-41f3-98dd-57b216953b7f)

 

6. Cash Deposit

![WhatsApp Image 2025-11-28 at 12 06 10_916f8b70](https://github.com/user-attachments/assets/734707c1-8975-4c78-946f-5bf295363fc7)

 
  
**Persistent Data Storage**

Every update made through the ATM (withdrawal, deposit, PIN change) is immediately written back to dataset.csv

This ensures:

    A.No data loss

    B.Real-time account updates

    C.Reliable behaviour over multiple runs

**Future Enhancements** 

You may extend the project by adding:

    A.Transaction history logs

    B.Admin dashboard

    C.Account creation/deletion

    D.GUI interface (Tkinter/PyQt)

    E.Encryption for PIN storage

**Conclusion**

This ATM Management System provides a complete demonstration of:

    A.Python file handling

    B.Data validation

    C.Modular program design

    D.Safe user authentication

    E.Persistent storage using CSV files
    
**NOTE: ** To run the program make sure that dataset.py file is executed first.

It is ideal for academic projects, demonstrations, and learning exercises involving Python fundamentals.

