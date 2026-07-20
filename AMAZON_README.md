# Amazon E-Commerce Platform

A Java-based e-commerce marketplace simulation that implements a complete platform with admin, merchant, and user functionalities. This system demonstrates multi-level authentication, inventory management, and transaction processing.

## 📋 Table of Contents

- [Features](#features)
- [System Architecture](#system-architecture)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
  - [Admin Panel](#admin-panel)
  - [Merchant Panel](#merchant-panel)
  - [User Panel](#user-panel)
- [Default Credentials](#default-credentials)
- [Classes and Data Structures](#classes-and-data-structures)
- [Key Features](#key-features)

## ✨ Features

### Admin Features
- **Secure Admin Login** - Authentication with username and password
- **View All Products** - See complete product inventory across all merchants
- **Merchant Management** - Add new merchants to the platform
- **Merchant Approval** - Verify and approve merchant accounts
- **Merchant Listing** - View all registered merchants and their details
- **Merchant Deletion** - Remove merchants from the platform
- **Product Management** - Add new product categories to the system

### Merchant Features
- **Merchant Authentication** - Register and login as a merchant
- **Add Products** - List new products for sale
- **Update Products** - Modify product count and pricing
- **Compare Products** - View competitor pricing for same products
- **Remove Products** - Delist products from inventory
- **View Products** - See all products listed by the merchant
- **Verification System** - Admin approval required before selling

### User Features
- **User Authentication** - Register and login functionality
- **Browse Products** - View all available products across merchants
- **Shopping Cart** - Add/manage items in cart
- **Product Purchase** - Buy products with wallet balance
- **Purchase History** - Track all transactions with timestamps
- **Digital Wallet** - Manage money balance
- **Wallet Operations** - Check balance, deposit funds, view statements

## 🏗️ System Architecture

### Three-Tier User Model
```
Admin (Platform Administrator)
├── Merchant (Product Sellers)
│   ├── Add/Update/Remove Products
│   └── Manage Inventory
└── User (Customers)
    ├── Browse Products
    ├── Shopping Cart
    └── Wallet Management
```

### Data Flow
1. **Admin** sets up products and verifies merchants
2. **Merchants** add and price products
3. **Users** browse and purchase products
4. **Transactions** are recorded with timestamps

## 📦 Prerequisites

- Java Development Kit (JDK) 8 or higher
- No external dependencies required (uses built-in Java collections)

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Anuvamsha/Placement.git
   cd Placement
   ```

2. **Compile the Java file**
   ```bash
   javac Amazon.java
   ```

3. **Run the application**
   ```bash
   java com.anuvamshasa.Main
   ```

## 📖 Usage

### Main Menu
When you start the application, you'll see the main menu:
- **Option 1**: Admin Panel
- **Option 2**: Merchant Portal
- **Option 3**: User Portal
- **Option 4**: Exit

### Admin Panel

**Default Credentials:**
- **Admin ID**: anu
- **Admin Password**: 24062002

**Admin Menu Options:**

1. **View All Products** (Option 1)
   - Displays complete product inventory with counts
   - Shows all products from all merchants

2. **Add New Merchant** (Option 2)
   - Create new merchant accounts directly
   - Automatically assign merchant IDs
   ```
   Enter Merchant Name: XYZ Electronics
   Enter Merchant Password: password123
   Your Merchant ID will be auto-generated
   ```

3. **Merchant Approval** (Option 3)
   - Verify pending merchant accounts
   - Required for merchants to start selling
   ```
   Enter Merchant ID: 1
   Status: Verified
   ```

4. **List of Merchants** (Option 4)
   - View all registered merchants
   - See verification status of each merchant

5. **Delete Merchant** (Option 5)
   - Remove merchants from the platform
   - Requires merchant ID

6. **Add Product Category** (Option 6)
   - Create new product categories
   - Initialize product inventory

### Merchant Panel

#### Merchant Authentication

**Merchant Menu:**
- **Option 1**: Login
- **Option 2**: Register
- **Option 3**: Back

**Registration:**
```
Enter Merchant Name: ABC Retail
Enter Password: secure_password
Your User ID -> 1
```

#### Merchant Operations

Once logged in, merchants can:

1. **Add Product** (Option 1)
   - Add products from admin-created categories
   - Set product count and pricing
   ```
   Product Name: Laptop
   Product Count: 50
   Price per Item: 45000
   ```

2. **Update Product** (Option 2)
   - Modify existing product count and price
   - Update pricing strategy

3. **Compare Product** (Option 3)
   - See competitors' pricing
   - Compare across merchants

4. **Remove Product** (Option 4)
   - Delist products from inventory
   - Updates global inventory

5. **List Products** (Option 5)
   - View all products listed by the merchant

### User Panel

#### User Authentication

**User Menu:**
- **Option 1**: Login
- **Option 2**: Register
- **Option 3**: Go Back

**Registration:**
```
Enter User Name: John Doe
Enter Password: user_password
Your User ID -> 1
Initial Wallet Balance: 0
```

#### User Operations

1. **List of Products** (Option 1)
   - Browse all available products
   - View product counts across merchants
   - Add items to cart

2. **Show Cart** (Option 2)
   - View cart contents
   - Purchase items from cart
   - Requires sufficient wallet balance
   ```
   Product: Laptop
   Quantity: 2
   Unit Price: 45000
   Total: 90000
   ```

3. **Purchase History** (Option 3)
   - View all past transactions
   - Timestamped transaction logs

4. **Wallet** (Option 4)
   - Check current balance
   - Deposit funds
   - View transaction statements

5. **Exit** (Option 5)
   - Return to main menu

## 🔒 Security Features

- **Multi-Level Authentication** - Separate login for Admin, Merchant, and User
- **Account Lockout** - 3-attempt limit for failed login
- **Merchant Verification** - Admin approval required before selling
- **Transaction Logging** - All transactions timestamped and recorded
- **Wallet Balance Check** - Prevents overspending

## 💾 Classes and Data Structures

### Main Class
- Central entry point handling all user flows
- Manages authentication for all three user types

### Create_Merchant_obj
```java
public String M_Name, M_Password, M_Verified;
public int M_Id;
public Dictionary<String, ArrayList<String>> M_Products;
```
- Stores merchant information
- Maintains product inventory per merchant

### Creat_User_Obj
```java
public String U_Name, U_Password;
public int U_Id, U_Money;
public Dictionary<String, ArrayList<String>> U_Cart;
public List<String> Statement;
public List<String> U_Buy;
```
- Stores user account details
- Manages shopping cart and wallet
- Maintains purchase history

### Data Collections
- `All_Products` - Global product catalog (Dictionary)
- `Merchants` - List of all merchant accounts (ArrayList)
- `User_List` - List of all user accounts (ArrayList)
- `M_Products` - Products per merchant (Dictionary)
- `U_Cart` - Items in user's cart (Dictionary)
- `U_Buy` - Purchase history (ArrayList)

## 📊 Sample Workflow

### Scenario: Customer Purchases a Laptop

1. **Admin** creates product category "Laptop" with 0 initial count
2. **Merchant ABC** registers and gets ID = 1
3. **Admin** approves Merchant ABC
4. **Merchant ABC** adds 50 Laptops at price 45000
5. **User John** registers with ID = 1
6. **User John** deposits 100000 to wallet
7. **User John** browses products and finds Laptop from Merchant 1
8. **User John** adds 2 Laptops to cart (90000 total)
9. **User John** purchases from cart
10. **User John** wallet balance reduced to 10000
11. **Merchant ABC** inventory reduced to 48 units

## 🎯 Key Algorithms

### Product Price Comparison
- Merchants can compare prices across the platform
- Allows competitive pricing strategy
- Shows all sellers offering the same product

### Smart Cart Management
- Tracks products by Merchant ID and Product Name
- Maintains quantity and unit price
- Prevents duplicate entries

### Transaction Processing
- Checks wallet balance before purchase
- Validates product availability
- Updates all related inventories atomically

## 📝 Notes

- Uses `System.out.print("\033[H\033[2J")` for screen clearing (Unix-like systems)
- All data stored in memory; reset on program termination
- No database persistence (can be enhanced with SQL integration)
- Supports multiple concurrent merchants and users
- Product pricing set by individual merchants

## 🔄 Potential Enhancements

- Database integration for data persistence
- User wallet encryption
- Payment gateway integration
- Product reviews and ratings system
- Order tracking and delivery status
- Merchant analytics and reporting
- GUI interface using Swing/JavaFX
- Multi-currency support
- Promotional codes and discounts
- User wishlists

## 📄 License

This project is for educational purposes as part of placement preparation.

## 🤝 Contributing

Feel free to fork this repository and submit pull requests for improvements.

## ✍️ Author

Anuvamsha

---

**Last Updated**: 2026-07-20
