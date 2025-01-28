# Basic Bank Management System in C

A simple console-based basic bank management system that allows users to create accounts, perform transactions, and manage their banking operations.

## Features

- **Account Creation**:  
  Users can create a new account by providing personal details, including:
  - First name, middle name, last name, and mother's name
  - Date of birth, IC/Passport number, email, and phone number
  - Username and password

- **User Authentication**:  
  Existing users can sign in using their username and password.

- **Transaction Operations**:  
  - **Check Balance**: View current account balance.  
  - **Deposit Money**: Add funds to the account.  
  - **Withdraw Money**: Withdraw funds (checks for insufficient balance).  
  - **Transfer Money**: Transfer funds to another registered account (validates recipient account existence).  
  - **Change Password**: Update account password.  

- **Data Persistence**:  
  Account details are stored in `.dat` files (one per user), ensuring data persists between sessions.

## Prerequisites

- C compiler (e.g., GCC)
- Unix-based system (for `system("clear")` command support)

## Installation & Usage

1. **Clone the Repository**:  
   ```bash
   git clone https://github.com/Irrfan47/Basic-Bank-Management-System.git
   cd bank-management-system
2. **Compile the Code:**
   ```bash
   gcc main.c -o bank_system
3. **Run the Program:**
   ```bash
   ./bank_system
4. **Follow On-Screen Instructions:**
    - Choose Option 1 to create an account.
    - Choose Option 2 to sign in and perform transactions.
    - Choose Option 3 to exit.

---

## Usage Example

1. **Create an Account:**
   ```bash
   *Welcome To MAS Bank Account System*
    Choose Your Options:
    1. Create a new account
    ...
    Enter your first name: John
    Enter your middle name: Doe
    ...
    Successfully Registered!
2. **Sign In and Transfer Money:**
   ```bash
   User Name: john_doe
    Password: ********
    Press 5 to TRANSFER MONEY
    Enter the recipient's account number: jane_smith
    Enter the amount: 500.00
    Transfer successful!

---

## Limitations

  - Passwords are stored in plain text (no encryption).
  - Input validation is minimal (e.g., no checks for email/phone format).
  - Concurrent access to accounts is not handled.
  - Password change updates the newpassword field but does not overwrite the original password field (requires code adjustment).

---

## Future Improvements

  - Add input validation for emails, phone numbers, and dates.
  - Encrypt sensitive data (e.g., passwords).
  - Implement multi-user concurrency handling.
  - Fix password change functionality to update the correct field.
