
🧪 User Management REST API with Flask

This is a simple RESTful API built using Flask for managing users in-memory (without a database). The API allows you to create, read, update, and delete users via standard HTTP methods.

📁 Project Structure

RESTAPI/
├── app.py         ← Flask application
└── README.txt     ← Project documentation (this file)

🚀 How to Run the Project

1. Clone or Download

   git clone https://github.com/dipesh22104114/REST-API.git
   cd RESTAPI

2. Install Flask

   pip install flask

3. Run the Server

   python app.py

You should see:

   * Running on http://127.0.0.1:5000/

📌 Base URL

http://127.0.0.1:5000

📖 API Endpoints & Usage

1. Home Route
   - URL: /
   - Method: GET
   - Response: Welcome to the User API! Use /users endpoint.

2. Get All Users
   - URL: /users
   - Method: GET
   - Description: Retrieves all users

3. Get User by ID
   - URL: /users/<id>
   - Method: GET
   - Example: /users/1

4. Create New User
   - URL: /users
   - Method: POST
   - Body (JSON):
     {
       "id": 1,
       "name": "Alice",
       "email": "alice@example.com"
     }

5. Update User
   - URL: /users/<id>
   - Method: PUT
   - Body (JSON):
     {
       "id": 1,
       "name": "Alice Updated",
       "email": "alice_updated@example.com"
     }

6. Delete User
   - URL: /users/<id>
   - Method: DELETE
   - Example: /users/1

🧪 Test with curl (PowerShell)

Add a User:
Invoke-RestMethod -Uri http://127.0.0.1:5000/users -Method Post -Body '{"id":1,"name":"Alice","email":"alice@example.com"}' -ContentType "application/json"

Get All Users:
Invoke-RestMethod -Uri http://127.0.0.1:5000/users -Method Get

Update User:
Invoke-RestMethod -Uri http://127.0.0.1:5000/users/1 -Method Put -Body '{"id":1,"name":"Alice Updated","email":"new@example.com"}' -ContentType "application/json"

Delete User:
Invoke-RestMethod -Uri http://127.0.0.1:5000/users/1 -Method Delete

📌 Notes

- All data is stored in a Python dictionary (not persistent)
- Restarting the server clears all users
- Ideal for learning REST API fundamentals


📃 Author
Dipesh Sahani
Simple Flask project REST API with full CRUD operations.
