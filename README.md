# ATM Management System

A Java-based ATM (Automated Teller Machine) simulation that implements core banking functionalities with both admin and user access control.

## 📋 Table of Contents

- [Features](#features)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
  - [Admin Panel](#admin-panel)
  - [User Panel](#user-panel)
- [System Architecture](#system-architecture)
- [Default Credentials](#default-credentials)
- [File Structure](#file-structure)

## ✨ Features

### Admin Features
- **Secure Admin Login** - Authentication with username and password
- **Account Lockout** - Automatic account lock after 3 failed login attempts
- **Deposit Money** - Add cash denominations to the ATM (2000, 500, 200, 100)
- **Check ATM Balance** - View total cash available and individual denomination counts

### User Features
- **User Authentication** - Login with user ID and PIN
- **Check Balance** - View current account balance
- **Deposit Money** - Deposit funds in denominations (2000, 500, 200, 100)
- **Withdraw Money** - Withdraw cash with automatic denomination optimization
- **Mini Statement** - View transaction history
- **Change PIN** - Update account security PIN
- **Account Lockout** - Automatic lock after 3 failed login attempts

## 🏗️ Project Structure

```
ATM Management System
├── Admin Authentication
├── User Authentication
├── Account Management
├── Transaction Processing
└── ATM Cash Management
```

## 📦 Prerequisites

- Java Development Kit (JDK) 8 or higher
- No external dependencies required

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Anuvamsha/Placement.git
   cd Placement
   ```

2. **Compile the Java file**
   ```bash
   javac ATM.java
   ```

3. **Run the application**
   ```bash
   java com.anuvamsha.Main
   ```

## 📖 Usage

### Main Menu
When you start the application, you'll see the main menu with three options:
- **Option 1**: Admin Login
- **Option 2**: User Login
- **Option 3**: Exit

### Admin Panel

**Default Credentials:**
- **Username**: Anu
- **Password**: 24062002

**Admin Menu Options:**
1. **Deposit Money** - Add cash denominations to ATM
   - Enter the count for 2000, 500, 200, and 100 denominations
   
2. **Check Balance** - View ATM cash status
   - Shows count and total amount for each denomination
   - Displays total amount in the ATM

3. **Back** - Return to main menu

### User Panel

**Sample User Accounts:**
- **User 1**
  - Username: Shadow
  - PIN: 1907
  - Initial Balance: 5000

- **User 2**
  - Username: Dark
  - PIN: 1907
  - Initial Balance: 6000

**User Menu Options:**
1. **Deposit Money** - Add funds to your account
   - Enter counts for each denomination (2000, 500, 200, 100)

2. **Check Balance** - View current account balance
   - Displays username and account balance

3. **Withdraw Money** - Withdraw funds from your account
   - System checks ATM availability and account balance
   - Automatically optimizes denomination usage

4. **Mini Statement** - View transaction history
   - Shows all deposits and withdrawals with timestamps

5. **Change PIN** - Update your account PIN
   - Enter new password for future logins

6. **Back to Main Menu** - Return to main menu

## 🔒 Security Features

- **Authentication**: Dual-factor (username/ID and password/PIN)
- **Account Lockout**: Automatic 3-attempt lockout protection
- **Password Change**: Users can update their PIN anytime
- **Transaction Logging**: All transactions are timestamped and recorded

## 💰 Denomination Support

The ATM supports the following denominations:
- **2000** - High value notes
- **500** - Medium-high value notes
- **200** - Medium value notes
- **100** - Low value notes

## 🔧 System Architecture

### Key Components

1. **Main Class** - Entry point and core logic
2. **Admin Login** - Validates admin credentials
3. **Admin Panel** - Manages ATM cash inventory
4. **User Login** - Authenticates user accounts
5. **User Panel** - User transaction interface
6. **Width_draw Method** - Processes withdrawal with optimal denomination algorithm

### Data Structures

- `money[]` - Array storing denomination counts in ATM
- `atm[]` - Array of user accounts
- `User_Statement` - ArrayList for transaction history

## 📊 Sample Transactions

### Deposit Example
```
Admin deposits:
- 5 notes of 2000 = 10,000
- 10 notes of 500 = 5,000
- 15 notes of 200 = 3,000
- 20 notes of 100 = 2,000
Total: 20,000
```

### Withdrawal Example
```
User withdraws: 4700
Optimal distribution:
- 2 × 2000 = 4,000
- 1 × 500 = 500
- 1 × 200 = 200
Total: 4,700
```

## 🎯 Future Enhancements

- Database integration for persistent storage
- GUI interface using Swing or JavaFX
- Multiple ATM support
- Enhanced withdrawal denomination optimization
- Transaction receipts generation

## 📝 Notes

- The application uses `System.out.print("\033[H\033[2J")` for screen clearing (works on Unix-like systems)
- All user data is stored in memory and will be reset when the program terminates
- The withdrawal system checks both user balance and ATM availability

## 📄 License

This project is for educational purposes as part of placement preparation.

## 🤝 Contributing

Feel free to fork this repository and submit pull requests for any improvements.

## ✍️ Author

Anuvamsha

---

**Last Updated**: 2026-07-20
