# Filtering-SQL-Queries

## Objective

### Skills Learned
- Understanding of SQL filters
- Querying information from an SQL database based on set parameters.

### Tools Used
- SQL

## Steps

### Retrieve After Hours Failed Login Attempts

It was recently discovered that a potential security incident has occurred after business hours. To investigate this, you need to query the ‘log_in_attempts’ table and review after hours login activity. To investigate the failed login attempts after 18:00, I would use the command ‘SELECT * FROM log_in_attempts WHERE login_time > ‘18:00’ AND success = 0;’. Since the entire table only has 200 entries, ;*’ is viable to get a full detail of login attempts. The ‘login_time > ’18:00’’ section will return all login attempts after the specified office hours and success = 0 is a Boolean variable type and ensures the output will return only the failed login attempts.

<p align="center">
  <img src="https://github.com/user-attachments/assets/e0554d68-792c-4d56-b392-c21471de0d58">
</p>

