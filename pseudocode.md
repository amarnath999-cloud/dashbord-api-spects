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

  - Call `getTotalProjects` in ProjectController with `id`
  - Return array of ProjectDTO in the response

### 1.2 Function to Get Completed Projects

- Method: GET
- API End Point: `/project/{id}/completedprojects`
- Parameters:
  - id (path)
- Response:
  - `200`: Array of ProjectDTO
  - `404`: "Service Not found"
  - `500`: "Internal Server Error"

  - Call `getCompletedProjects` in ProjectController with `id`
  - Return array of ProjectDTO in the response

### 1.3 Function to Get In-progress Projects

- Method: GET
- API End Point: `/project/{id}/inprogressprojects`
- Parameters:
  - id (path)
- Response:
  - `200`: Array of ProjectDTO
  - `404`: "Service Not found"
  - `500`: "Internal Server Error"

  - Call `getInprogressProjects` in ProjectController with `id`
  - Return array of ProjectDTO in the response

### 1.4 Function to Get Unassigned Projects

- Method: GET
- API End Point: `/project/{id}/unassignprojects`
- Parameters:
  - id (path)
- Response:
  - `200`: Array of ProjectDTO
  - `404`: "Service Not found"
  - `500`: "Internal Server Error"

  - Call `getUnassignProjects` in ProjectController with `id`
  - Return array of ProjectDTO in the response

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

  - Call `getUsecase` in UseCaseController with `id`
  - Return ProjectDTO in the response

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

  - Call `getResources` in ResourceController with `id`
  - Return array of ResourcesDTO in the response

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

  - Call `addResourcesToProject` in ResourceController with `id` and `ResourcesDTO`
  - Return ResourcesDTO in the response
