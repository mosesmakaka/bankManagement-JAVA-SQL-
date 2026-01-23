## 🏦 **BANK MANAGEMENT SYSTEM - JAVA SWING + JDBC + MYSQL**



📋 DESCRIPTION
---------------------------------------------------------------
This is a Java-based Bank Management System built using Swing for the GUI
and JDBC for database operations. The system allows users to register,
select account types, perform deposits, withdrawals, and change their PIN.

It connects to a MySQL database and uses the JCalendar library
(`jcalendar.jar`) for date selection.

🛠 TECHNOLOGIES USED
---------------------------------------------------------------
- Java (JDK 8+)
- Swing (for GUI)
- JDBC (for DB connection)
- MySQL (for database)
- jcalendar.jar (for date selection)



🧾 DATABASE SCHEMA (MySQL)
---------------------------------------------------------------
USE bankdb;

CREATE TABLE signup (
  formno VARCHAR(20), name VARCHAR(50), fname VARCHAR(50),
  dob VARCHAR(20), gender VARCHAR(10), email VARCHAR(50),
  marital VARCHAR(10), address VARCHAR(100), city VARCHAR(30),
  pincode VARCHAR(10), state VARCHAR(30)
);

CREATE TABLE signuptwo (
  formno VARCHAR(20), religion VARCHAR(20), category VARCHAR(20),
  income VARCHAR(20), education VARCHAR(20), occupation VARCHAR(20),
  pan VARCHAR(20), aadhar VARCHAR(20), scitizen VARCHAR(10),
  eaccount VARCHAR(10)
);

CREATE TABLE signupthree (
  formno VARCHAR(20), accountType VARCHAR(30),
  cardno VARCHAR(20), pin VARCHAR(10), facility VARCHAR(200)
);

CREATE TABLE login (
  formno VARCHAR(20), cardno VARCHAR(20), pin VARCHAR(10)
);

CREATE TABLE bank (
  pin VARCHAR(10), date VARCHAR(50),
  type VARCHAR(20), amount VARCHAR(20)
);

✅ FEATURES
---------------------------------------------------------------
- Multi-step Signup form
- Card number and PIN generation
- Deposit and Withdraw functionality
- Change PIN (with PIN confirmation)
- JDBC-based data insertion and validation
- Input field validations (like max ₹10,000 withdrawal)

🔧 SETUP INSTRUCTIONS
---------------------------------------------------------------
1. Install MySQL and create `bankdb` database using the above schema.
2. Add `jcalendar.jar` to your project classpath.
3. Add MySQL Connector JAR to your project (`mysql-connector-java-x.x.x.jar`)
4. Update `Con.java` with your DB credentials:

   Example:
   -----------------------------------
   connection = DriverManager.getConnection(
     "jdbc:mysql://localhost:3306/bankdb", 
     "root", 
     "your_mysql_password"
   );
   -----------------------------------

5. Run `login.java` to begin registration.
6. After completing all forms, you can deposit, withdraw or change PIN.

📍 NOTES
---------------------------------------------------------------
- Make sure MySQL server is running.
- Add `jcalendar.jar` to your libraries to use JDateChooser.
- You can add more validations (e.g., valid email, Aadhar format).
- Improve UX by connecting all screens from a proper Login page.

👨‍💻 AUTHOR
---------------------------------------------------------------
Developed by: Yeswanth
3rd Year CSE Student  
Aspiring Full Stack Java Developer
