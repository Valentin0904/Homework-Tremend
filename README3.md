1) "docker run --name mysql-container-new -e MYSQL_ROOT_PASSWORD=tremend -d mysql:latest" - the "docker run" command was used to create and start a Docker container named "mysql-container-new"
using the MySQL "latest" image.

 "docker exec -it mysql-container-new mysql -uroot -ptremend": This command is used to enterthe Docker container where the MySQL server is running. It allows executing MySQL commands
from the terminal.

 "CREATE DATABASE" company;: This MySQL command is used to create a new database named "company".

2)" Get-Content "C:\Users\valii\Desktop\Useful-Resources\3-database\company.sql" | docker exec -i mysql-container  mysql -uroot -ptremend company"  
This command is used to import an SQL file into the "company" database within the Docker container.
Initially, the command didn't work because line 53 was wrong as it should have been an INT and I had a string 'Consulting' in the code. So, I replaced it with the number 4

3) "CREATE USER 'new_user'@'%' IDENTIFIED BY 'password';" : This command is used to create a new MySQL user with the name "new_user" and the specified password.
"GRANT ALL PRIVILEGES ON company.* TO 'new_user'@'%';" : This command is used to grant all privileges for the "company" database to the user "new_user".
"FLUSH PRIVILEGES;": This command is used to reload privileges and apply them immediately.

4) "USE company;": This command is used to select the "company" database for executing subsequent commands.
"SELECT department, AVG(salary) AS average_salary FROM employees GROUP BY department;": This command is used to calculate the average salary for each department from the "employees"
table in the "company" database.
