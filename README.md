# SQL-challenge

## Contents

- [Overview](#overview)
- [Data Modeling](#data-modeling)
- [Data Engineering](#data-engineering)
- [Data Analysis](#data-analysis)
- [Contact](#contact)
- [Acknowlegements](#acknowledgements)

## Overview

This challenge involves creating a database to store and manage employee information. The data includes details about employees, departments, salaries, job titles, and managers. Using SQL, we organize this data into tables and establish connections between them to make it easier to query and analyze.

It is divided into 3 parts: data modeling, data engineering, and data analysis.

## Data Modeling

In this phase, the database structure is designed using an Entity-Relationship Diagram (ERD). The ERD visualizes how different entities (employees, departments, salaries, titles, dept_emp, dept_manager) relate to one another.

![alt text](image.png)

The ERD image above represents the design of an Employee Management Database. It shows how different entities (tables) are related:

1. Departments: Stores department information (e.g., department number, name).
2. Employees: Holds employee details (e.g., employee number, name, hire date).
3. Dept_emp: Acts as a bridge table to track which department each employee belongs to, allowing for a many-to-many relationship between employees and departments.
4. Dept_manager: Tracks which employees are managers of departments, with a one-to-one relationship between departments and managers.
5. Titles: Stores the job titles for employees, linked to the employees table.
6. Salaries: Records the salary history for each employee, with multiple salary records possible for each employee.

The diagram ensures that all data (e.g., employee roles, departments, salaries) is interconnected through foreign keys, providing a clear structure for managing employee-related information in the database.

## Data Engineering

In this phase, the database tables are created using the SQL script (employees_table_schemata.sql). The script defines the structure of the database with the following key tables:

1. employees: Stores employee information (e.g., name, birth date, hire date).

![alt text](employees_table.png)

2. departments: Holds department details.

![alt text](departments_table.png)

3. titles: Lists job titles for employees.

![alt text](titles_table.png)

4. salaries: Tracks salary history for each employee.

![alt text](salaries_table.png)

5. dept_emp: Connects employees to departments.

![alt text](dept_emp_table.png)

6. dept_manager: Tracks managers for each department.

![alt text](dept_manager_table.png)

- Relationships

Foreign keys ensure that the tables are properly connected. For example, dept_emp links employees to departments, and salaries tracks salary records for each employee.

- Data Integrity

Primary keys and foreign keys are used to maintain data consistency and prevent errors between the tables.

## Data Analysis

In this phase, SQL queries are used to analyze employee data.
The following queries were executed to analyze the employee data. These queries provide insights into employee salaries, department assignments, managerial roles, and more.

1. Employee Salaries

- List the employee number, last name, first name, sex, and salary of each employee.

![alt text](https://github.com/rinals/sql-challenge/blob/89750d07ce700edb64fffead8f3e0a62c39b19ef/EmployeeSQL/images/Data_analysis/Query1.png)

This query lists the employee number, first name, last name, sex, and salary for each employee by joining the employees and salaries tables.

2. Employees Hired in 1986

- List the first name, last name, and hire date for the employees who were hired in 1986.

![alt text](https://github.com/rinals/sql-challenge/blob/89750d07ce700edb64fffead8f3e0a62c39b19ef/EmployeeSQL/images/Data_analysis/Query2.png)

This query retrieves the first name, last name, and hire date of employees who were hired in 1986.

3. Department Managers
  
- List the manager of each department along with their department number, department name, employee number, last name, and first name.

![alt text](https://github.com/rinals/sql-challenge/blob/89750d07ce700edb64fffead8f3e0a62c39b19ef/EmployeeSQL/images/Data_analysis/Query3.png)

This query lists the managers of each department along with their department number, department name, employee number, and employee names.

4. Employees by Department

- List the department number for each employee along with that employee’s employee number, last name, first name, and department name.

![alt text](https://github.com/rinals/sql-challenge/blob/89750d07ce700edb64fffead8f3e0a62c39b19ef/EmployeeSQL/images/Data_analysis/Query4.png)

This query lists the department number, employee number, and employee names for each department.

5. Employees Named Hercules with Last Name Starting with 'B'

- List first name, last name, and sex of each employee whose first name is Hercules and whose last name begins with the letter B.

![alt text](https://github.com/rinals/sql-challenge/blob/89750d07ce700edb64fffead8f3e0a62c39b19ef/EmployeeSQL/images/Data_analysis/Query5.png)

This query lists employees whose first name is "Hercules" and last name starts with the letter 'B'.

6. Employees in Sales Department

- List each employee in the Sales department, including their employee number, last name, and first name.

![alt text](https://github.com/rinals/sql-challenge/blob/89750d07ce700edb64fffead8f3e0a62c39b19ef/EmployeeSQL/images/Data_analysis/Query6.png)

This query lists employees in the Sales department, including their employee number, name, and department name.

7. Employees in Sales and Development Departments

- List each employee in the Sales and Development departments, including their employee number, last name, first name, and department name.

![alt text](https://github.com/rinals/sql-challenge/blob/89750d07ce700edb64fffead8f3e0a62c39b19ef/EmployeeSQL/images/Data_analysis/Query7.png)

This query lists employees in both the Sales and Development departments.

8. Frequency of Last Names

- List the frequency counts, in descending order, of all the employee last names (that is, how many employees share each last name).

![alt text](https://github.com/rinals/sql-challenge/blob/89750d07ce700edb64fffead8f3e0a62c39b19ef/EmployeeSQL/images/Data_analysis/Query8.png)

This query retrieves the frequency count of each last name among employees, sorted in descending order.

## Contact

Rinal Shastri - rinal.shastri@outlook.com or rinaljoginshastri@gmail.com
Github - https://github.com/rinals

## Acknowledgements

Brian Perry - edexbootcamp/ucberkeley -  TA

ChatGPT

