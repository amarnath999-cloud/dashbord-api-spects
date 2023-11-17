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

 1. Request is passed to the API
 2. Lambda is triggered with the request
 3. There is GET method is defined inside the Lambda.
 4. Lambda executes GET sql query.
 5. Total projects are listed.

### 1.2 Function to Get Completed Projects

- Method: GET
- API End Point: `/project/{id}/completedprojects`
- Parameters:
  - id (path)
- Response:
  - `200`: Array of ProjectDTO
  - `404`: "Service Not found"
  - `500`: "Internal Server Error"

 1. Request is passed to the API
 2. Lambda is triggered with the request
 3. There is GET method is defined inside the Lambda.
 4. Lambda executes GET sql query.
 5. Completed projects are listed.

### 1.3 Function to Get In-progress Projects

- Method: GET
- API End Point: `/project/{id}/inprogressprojects`
- Parameters:
  - id (path)/project/{id}/inprogressprojects
- Response:
  - `200`: Array of ProjectDTO
  - `404`: "Service Not found"
  - `500`: "Internal Server Error"

 1. Request is passed to the API
 2. Lambda is triggered with the request
 3. There is GET method is defined inside the Lambda.
 4. Lambda executes GET sql query.
 5. Inprogress projects are listed.

### 1.4 Function to Get Unassigned Projects

- Method: GET
- API End Point: `/project/{id}/unassignprojects`
- Parameters:
  - id (path)
- Response:
  - `200`: Array of ProjectDTO
  - `404`: "Service Not found"
  - `500`: "Internal Server Error"

 1. Request is passed to the API
 2. Lambda is triggered with the request
 3. There is GET method is defined inside the Lambda.
 4. Lambda executes GET sql query.
 5. Unassign projects are listed.

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

 1. Request is passed to the API
 2. Lambda is triggered with the request
 3. There is GET method is defined inside the Lambda.
 4. Lambda executes GET sql query.
 5. Details of particular usecase is displayed.

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

 1. Request is passed to the API
 2. Lambda is triggered with the request
 3. There is GET method is defined inside the Lambda.
 4. Lambda executes GET sql query.
 5. Total resources are listed.

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

 1. Request is passed to the API
 2. Lambda is triggered with the request
 3. There is POST method is defined inside the Lambda.
 4. Lambda executes POST sql query.
 5. New resource is inserted in the resource table.
