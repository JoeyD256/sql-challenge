# sql-challenge

## Background
The goal of this project was to conduct research about people who the company employed during the 1980s and 1990s. I was tasked with designing the tables to hold the data from the CSV files, import the CSV files into a SQL database and then answer questions about the data.

## Creating Necessary Tables
I started off by sketching the relational database in a free to use tool: https://www.quickdatabasediagrams.com/
When I determined what all of the tables were going to be, and I decided what the primary keys and foreign keys were going to be, I created them (lines 3 - 40).

## Answering Provided Questions
### List the employee number, last name, first name, sex, and salary of each employee
For this step, I selected the columns called "emp_no," "last_name," "sex," and "salary" from the employees table and joined it with the salaries table (lines 44 - 47).

### List the first name, last name, and hire date for the employees who were hired in 1986
For this, I selected the first_name, last_name, and hire_data columns from the employees table, and filtered the returned values using the where the hire date value was in the year 1986 (lines 51 - 52).

### List the manager of each department along with their department number, department name, employee number, last name, and first name
I displayed this information by selecting the columns "dept_no", "dept_name", "emp_no", "last_name", and "first_name" from the "dept_manager" table. Then I joined it with the "employees" table, then joined that with the "departments" table. (lines 56 - 61). 

### List the department number for each employee along with that employee's employee number, last name, first name, and department name
For this, I selected the "dept_no" and "emp_no" columns from the "dept_emp" table, the "last_name" and "first_name" columns from the "employees" table, and the "dept_name" from the "departments" table joined together. (lines 65 - 70)


### List first name, last name, and sex of each employee whose first name is Hercules and whos last name begins with the letter B.
To make this query I selected the "first_name", "last_name", and "sex" columns from the "employees" table. Then I filtered the results to only return the values where the "first_name" column value is "Hercules" and the "last_name" column has a value that starts with the letter "B." (lines 74 - 77)

### List each employee in the Sales department, including their employee number, last name, and first name
To display this, I selected the "dept_name" and "dept_no" from the "departments" table, the "emp_no" column from the "dept_emp" table, the "first_name" and "last_name" columns from the "employees table" table joined together, and filtered the values where the "dept_name" column has a value of "Sales". (lines 81 - 87).

### List each employee in the Sales and Development departments, including their employee number, last name, first name, and departments name
Finally, for this step, I selected the "dept_name" column from the "departments" table, the "emp_no" from the "dept_emp" table, and the "first_name" and "last_name" columns from the "employees" table joined together and filtered the results where the "dept_name" column equaled "Sales" or the "dept_name" colum equals "Development" (lines 91 - 98).


## Credits
For this challenge, no outside support was used.

It is important to note that on the rubric for this assignment, it says that Primary Keys should be set for all tables. However, for the 'dept_emp' table, both columns had reoccuring values, and thus I could not create a primary key for that table.
