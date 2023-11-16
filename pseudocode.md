# Workflow Management API Pseudocode

## 1. Project Controller

### 1.1 Function to Get Total Projects

- Method: GET
- API End Point: `/project/{id}/totalprojects`
- Parameters:
  - id (path)
- Response:
  - `200`: Array of ProjectDTO
  - `404`: "Service Not found"
  - `500`: "Internal Server Error"

    1. when the user hits the `/project/{id}/totalprojects` endpoint an event is started.
    2. this event triggers the correponding lambda with the request body.
    3. Lambda contains the asynchronous function with logical code for connecting to the postgresql database.
    4. we are using aws secrets manager to store our postgresql credentials.
    5. Lambda recieve postgresql credentials from aws secrets manager and connection is made to the corresponding database.
    6. lambda function takes the request from the user
    7. gets All projects from the `project` table from the database by executing the GET query.
    8. Then the connection to the database is terminated and the instance of the lambda is no longer in existence.

### 1.2 Function to Get Completed Projects

- Method: GET
- API End Point: `/project/{id}/completedprojects`
- Parameters:
  - id (path)
- Response:
  - `200`: Array of ProjectDTO
  - `404`: "Service Not found"
  - `500`: "Internal Server Error"

  1. when the user hits the `/project/{id}/completedprojects` endpoint an event is started.
    2. this event triggers the correponding lambda with the request body.
    3. Lambda contains the asynchronous function with logical code for connecting to the postgresql database.
    4. we are using aws secrets manager to store our postgresql credentials.
    5. Lambda recieve postgresql credentials from aws secrets manager and connection is made to the corresponding database.
    6. lambda function takes the request from the user
    7. gets All completed projects from the `project` table from the database by executing the GET query.
    8. Then the connection to the database is terminated and the instance of the lambda is no longer in existence.

### 1.3 Function to Get In-progress Projects

- Method: GET
- API End Point: `/project/{id}/inprogressprojects`
- Parameters:
  - id (path)/project/{id}/inprogressprojects
- Response:
  - `200`: Array of ProjectDTO
  - `404`: "Service Not found"
  - `500`: "Internal Server Error"

  1. when the user hits the `/project/{id}/inprogressprojects` endpoint an event is started.
    2. this event triggers the correponding lambda with the request body.
    3. Lambda contains the asynchronous function with logical code for connecting to the postgresql database.
    4. we are using aws secrets manager to store our postgresql credentials.
    5. Lambda recieve postgresql credentials from aws secrets manager and connection is made to the corresponding database.
    6. lambda function takes the request from the user
    7. gets All inprogress projects from the `project` table from the database by executing the GET query.
    8. Then the connection to the database is terminated and the instance of the lambda is no longer in existence.

### 1.4 Function to Get Unassigned Projects

- Method: GET
- API End Point: `/project/{id}/unassignprojects`
- Parameters:
  - id (path)
- Response:
  - `200`: Array of ProjectDTO
  - `404`: "Service Not found"
  - `500`: "Internal Server Error"

  1. when the user hits the `/project/{id}/unassignprojects` endpoint an event is started.
    2. this event triggers the correponding lambda with the request body.
    3. Lambda contains the asynchronous function with logical code for connecting to the postgresql database.
    4. we are using aws secrets manager to store our postgresql credentials.
    5. Lambda recieve postgresql credentials from aws secrets manager and connection is made to the corresponding database.
    6. lambda function takes the request from the user
    7. gets All unassigned projects from the `project` table from the database by executing the GET query.
    8. Then the connection to the database is terminated and the instance of the lambda is no longer in existence.

## 2. UseCase Controller

### 2.1 Function to Get Usecase of a Given ID

- Method: GET
- API End Point: `/usecase/{id}`
- Parameters:
  - id (path)
- Response:
  - `200`: ProjectDTO
  - `404`: "Service Not found"
  - `500`: "Internal Server Error"

    1. when the user hits the `/usecase/{id}` endpoint an event is started.
    2. this event triggers the correponding lambda with the request body.
    3. Lambda contains the asynchronous function with logical code for connecting to the postgresql database.
    4. we are using aws secrets manager to store our postgresql credentials.
    5. Lambda recieve postgresql credentials from aws secrets manager and connection is made to the corresponding database.
    6. lambda function takes the `{id}` from the user
    7. gets the details of the project from the `usecase` table in the database by executing the GET query.
    8. Then the connection to the database is terminated and the instance of the lambda is no longer in existence.

## 3. Resource Controller

### 3.1 Function to Get List of Resources

- Method: GET
- API End Point: `/resource/{id}`
- Parameters:
  - id (path)
- Response:
  - `200`: Array of ResourcesDTO
  - `404`: "Service Not found"
  - `500`: "Internal Server Error"

  1. when the user hits the `/resource/{id}` endpoint an event is started.
    2. this event triggers the correponding lambda with the request body.
    3. Lambda contains the asynchronous function with logical code for connecting to the postgresql database.
    4. we are using aws secrets manager to store our postgresql credentials.
    5. Lambda recieve postgresql credentials from aws secrets manager and connection is made to the corresponding database.
    6. lambda function takes the request from the user
    7. gets All resources from the `resource` table from the database by executing the GET query.
    8. Then the connection to the database is terminated and the instance of the lambda is no longer in existence.

### 3.2 Function to Add Resources to a Project

- Method: POST
- API End Point: `/resource/{id}`
- Parameters:
  - id (path)
- Request Body:
  - ResourcesDTO
- Response:
  - `200`: ResourcesDTO
  - `201`: ResourcesDTO
  - `404`: "Service Not found"
  - `500`: "Internal Server Error"

    1. when the user hits the `/resource/{id}` endpoint an event is started.
    2. this event triggers the correponding lambda with the request body.
    3. Lambda contains the asynchronous function with logical code for connecting to the postgresql database.
    4. we are using aws secrets manager to store our postgresql credentials.
    5. Lambda recieve postgresql credentials from aws secrets manager and connection is made to the corresponding database.
    6. lambda function takes the request object which has details of new resources from the user
    7. adds the new resource to the `resource` table in the database by executing the POST query.
    8. Then the connection to the database is terminated and the instance of the lambda is no longer in existence.
