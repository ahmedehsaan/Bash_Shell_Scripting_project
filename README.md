# Bash_Shell_Scripting_project
Bash Project
Write a bash project that simulate the MySQL database and do the following:
The Project will be under Directory Called MySQL
There will be a main script called MySQL/main.sh
When A user run it the screen will be cleared and ask for the below entry and need to be selected by it’s number Each one will run a specific script.
1) Create Database user.
2) Delete Database User.
3) Create new Database.
4) Delete an existing Database.
5) Create A new Table inside Database
6) Insert A New Row in a Table
7) Select Data from Table
=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=


1) Create Database user
• By default, will be a system user called “oracle”
(To test create a user by useradd oracle)
• If the user that run the script is “oracle” or an admin user then he can do the following:
. Will Ask you for a new admin user.
. If this user already exists MSG will appear that tells the user is already exist
. If not, the entered user will be in a file called DB_admins.db
. DB_admins.db will have a list of admin users, including oracle and other created users

2) Delete Database User
• Only users in DB_admins.db can run this script.
• The Script will show you the list of users in DB_admins.db
• If one is selected then it will be deleted from DB_admins.db
o HINT ) using sed command
• user “oracle” can’t be deleted.

3) Create new Database
• Only users in DB_admins.db can run this script.
• The script will ask you for database name
• Then A Directory is created with the entered DB name under the Following Path:
MySQL/DataBases/YOUR_NEW_DB
• A file will be in this path called owner.txt will have the user name for the user that create this database.
• The final output for this script is A directory with DataBase Name
For example) MySQL/DataBases/EmplyeeDB

4) Delete an existing Database
• Only users in DB_admins.db can run this script.
• The script will show all available created Databases inside MySQL/DataBases
• If the Database owner is the same with the user that run this script, then Database directory and it’s content be deleted.
• example) if EmplyeeDB is selected directory and it’s content be deleted.

5) Create A new Table inside Database
• Only users in DB_admins.db can run this script
• The script will show all available created Databases inside MySQL/DataBases.
• If the Database owner is the same with the user that run this script,
then will ask you for Table Name, Number of columns need to be created.
• If Table Name not already exist inside this Database then will ask you to enter the Column Names according to the entered number of columns.
• The final output for this script must create a file named with the entered Table Name
for example, MySQL/DataBases/EmplyeeDB/employee.table:
#cat employee.table
emp_id,emp_name,job_name,manager_id,hire_date
• Each Column name is separated by comma.

6) Insert A New Row in a Table
• Only users in DB_admins.db can run this script
• The script will show all available created Databases inside MySQL/DataBases to select your working database.
• If the selected Database owner is the same with the user that run this script, then will show all available tables inside this database to select from it.
• For the selected Table The script will start reading the table header then will ask you to enter these data.
• First column must be always unique
BOUNS(Optional) Read CSV file and read auto insert the matching header inside your table

7) Select Data from Table
• The script will show all available created Databases inside MySQL/DataBases to select your working database
• then will show all available tables inside this database to select from it.
• Now you will have two options:
o Show The content of the selected table will be shown by cat this table name
#cat employee.table
emp_id,emp_name,job_name,hire_year
1,Mohamed,unix admin,2021
2,Ahmed,unix admin,2016
3,Ahmed,DBA,2019
o Search inside table take a string then show you the rows that have this string.
BOUNS)

8) Delete Row from Table
• From the selected table each row the contain a specific string must be deleted
• Then show you the updated table
