# 🎓 Student Mark Management System
A Java-based dynamic web application for managing student marks. This project supports CRUD operations and report generation using JSP, Servlets, JDBC, and MySQL. It is developed as a Dynamic Web Project in Eclipse IDE and deployed on Apache Tomcat.
# 📌 Features
📝 Add a new student mark record

🛠️ Update existing student mark information

❌ Delete student mark record using student ID

📋 Display student marks using student ID

📊 Reports:
Marks by subject and above a threshold

All student mark records
🧮 Database Setup
Step 1: Create the Database
Open phpMyAdmin or MySQL CLI (via XAMPP) and run the following SQL:

sql
Copy
Edit
CREATE DATABASE markdb;
USE markdb;

CREATE TABLE StudentMarks (
    studentID INT PRIMARY KEY,
    studentName VARCHAR(100),
    subject VARCHAR(100),
    marks INT,
    examDate DATE
);
🧑‍💻 How to Run the Project
Step 1: Clone the Repository
Download or clone the project:

bash
Copy
Edit
git clone https://github.com/yourusername/mark-management-system.git
Or manually download the ZIP and extract it.

Step 2: Import into Eclipse
Open Eclipse IDE

Go to File > Import > Existing Projects into Workspace

Choose "Select root directory" and browse to the extracted folder MarkWebApp

Click Finish

Step 3: Set Up MySQL Connection
Open MarkDAO.java in src/dao folder

Update these lines with your database credentials:

java
Copy
Edit
private final String jdbcURL = "jdbc:mysql://localhost:3306/markdb";
private final String jdbcUsername = "root";
private final String jdbcPassword = "your_password";
Make sure MySQL is running via XAMPP.

Step 4: Configure Apache Tomcat
Add Apache Tomcat 10+ to Eclipse:

Window > Preferences > Server > Runtime Environments

Right-click on the project > Run As > Run on Server

Then visit:

arduino
Copy
Edit
http://localhost:8080/MarkWebApp/
📁 Project Structure
pgsql
Copy
Edit
MarkWebApp/
├── WebContent/
│   ├── index.jsp
│   ├── markadd.jsp
│   ├── markupdate.jsp
│   ├── markdelete.jsp
│   ├── markdisplay.jsp
│   ├── displayMarks.jsp
│   ├── reports.jsp
│   ├── report_form.jsp
│   └── report_result.jsp
├── src/
│   ├── dao/
│   │   └── MarkDAO.java
│   ├── model/
│   │   └── StudentMark.java
│   └── servlet/
│       ├── AddMarkServlet.java
│       ├── UpdateMarkServlet.java
│       ├── DeleteMarkServlet.java
│       ├── DisplayMarksServlet.java
│       ├── ReportServlet.java
│       └── ReportCriteriaServlet.java
└── WEB-INF/
    └── web.xml
    
# 🧪 Tools and Technologies
Java (JDK 11+)

JSP and Servlets

JDBC (MySQL connectivity)

Apache Tomcat 10+

MySQL with XAMPP

Eclipse IDE

HTML/CSS

🙌 Author
Developed by: Mehek H N

