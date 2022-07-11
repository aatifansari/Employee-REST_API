## Employee-REST_API
Springboot project to implement RESTful webservices to perform CRUD operations on employee resource using MySQL database. Hibernate used for object relation mapping and maven for build automation. Backend separated into resource, service and repository(DAO) layers.

### Application Architecture

![Application_architecture](https://user-images.githubusercontent.com/44142827/159642614-cda73fd6-9859-484e-91ef-048daca248f5.PNG)

### Project Directory

![image](https://user-images.githubusercontent.com/44142827/178201660-b4890fcf-5e05-4d56-8612-7bff05f80a34.png)


### Database Schema

![image](https://user-images.githubusercontent.com/44142827/159650837-17894a90-4c12-4efa-ba50-8418c942c6d5.png)


Employee Object fields
- id
- firstName
- lastName
- email

### APIs Description

#### 1. Add Employee

Request Method & Endpoint - POST https://{host_name}/api/employees
- addEmployee() - save new employee data into the table. Input data is passed as json in the request body

Postman Request and Response

![AddEmployeePostman](https://user-images.githubusercontent.com/44142827/178208775-931a2605-3165-4c47-884e-318ceac475b5.PNG)

Database 

![POST_Add_Employee_DB](https://user-images.githubusercontent.com/44142827/178208892-7d385344-80d0-4eaa-b741-41c00bc0bc3b.PNG)


#### 2. Get All Employees

Request Method & Endpoint - GET https://{host_name}/api/employees
- findAll() - fetch entire employee table data and return a json file

Postman Request and Response

![GetAllEmployeePostman](https://user-images.githubusercontent.com/44142827/178209087-6cdfc52a-1a96-4f60-be9c-005fc239c1d2.PNG)

Database

![GetAllEmployeeDB](https://user-images.githubusercontent.com/44142827/178209158-6009a984-9283-4669-ba97-ae445d978a02.PNG)



#### 3. Get Employee By Id

Request Method & Endpoint - GET https://{host_name}/api/employees/{employeeId}
- findById() - fetch specific employee data from table using employeeId path variable. 
Exception Handling - If employeeId does not exists in table runtime exception displaying "Employee id not found" is thrown back.

Postman Request and Response

![GetEmployeeByIdPostman](https://user-images.githubusercontent.com/44142827/178209576-3a5fe126-e03f-46fd-b8d6-63fdc4213452.PNG)


#### 4. Update Employee 

Request Method & Endpoint - PUT https://{host_name}/api/employees
- updateEmployee - update existing employee data in the table using id attribute. Input data is passed as json in the request body

Postman Request and Response

![UpdateEmployeePostman](https://user-images.githubusercontent.com/44142827/178209687-503294cb-1341-43c6-aa91-4d84f99c475e.PNG)

Database

![UpdateEmployeeDB](https://user-images.githubusercontent.com/44142827/178209871-54a17438-7ee1-4a76-92a0-ba0443dfae56.PNG)


#### 5. Delete Employee By Id

Request Method & Endpoint - DELETE  https://{host_name}/api/employees/{employeeId}
- deleteEmployee - delete specific employee data from table using employeeId path variable.
Exception Handling - If employeeId does not exists in table runtime exception displaying "Employee id not found" is thrown back.

Postman Request and Response

![DeleteEmployeePostman](https://user-images.githubusercontent.com/44142827/178209800-663e68a0-16af-4e4f-b45c-f3ddda72d3f4.PNG)

Database

![DeleteEmployeeDB](https://user-images.githubusercontent.com/44142827/178209831-f7abec0b-25fc-498e-b8e9-b7fd1f7c8d29.PNG)


### Technology Stack

- Java 17
- Framework - Springboot
- ORM - Hibernate
- RDBMS - MySQL
- Server - Embedded Tomcat Server
- Build Tool - Maven
