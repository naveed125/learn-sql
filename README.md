# Learn SQL
This repo makes it easy to setup a learning environment for SQL by using MySQL docker image. The connection information is in docker-compose.yml. MySQL sample database provided by [MySQL Tutorial](https://www.mysqltutorial.org/mysql-sample-database.aspx) website.

# Setup
Use the following command to setup and start the local MySQL Database Server

```
% docker compose up -d --force-recreate
```

# Test local database
Use the included [Adminer](http://localhost:8080) web server to connect to local database. Remember to use the following username and password to connect to the database:
```
User: user
Password: user
Database: test
```

# Load Test Data
Use the [Import](http://localhost:8080/?server=db&username=user&db=test&import=) option in Adminer to load the sample database. Use the included `sample-database.sql` file. Once loaded try running a SQL by using the [SQL Command](http://localhost:8080/?server=db&username=user&db=test&sql=) window, for example:

```
select * from orders where status = 'Resolved';
```