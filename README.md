<h3>EMPLOYEE CRUD OPERATION:</h3>
     <p>Create Employee CRUD operation and write Http based rest API's using java spring boot.</p>

<h4>HOW TO RUN THIS PROJECT?</h4>

<h4>FROM THE IDE:</h4>
<ol>
<li>Open the project in an IDE like Eclipse.</li>
<li>You can run the DBScript provided in MySQL to create database and tables with basic values. 
	(Creating database is necessary since hibernate- update option is used : "spring.jpa.hibernate.ddl-auto = update")</li>
<li>In case you do not want to run file, you can change the line "spring.jpa.hibernate.ddl-auto = update"  to  "spring.jpa.hibernate.ddl-auto = create-drop" in src/main/resources/application.properties file.</li>
<li>Check your database connection in src/main/resources/application.properties file and change if needed.</li>
<li> Go to com.employee.management</li>
<li> Right Click on class Application.</li>
<li> Hit "Run As Java Application" in the IDE.</li>
<li>Check if localhost server has started.</li>
<li>Open Postman client service on Google chrome.</li>
<li>Hit url : "http://localhost:8080/employees" and url : "http://localhost:8080/departments"</li>
	<li>Accordingly select the request method and the url as follows:</li>
</ol>
	Department:
	<ul>
		<li>GET - "http://localhost:8080/departments" - gets list of all departments</li>
		<li>GET - "http://localhost:8080/departments/{id}" - gets department with selected id</li>
		<li>POST - "http://localhost:8080/departments" - inserts into department</li>
		<li>PUT - "http://localhost:8080/departments/{id}" - updates departments with selected id</li>
		<li>DELETE - "http://localhost:8080/departments" - deletes all departments</li>
		<li>DELETE - "http://localhost:8080/departments/{id}" - deletes departments with selected id</li>
		<li>PATCH - "http://localhost:8080/departments/{id}" - patches/updates departments with selected id</li>
		</ul>
	Employee:
	<ul>
		<li>GET - "http://localhost:8080/employees" - gets list of all employees</li>
		<li>GET - "http://localhost:8080/employees/{id}" - gets employees with selected id</li>
		<li>POST - "http://localhost:8080/employees" - inserts into employees</li>
		<li>PUT - "http://localhost:8080/employees/{id}" - updates employees with selected id</li>
		<li>DELETE - "http://localhost:8080/employees" - deletes all employees</li>
		<li>DELETE - "http://localhost:8080/employees/{id}" - deletes employees with selected id</li>
		<li>PATCH - "http://localhost:8080/employees/{id}" - patches/updates employees with selected id</li>
   </ul>

<h4>ASSUMPTIONS:</h4>
<ol>
<li>DATABASE and TABLES are created in MySQL</li>
<li>DepartmentID is a foreign key in Employee table.</li>
<li> Make sure department table is populated with the department you refer for in employee.</li>
<li>While inserting employee detail through postman service: give a department id for department. </li>
</ol>
	Eg: <br>{<br>
			"employeeID": 2,<br>
			"firstName": "Muthu",<br>
			"lastName": "vignesh",<br>
                        "mobileNumber": 9360162026,<br>
			"address": "madurai",<br>
			"department": 3<br>
	     } 
    

<h4>TECHNOLOGY STACK:</h4>
<ol>
<li>Java</li>
<li>Eclipse Neon 4.6.0</li>
<li>MySQL Workbench</li>
<li>Postman for Chrome</li>
</ol>


<h4>DESIGN DISCUSSION:</h4>
<li>The employee table has a department id foreign key.</li>
<li>Department table needs to have a value existing to be referred by the employee table.</li>
<li> Get mapping will fetch the results, Post mapping will insert results, Put mapping and Patch mapping will update results, Delete mapping will delete results.</li>
<li> You will need to create database if not, change in the application.properties file.</li>


### Ease of extending the program ###
<li> You can add useraccount table and assign username and password details for the employee.</li>
<li>You can also create a system account who handles all the creation and deleting of employee and department.</li>
