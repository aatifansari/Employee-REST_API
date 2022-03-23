# Employee-REST_API
Springboot project to implement RESTful webservices to perform CRUD operation on MySQL database.

Application Architecture

![Application_architecture](https://user-images.githubusercontent.com/44142827/159642614-cda73fd6-9859-484e-91ef-048daca248f5.PNG)


Database Schema

![image](https://user-images.githubusercontent.com/44142827/159650837-17894a90-4c12-4efa-ba50-8418c942c6d5.png)


Employee Object fields
- id
- firstName
- lastName
- email

Endpoints and methods mapping


1. GET https://{host_name}/api/employees

- findAll() - fetch entire employee table data and return a json file

2. GET https://{host_name}/api/employees/{employeeId}

- findById() - fetch specific employee data from table using employeeId path variable. 
Exception Handling - If employeeId does not exists in table runtime exception displaying "Employee id not found" is thrown back.

3. POST https://{host_name}/api/employees

- addEmployee() - save new employee data into the table. Input data is passed as json in the request body
![json data](https://user-images.githubusercontent.com/44142827/159646748-2389e31b-8f3e-4768-a5ca-6d9826c541eb.PNG)

4. PUT https://{host_name}/api/employees

- updateEmployee - update existing employee data in the table using id attribute. Input data is passed as json in the request body
![image](https://user-images.githubusercontent.com/44142827/159649189-4d251bde-ddca-437b-bcc7-eba93c4f58f0.png)

5. DELETE  https://{host_name}/api/employees/{employeeId}

- deleteEmployee - delete specific employee data from table using employeeId path variable.
Exception Handling - If employeeId does not exists in table runtime exception displaying "Employee id not found" is thrown back.

Technology Stack

- Framework - Springboot
- ORM - Hibernate
- JSON processor - jackson-databind
- RDBMS - MySQL
- Server - Embedded Tomcat Server
- Build Automation Tool - Maven
