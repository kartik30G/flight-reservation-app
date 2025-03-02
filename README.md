# Flight-Reservation-App
Flight Reservation App by Cloudblitz | Greamio Technologies Pvt Ltd

## Overview
The **Flight Reservation System** is a web application that allows users to search for flights, book tickets, and manage their reservations. This application is built using Java (Spring Boot) for the backend and MySQL as the database.

## Features
- ✅ User authentication and authorization
- ✈️ Flight search and booking
- 🛠️ Admin dashboard for flight management

## Prerequisites
Before setting up the application, ensure you have the following installed on your system:

- **🖥️ Ubuntu/Linux Environment**
- **🗄️ MySQL Server**
- **☕ OpenJDK 17**
- **🛠️ Maven**
- **📂 Git**

## Database Setup Instructions

### Step 1: Update Package List
```sh
apt update
```

### Step 2: Install MySQL Server
```sh
apt install mysql-server -y
```

### Step 3: Secure MySQL Installation
```sh
mysql_secure_installation
```

### Step 4: Login to MySQL and Create Database
```sh
mysql -uroot -p
>> CREATE DATABASE flightdb;
>> CREATE USER "DBUSER" IDENTIFIED BY "DBPASSWORD";
>> GRANT ALL PRIVILEGES ON flightdb.* TO "DBUSER";
>> FLUSH PRVILEGES;
```

## Backend Setup Instructions

### Step 1: Install Java (OpenJDK 17)
```sh
apt install openjdk-17-jdk -y
```

### Step 2: Install Maven
```sh
apt install maven -y
```

### Step 3: Clone the Repository
```sh
git clone https://github.com/shubhamkalsait/flight-reservation-app.git
```

### Step 4: Navigate to the Backend Directory
```sh
cd flight-reservation-app/Backend/FlightReservationApp/
```

### Step 5: Set Up Database Configuration
```sh
export DATASOURCE_URL="jdbc:mysql://localhost:3306/flightdb"
export DATASOURCE_USER="DBUSER"
export DATASOURCE_PASSWORD="DBPASSWORD"
```

### Step 6: Build the Application
```sh
mvn clean package
```

## Running the Application
Once the build is successful, you can run the application using:
```sh
java -jar target/flight-reservation-app.jar
```


