# Farmer–Retailer Auction

A Java console application where farmers can list agricultural products and retailers can place bids to purchase them. The application saves user and auction data in files between sessions.

## Features

- Register as a farmer, individual retailer, or company retailer
- Log in with a registered username
- Create and view product listings with quantities and base prices
- Place retailer bids on listings
- Let farmers select a winning bid and close an auction
- Save closed auction results in a history file

## Requirements

- Java Development Kit (JDK)
- A terminal or Java IDE

## Run the application

From the project directory, compile the Java files:

```bash
javac Main.java models/*.java enums/*.java services/*.java controllers/*.java
```

Start the application:

```bash
java Main
```

## How to use

1. Register with a username and choose a user type.
2. Log in with your username.
3. Farmers can create listings, view listings, and close auctions.
4. Retailers can view listings, review retailer bids, and place bids.
5. When closing a listing, the farmer selects the winning retailer bid.

## Data files

The application uses files in the `files/` directory:

- `users.txt` stores registered users and their roles.
- `base_bids.txt` stores product listings.
- `retailer_bids.txt` stores retailer bids.
- `history.txt` stores closed auction results.

**Setup note:** The current source code uses hard-coded Windows file paths for data storage. Update those paths in `UserAuthentication.java` and `BidManagement.java` to match your computer before running the application.

## Project structure

.
├── Main.java
├── controllers/
│   └── BidManagement.java
├── enums/
│   └── UserType.java
├── files/
├── models/
│   ├── Bid.java
│   └── User.java
└── services/
    └── UserAuthentication.java

## Note

This is a console-based project for learning and demonstration. Login currently checks usernames only and does not use passwords.