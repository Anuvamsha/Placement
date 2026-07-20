# Placement Preparation - Java Console Applications

A collection of **three practice projects** demonstrating core Java concepts, object-oriented design, and system architecture for placement interview preparation.

## 📚 Projects Overview

| Project | Type | Key Features |
|---------|------|--------------|
| **Amazon E-Commerce** | Multi-tier marketplace | Admin/Merchant/User roles, Shopping cart, Wallet system |
| **ATM Management** | Banking simulation | Secure authentication, Cash management, Transactions |
| **Railway Reservation** | Booking system | Seat allocation, Waiting lists, Ticket management |

## 🚀 Quick Start

Each project is standalone and can be compiled/run independently:

```bash
# Amazon E-Commerce Platform
javac Amazon.java
java com.anuvamshasa.Main

# ATM Management System
javac ATM.java
java com.anuvamsha.Main

# Railway Reservation System
javac Railway.java
java com.anuvamsha.Main
```

## 📖 Detailed Documentation

- [**Amazon E-Commerce Platform**](./AMAZON_README.md) - Full marketplace simulation with merchant and user management
- [**ATM Management System**](./ATM_README.md) - Banking operations with secure authentication
- [**Railway Reservation System**](./Railway_README.md) - Ticket booking with waiting list management

## 🎯 Common Concepts Across All Projects

All three projects demonstrate real-world software engineering patterns:

### 🔐 Security & Authentication
- **Multi-level Access Control** - Different roles (Admin, User, Merchant)
- **Account Lockout Protection** - 3-attempt limit to prevent brute force attacks
- **Secure Credentials** - Password-based authentication

### 📊 Data Management
- **Collections Framework** - ArrayLists, Dictionaries for dynamic data storage
- **Arrays** - 2D arrays for seat allocation and cash management
- **Data Structures** - Custom classes for users, transactions, and bookings

### 💼 Business Logic
- **Transaction Processing** - Handling purchases, withdrawals, and bookings
- **Inventory Management** - Stock tracking and updates
- **State Management** - User sessions and cart/wallet management

### 🎨 Design Patterns
- **Object-Oriented Programming** - Classes and inheritance
- **Encapsulation** - Data hiding and controlled access
- **Separation of Concerns** - Clear role-based functionality

## 📋 Project Requirements

- **Java Development Kit (JDK)** 8 or higher
- **No external dependencies** - Uses only built-in Java libraries

## 🔍 Project Details

### 1. Amazon E-Commerce Platform
**What it teaches:** Multi-tier system design, inventory management, financial transactions

**Key Components:**
- Admin panel for merchant verification and product management
- Merchant portal for inventory and pricing control
- User panel with shopping cart and wallet functionality
- Real-time product availability tracking

**Credentials:**
```
Admin ID: anu
Password: 24062002
```

### 2. ATM Management System
**What it teaches:** Banking operations, denomination optimization, secure account management

**Key Components:**
- Admin deposit and ATM balance management
- User authentication with PIN security
- Smart withdrawal algorithm (optimal denomination usage)
- Transaction history tracking

**Sample User:**
```
Username: Shadow
PIN: 1907
Balance: 5000
```

### 3. Railway Reservation System
**What it teaches:** Resource allocation, waiting list management, real-time availability

**Key Components:**
- Admin seat and station configuration
- User ticket booking with automatic seat allocation
- Waiting list with automatic promotion
- Ticket cancellation and booking history

**Credentials:**
```
Admin ID: anu
Password: 24062002
```

## 💡 Learning Outcomes

After exploring these projects, you'll understand:

✅ How to implement user authentication and authorization  
✅ Managing complex data structures and collections  
✅ Implementing business logic (transactions, inventory, bookings)  
✅ Handling edge cases (account lockout, insufficient balance, seat availability)  
✅ Clean code practices with multiple classes and methods  
✅ Console-based UI design and user interaction  

## 🔧 System Architecture Pattern

All three projects follow a similar architectural pattern:

```
Main Entry Point
    ↓
Authentication Layer
    ├─ Admin Login
    ├─ User/Merchant Login
    └─ Account Lockout Protection
    ↓
Role-Based Menu
    ├─ Admin Operations
    ├─ User/Merchant Operations
    └─ Back to Main Menu
    ↓
Data Management
    ├─ Collections (ArrayList, Dictionary)
    ├─ In-Memory Storage
    └─ Session-based State
```

## 📝 Common Features

| Feature | Amazon | ATM | Railway |
|---------|--------|-----|---------|
| Admin Authentication | ✅ | ✅ | ✅ |
| Account Lockout | ✅ | ✅ | ✅ |
| User Registration | ✅ | ✅ | ✅ |
| Transaction History | ✅ | ✅ | ✅ |
| Balance Management | ✅ | ✅ | ✅ |
| Inventory System | ✅ | ✅ | ✅ |

## 🎯 Ideal Use Cases

**For Interview Preparation:**
- Understand how large systems are broken into smaller components
- Practice explaining system architecture and design decisions
- Demonstrate knowledge of collections and data structures
- Show ability to implement real-world business logic

**For Learning:**
- Fundamental Java concepts in practical context
- How to structure a console application
- Best practices for authentication and data management
- Object-oriented design principles

## 🚀 Future Enhancements

All projects can be extended with:
- ✨ Database integration (SQL/JDBC) for persistent storage
- 🎨 GUI interface (Swing/JavaFX)
- 🔐 Enhanced security (encryption, hashing)
- 📊 Analytics and reporting features
- 🌐 Network support for distributed access
- 📱 Mobile application ports

## 📄 Repository Structure

```
Placement/
├── README.md (This file - Overview)
├── AMAZON_README.md (Project-specific documentation)
├── ATM_README.md (Project-specific documentation)
├── Railway_README.md (Project-specific documentation)
├── Amazon.java (Source code)
├── ATM.java (Source code)
└── Railway.java (Source code)
```

## 📝 Notes

- All projects use **in-memory storage** - data is reset when the program terminates
- Screen clearing uses `System.out.print("\033[H\033[2J")` - works on Unix-like systems
- Each project is **independent** and can be run separately
- Projects are designed for **educational purposes** and interview preparation

## 🤝 Contributing

Feel free to fork this repository and submit pull requests for:
- Bug fixes
- Code optimizations
- Feature additions
- Documentation improvements

## ✍️ Author

**Anuvamsha** - Placement Preparation Portfolio

---

**Last Updated**: 2026-07-20

**Status**: ✅ Complete - Ready for interview preparation and learning
