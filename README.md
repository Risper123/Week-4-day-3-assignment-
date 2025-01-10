# Week-4-day-3-assignment-
My assignment for week 4 day 3
Assignment Questions
You are tasked with creating a database for a bill management system.

One of the tables in this system is the categories table, which stores information about different categories of bills.

Write an SQL query to create the categories table with the following requirements:

I. The table should have a primary key column named categoryID which is an integer and will auto-increment.
II. The table should have another column named categoryName which is a string (VARCHAR) that can hold up to 50 characters.

CREATE TABLE categories (
    categoryID INT AUTO_INCREMENT PRIMARY KEY,
    categoryName VARCHAR(50)
);

Write an SQL query to insert at least 5 categories into the categories table. Each category should have a unique categoryName

INSERT INTO categories (categoryName) VALUES
    ('Rent'),
    ('Utilities'),
    ('Groceries'),
    ('Transportation'),
    ('Entertainment');

    
You are tasked with creating a table for storing customer information in a bills management system. Write an SQL query to create the customer table with the following requirements:
The table should have a primary key column named customerID, which is an integer and will auto-increment.
The table should include the following columns:
customerName: A string (VARCHAR) that can hold up to 50 characters. This field should not allow NULL values.
email: A string (VARCHAR) that can hold up to 50 characters.
phoneNumber: A string (VARCHAR) that can hold up to 11 characters.
customerAddress: A string (VARCHAR) that can hold up to 20 characters.
dateCreated: A timestamp that records the time the customer was added to the database. The default value should be the current timestamp.

CREATE TABLE customer (
    customerID INT AUTO_INCREMENT PRIMARY KEY,
    customerName VARCHAR(50) NOT NULL,
    email VARCHAR(50),
    phoneNumber VARCHAR(11),
    customerAddress VARCHAR(20),
    dateCreated TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

You are tasked with inserting data into the customer table. Write an SQL query to insert at least 4 customer records into the table.

INSERT INTO customer (customerName, email, phoneNumber, customerAddress) VALUES
    ('John Doe', 'john.doe@example.com', '0712345678', 'Nairobi'),
    ('Jane Smith', 'jane.smith@example.com', '0721234567', 'Mombasa'),
    ('David Lee', 'david.lee@example.com', '0731234567', 'Kisumu'),
    ('Sarah Jones', 'sarah.jones@example.com', '0741234567', 'Nakuru');

    
You need to update the customerAddress to "Lavington" for two customers in the customer table. The customers have the following customerID:

customerID = 1 and customerID = 2

Write an SQL query to update the customerAddress to "Lavington" for both customers.

Make sure to use the correct WHERE condition to select the customers by customerID.
UPDATE customer 
SET customerAddress = 'Lavington' 
WHERE customerID IN (1, 2);


You are tasked with deleting a category from the categories table. Write an SQL query to delete the category where the categoryID is equal to 2.

DELETE FROM categories 
WHERE categoryID = 2;
