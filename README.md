# Hotel Reservation System

A console-based hotel room reservation system built with *Java, **JDBC* and *MySQL*.

## Features
- Reserve a room (with duplicate room booking check)
- View all reservations
- Get room number by reservation ID and guest name
- Update a reservation
- Delete a reservation

## Tech Stack
- Java
- JDBC (MySQL Connector/J)
- MySQL
- IntelliJ IDEA

## Security
- All queries use PreparedStatement (protects against SQL injection)
- Database credentials are kept in config.properties, which is excluded from Git via .gitignore

## Database Setup
sql
CREATE DATABASE IF NOT EXISTS hotel_db;
USE hotel_db;

CREATE TABLE IF NOT EXISTS reservations (
    reservation_id INT AUTO_INCREMENT PRIMARY KEY,
    guest_name VARCHAR(100) NOT NULL,
    room_number INT NOT NULL,
    contact_number VARCHAR(15) NOT NULL,
    reservation_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);


## How to Run
1. Install MySQL and create the database using the SQL above.
2. Add mysql-connector-j to the project libraries.
3. Create a config.properties file in the project root:
   
   db.url=jdbc:mysql://localhost:3306/hotel_db
   db.username=root
   db.password=your_password_here
   
4. Run HotelReservationSystem.java.

## Author
*Ritik Singh*
- GitHub: https://github.com/ritiksingh73838-arch
- Email: your_email@gmail.com
