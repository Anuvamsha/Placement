# Online Railway Reservation System

A Java-based console application for managing railway ticket bookings with admin and user functionalities.

## Overview

This is a command-line railway reservation system that allows users to book tickets and administrators to manage the system. The application features seat allocation, waiting list management, and ticket history tracking.

## Features

### Admin Features
- **Login Authentication**: Secure admin login with credentials (ID: "anu", Password: "24062002")
- **Account Security**: 3-attempt login protection with account lockout
- **Seat Management**: Add and configure number of stations and seats
- **Availability View**: Check real-time seat availability across all routes

### User Features
- **User Registration**: Create new user accounts with name and password
- **User Login**: Secure authentication with auto-generated User ID
- **Ticket Booking**: 
  - Select starting and landing points (7 stations available)
  - Automatic seat allocation
  - Waiting list support when seats are full
- **Ticket Cancellation**: Cancel booked tickets and promote waiting list passengers
- **Booking History**: View all current and waiting list bookings

## System Architecture

### Data Structures

**Main Arrays:**
- `seat[][]`: 10x7 array for storing booked seat information
- `waitseat[][]`: 3x7 array for managing waiting list seats
- `station[][]`: 5x10 array for station management

**Collections:**
- `Booking`: ArrayList storing confirmed bookings
- `Waiting`: ArrayList storing waiting list entries
- `User_List`: ArrayList maintaining user profiles

### Classes

1. **Main**: Core application with all methods for admin and user operations
2. **Creat_User_Obj**: User profile class storing name, password, and ID
3. **Booking_S**: Booking details class with user info, seat, and route information
4. **Waiting_S**: Waiting list entry class with same structure as Booking_S

## Usage

### Running the Application

```bash
javac Railway.java
java com.anuvamsha.Main
```

### Main Menu

```
Welcome To Online Reservation System!
1 -> Admin
2 -> User
3 -> Exit
```

### Admin Access
- Enter Admin ID: `anu`
- Enter Admin Password: `24062002`
- Max 3 login attempts before lockout

### User Workflow
1. Select "Register" to create a new account
2. Login with your User ID and password
3. Book tickets by selecting starting and landing points
4. View booking history anytime
5. Cancel tickets as needed

## Example Stations

The system supports 7 stations:
- Place → 1
- Place → 2
- Place → 3
- Place → 4
- Place → 5
- Place → 6
- Place → 7

## Seat System

- **Regular Seats**: 10 rows available for confirmed bookings
- **Waiting List Seats**: 3 rows for overflow when regular seats are full
- **Automatic Promotion**: Waiting list passengers are automatically promoted to regular seats when bookings are cancelled

## Key Features

### Intelligent Seat Allocation
- Checks seat availability for the selected route
- Allocates continuous seats across stations
- Falls back to waiting list if no seats available

### Waiting List Management
- Maintains separate waiting list with limited capacity
- Automatically upgrades waiting passengers when seats become available
- Tracks waiting list status in booking history

### Session Management
- Clear screen functionality for better UI
- Persistent data storage during session
- Easy navigation between admin and user panels

## Default Credentials

**Admin:**
- User ID: `anu`
- Password: `24062002`
- Login Attempts: 3

## Notes

- Booking IDs start from 1001
- User IDs are auto-generated starting from 1
- The system uses 1-based indexing for stations and seats
- Seat allocation uses a first-fit algorithm

## Future Enhancements

- Database integration for persistent storage
- Enhanced UI with GUI
- Email notifications for booking confirmations
- Payment gateway integration
- Train schedule management
- Advanced analytics and reporting

---

**Package**: `com.anuvamsha`

**Language**: Java

**Type**: Console Application
