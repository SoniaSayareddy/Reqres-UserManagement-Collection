**Kickstart API Testing with Postman**
# Reqres User Management - Postman Collection

This repository contains a Postman collection that demonstrates key API testing concepts using the [Reqres](https://reqres.in/) sample API.  
It covers CRUD operations, variables, tests, data parsing, and more — making it a great reference for learning Postman and showcasing API automation skills.

---

## 📂 Contents
- `ReqresUserManagementCollection.json` → Exported Postman collection
- (Optional) `ReqresEnvironment.json` → Postman environment file if you use variables

---

## 🚀 Features
- **CRUD Operations**: Create, Read, Update, Delete users
- **Variables**: Environment & global variables for dynamic requests
- **Tests**: Assertions for status codes, response body, headers
- **Data Parsing**: Extracting values from responses and chaining requests
- **Collection Runner**: Iterating requests with CSV/JSON data files

---

## 🛠️ Setup Instructions
1. Download the `.json` file from this repo.
2. Open Postman → Click **Import** → Select the file.
3. (Optional) Import the environment file if provided.
4. Run the collection manually or via **Collection Runner**.

---

## 🔑 API Endpoints Covered

### 1. POST /api/login
Authenticates a user and retrieves a session token.  
- **Request Body:**
  ```json
  {
    "email": "eve.holt@reqres.in",
    "password": "cityslicka"
  }
**Tests**: Extracts token from the response and saves it as an environment variable for subsequent requests.

**2. POST /api/users**
Creates a new user.

**Request Body:**
{
  "name": "morpheus",
  "job": "leader"
}
**Tests**: Extracts id from the response and stores it in userId.

**3. PUT /api/users/{{userId}}**
Updates an existing user’s details.

**Request Body:**
{
  "name": "Sonia",
  "job": "zion resident"
}
**Scripts:** Logs old vs. new values, compares payloads, and cleans up temporary variables.

**4. DELETE /api/users/{{userId}}**
Deletes a user by ID.

Method: DELETE

**Tests**: Logs and verifies the response status code.

**▶️ Running with Collection Runner**
Open the collection in Postman.
Click Run (top right).
Configure environment, iterations, and data file (CSV/JSON).
Click Start Run to execute all requests.

**🤝 Contributing**
Feel free to fork this repo, improve the collection, or add new examples.
Pull requests are welcome!
