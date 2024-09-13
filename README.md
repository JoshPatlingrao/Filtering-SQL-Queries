# Filtering-SQL-Queries

This project was facilitated by the Google Cybersecurity Professional Certificate in Coursera. The student was in a scenario where they're currently working to make their organization's system more secure. Their tasks will involve ensuring that the system is safe, investigating all potential security issues, and updating employee computers as needed. The following steps will demonstrate how they use SQL with filters to perform security-related tasks.

## Objective

### Skills Learned
- Understanding of SQL filters
- Querying information from an SQL database based on set parameters.

### Tools Used
- SQL

## Steps

### Retrieve After Hours Failed Login Attempts

It was recently discovered that a potential security incident has occurred after business hours. To investigate this, I need to query the ‘log_in_attempts’ table and review after hours login activity. To investigate the failed login attempts after 18:00, I would use the command ‘SELECT * FROM log_in_attempts WHERE login_time > ‘18:00’ AND success = 0;’. Since the entire table only has 200 entries, ;*’ is viable to get a full detail of login attempts. The ‘login_time > ’18:00’’ section will return all login attempts after the specified office hours and success = 0 is a Boolean variable type and ensures the output will return only the failed login attempts.

<p align="center">
  <img src="https://github.com/user-attachments/assets/e0554d68-792c-4d56-b392-c21471de0d58">
</p>

### Retrieve Login Attempts on Specific Dates

A suspicious event occurred on 2022-05-09. To investigate this event, I need to review all login attempts which occurred on this day and the day before. The command I would use for this would be ‘SELECT * FROM log_in_attempts WHERE login_date = ‘2022-05-09’ OR login_date = ‘2022-05-08’;’. I used an OR operator since there are only two specified dates, where it would output login attempts on 2022-05-08 and 2022-05-09.

<p align="center">
  <img src="https://github.com/user-attachments/assets/e57f95dc-ce4a-4b5e-8f71-9fd5e60cff48">
</p>

### Retrieve Login Attempts Outside of Mexico

There has been suspicious activity with login attempts, but the team has determined that this activity didn't originate in Mexico. Now, I need to investigate login attempts that occurred outside of Mexico. The command I would use for this would be ‘SELECT * FROM log_in_attempts WHERE country NOT LIKE ‘MEX%’;’. I used NOT as I want to find login attempts outside of Mexico and the LIKE command to exclude the potential shortened versions of Mexico in country as shown for CAN and Canada. Due to the assumption that any country that starts with Mex represents Mexico the ‘%’ operator will ensure it will be excluded as well.

<p align="center">
 <img src="https://github.com/user-attachments/assets/4674fca4-98df-40fe-b531-66b84feaedf8"> 
</p>

### Retrieve Employees in Marketing

The team wants to perform security updates on specific employee machines in the Marketing department. I will be responsible for getting information on these employee machines and will need to query the employees table. The command I would use for this would be, ‘‘SELECT * FROM employees WHERE department = ‘Marketing’ AND office LIKE ‘East%’;’. I’m only interested in machines being used by the Marketing department which is why I can use the ‘=’ but these machines also need to be in the East building, but due to East building having multiple offices I used the LIKE ‘East%’ command to include every office within the East building. The Like command will return every string containing the word ‘East’ regardless of the office space within.

<p align="center">
  <img src="https://github.com/user-attachments/assets/cafbf0cf-f773-4a68-bc5e-cde855badfe5">
</p>

### Retrieve Employees in Finance and Sales

The team now needs to perform a different security update on machines for employees in the Sales and Finance departments. I would use the command ‘SELECT * FROM employees WHERE department = ‘Sales’ OR department = ‘Finance’;’. I used the OR operator as each employee can only be in one department. It ensures that machines either in Sales or Finance will be included.

<p align="center">
  <img src="https://github.com/user-attachments/assets/528cc381-d776-4c5e-b81c-5c3c95e6c7d7">
</p>

### Retrieve All Employees not in IT

The team needs to make one more update to employee machines. The employees who are in the Information Technology department already had this update, but employees in all other departments need it. I used the command, ‘SELECT * FROM employees WHERE NOT department = ‘Information Technology’;’. In this case I used to NOT operator so every employee who’s in the IT team will be excluded as they have already received the update.

<p align="center">
  <img src="https://github.com/user-attachments/assets/b3448067-23dd-4e24-98d6-89b83c0b436a">
</p>

## Summary

This project has allowed me to demonstrate my ability to filter through various datasets as described by the parameters. I used the AND, OR and NOT operators to filter for specific information, and used LIKE and Wildcard (%) to filter for patterns. Through the use of these operators I am able to filter and extract specific information out of large datasets.
