##  Go REST API with PostgreSQL

This project provides a simple RESTful API built with Go, interacting with a PostgreSQL database.  It includes Docker Compose for easy setup and management.


**Prerequisites:**

* Go installed on your system.
* Docker and Docker Compose installed.


**Getting Started:**

1. **Clone the repository:**
   ```bash
   git clone [repository_url]
   ```

2. **Build and run the application using Docker Compose:**
   ```bash
   cd docker
   docker-compose up -d 
   ```

3. **Access the Database:** 
   You can connect to the PostgreSQL instance using your preferred database client, configured with:
   * Host: localhost
   * Port: 32300
   * Database: docker
   * User: docker
   * Password: docker


**API Endpoints:**

* **Get All Users:**
   ```
   GET /getAll
   ```

* **Create a New User:**
   ```
   POST /newUser
   ```
   Request Body (JSON):
   ```json
   {
     "name": "John",
     "surname": "Doe",
     "age": 30
   }
   ```

* **Get User by ID:**
   ```
   GET /users/{id}
   ```

* **Update User by ID:**
   ```
   PUT /users/{id}
   ```
   Request Body (JSON):
   ```json
   {
     "name": "John",
     "surname": "Doe",
     "age": 35
   }
   ```

* **Delete User by ID:**
   ```
   DELETE /users/{id} 
   ```


**Configuration:**

Database connection details can be found and modified in the `config/config.go` file.


**Built With:**

* Go
* PostgreSQL
* Docker
* Docker Compose


**License:**

This project is licensed under the MIT license. 
