# Employee Management System

The Employee Management System is a Java-based application designed to manage employee data effectively. It allows users to perform operations such as adding, updating, viewing, and removing employee details. The system also includes user authentication via a login page.

## Features

**Employee Management:**
  - Add new employees
  - Update existing employee details
  - View employee information
  - Remove employees from the system

**User Authentication:**
  - Secure login functionality
  - Newly added signup functionality for user registration

**User Interface:**
  - Simple and intuitive UI
  - Use of images and icons for better user experience

## Getting Started

### Prerequisites

- Java Development Kit (JDK) 8 or higher
- An IDE like IntelliJ IDEA or Eclipse
- MySQL or any other relational database system

### Setup Instructions

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/your-username/employee-management-system.git
   cd employee-management-system
   ```

2. **Import the Project:**
   - Open your IDE and import the project.
   - Ensure all dependencies are resolved and the project is set up correctly.

3. **Database Configuration:**
   - Create a MySQL database and name it `employee_management`.
   - Execute the following SQL script to create the necessary tables:

   ```sql
   CREATE TABLE users (
       id INT PRIMARY KEY AUTO_INCREMENT,
       username VARCHAR(50) NOT NULL UNIQUE,
       password VARCHAR(100) NOT NULL,
       email VARCHAR(100) NOT NULL
   );

   CREATE TABLE employees (
       id INT PRIMARY KEY AUTO_INCREMENT,
       name VARCHAR(100),
       age INT,
       position VARCHAR(100),
       salary DOUBLE
   );
   ```

   - Update the `conn.java` file with your database credentials:

   ```java
   String url = "jdbc:mysql://localhost:3306/employee_management";
   String user = "your-username";
   String password = "your-password";
   ```

4. **Run the Application:**
   - Compile and run the `Main_class.java` file to start the application.
   - Use the login functionality to access the system. If you haven't created a user, use the signup option.

### Adding Signup Functionality

To add the signup option, a new `Signup.java` class was created. This allows new users to register their accounts. The `Login.java` class was also updated to link to the signup form.

### Project Structure

- **src/employee/management/system/**
  - `Main_class.java`: Entry point of the application
  - `Login.java`: Handles user authentication
  - `Signup.java`: Handles new user registration
  - `AddEmployee.java`: Adds new employee records
  - `UpdateEmployee.java`: Updates employee information
  - `RemoveEmployee.java`: Removes employee records
  - `View_Employee.java`: Displays employee details
  - `conn.java`: Manages database connections

- **src/icons/**: Contains icons and images used in the application.

## Contributing

Contributions are welcome! Please submit a pull request or open an issue to discuss any changes.


### Steps to Customize:
1. Replace `your-username` with your actual GitHub username.
2. Customize the MySQL database connection settings in the `conn.java` file as needed.
