
# Basic CRUD: Flask & PostgreSQL

# Check 7. [RESUME]

1. Activate __PostgreSQL__ server:
    
    ```bash
    $ cd C:\Program Files\PostgreSQL\10\bin
    $ psql -U postgres
      Password for user postgres: <insert password here>
    ```

#

2. Create a database on PostgreSQL, my database name is __"EmployeeDB"__:
    
    ```bash
    postgres=#  CREATE DATABASE EmployeeDB
    postgres=#  \l 
    postgres=#  \c EmployeeDB
    ``` 

#

3. Create a __"users"__ table on __"EmployeeDB"__ database:
    
    ```bash
    EmployeeDB=#  CREATE TABLE users(
                 id SERIAL PRIMARY KEY,
                 name VARCHAR(255),
                 age VARCAR(255)
                 );
    EmployeeDB=#  \d
    ``` 

#

4. Clone this repo. Insert your database URI to __database.yaml__ file, then install all the packages needed. In this project I'm using __flask__, __flask_cors__, __flask_mysqldb__, __Flask-SQLAlchemy__ & __psycopg2__:
    ```bash
    $ git clone ..
    $ cd CRUD_Flask_PostgreSQL
    $ pip install flask flask_cors Flask-SQLAlchemy psycopg2
    ```

#

5. Run the server file. Make sure your PostgreSQL server is still running. Your application server will run locally at __*http://localhost:5000/*__ :
    ```bash
    $ python app.py
    ```

#

6. Give a request to the server. You can use __Postman__ app or Thunder_VSC:
    
    __See the opening screen (*home.html*)__
    ```bash
    GET /
    ```

    __Post a data to database:__ 
    ```bash
    POST /data
    body request: {name:"x", age:"y"}
    ```
    __Get all data & specific data by id:__
    ```bash
    GET /data
    GET /data/{:id}
    ```
    __Update a data by id__:
    ```bash
    PUT /data/{:id}
    body request: {name:"x", age:"y"}
    ```
    __Delete a data by id:__
    ```bash
    DELETE /data/{:id}
    ```

7. [RESUME]
7.1. Activate PostgreSQL server:
    $ cd C:\Program Files\PostgreSQL\10\bin
    $ psql -U postgres
      Password for user postgres: 12345

7.2. Create 'EmployeeDB' database:
    postgres=#  CREATE DATABASE lin_flask;
    postgres=#  \l 
    postgres=#  \c lin_flask

7.3. Create 'users' table on 'lin_flask' database:
    lin_flask=#  CREATE TABLE users(
                 id SERIAL PRIMARY KEY,
                 name VARCHAR(255),
                 age VARCHAR(255)
                 );
    lin_flask=#  \d

7.4. run server
    $ python app.py    

