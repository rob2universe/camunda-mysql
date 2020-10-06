# Spring Boot Camunda with MySQL (Docker)
Simple Camunda Spring Boot project configured to connect against a MySQL database.
DB can be created and run for instance on Docker using:

**docker run --name mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=camdb -d mysql**

The database (here named camdb) will be created by the container during startup if the parameter *-e MYSQL_DATABASE* is passed in.
  
The database schema will be created automatically by Camunda during the first startup.

The web applications will be accessible on http://localhost:9090

### Essential Config
**spring.datasource.url** in
[application.yaml](src/main/resources/application.yaml)


*driverClassName....."com.mysql.cj.jdbc.Driver"* will be deducted automatically and does not have to be configured explicitly.