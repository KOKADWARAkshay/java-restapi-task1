# java-restapi-task1

Requirements
To run this application, you need to have the following installed on your machine:

Java 8 or higher
MongoDB 3.2 or higher
Libraries
This application uses the following libraries:

Spring Boot
Spring Data MongoDB
Spring Web
Getting Started
To get started with the application, follow these steps:

Clone the repository to your local machine using Git:
bash
Copy code
git clone https://github.com/example/server-api.git
Change into the project directory:
bash
Copy code
cd server-api
Build the application using Maven:
go
Copy code
mvn clean package
Start the application:
bash
Copy code
java -jar target/server-api-1.0.0.jar
The application will now be running on http://localhost:8080.

API Endpoints
The following endpoints are available in the API:

GET servers
This endpoint returns all servers if no parameters are passed. When a server ID is passed as a parameter, it returns a single server or a 404 if there is no such server.

bash
Copy code
GET /servers
GET /servers/{id}
PUT a server
This endpoint creates a new server object. The server object is passed as a JSON-encoded message body.

bash
Copy code
PUT /servers
Example request body:

json
Copy code
{
  "name": "my centos",
  "id": "123",
  "language": "java",
  "framework": "django"
}
DELETE a server
This endpoint deletes a server object. The parameter is a server ID.

bash
Copy code
DELETE /servers/{id}
GET (find) servers by name
This endpoint searches for servers by name. The parameter is a string. It checks if a server name contains this string and returns one or more servers found. Returns 404 if nothing is found.

bash
Copy code
GET /servers?name={name}
Using Postman
You can test the API endpoints using Postman. Here are the steps:

Open Postman.
Create a new request by clicking the "New" button.
Set the request method (GET, PUT, DELETE) and URL.
Set the request headers (if required).
Set the request body (if required).
Click the "Send" button to make the request.
Using Curl
You can also test the API endpoints using Curl. Here are some examples:

bash
Copy code
# Get all servers
curl http://localhost:8080/servers

# Get a single server by ID
curl http://localhost:8080/servers/123

# Create a new server
curl -X PUT -H "Content-Type: application/json" -d '{"name": "my centos", "id": "123", "language": "java", "framework": "django"}' http://localhost:8080/servers

# Delete a server by ID
curl -X DELETE http://localhost:8080/servers/123

# Find servers by name
curl http://localhost:8080/servers?name=my







![Screenshot 2023-03-29 214236](https://user-images.githubusercontent.com/70112790/228631207-8bb14f2a-4db7-422d-839f-84f07137862a.jpg)

![WhatsApp Image 2023-03-29 at 11 38 03 PM](https://user-images.githubusercontent.com/70112790/228631266-f2f19ced-cb80-4f4a-a67d-1607b1b896d4.jpeg)
