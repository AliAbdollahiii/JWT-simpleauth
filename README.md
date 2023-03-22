# JWT-simpleauth
Simple JWT-enabled authentication form 

This project involves building a secure and scalable authentication system using Flask and JSON Web Tokens (JWT). The system will allow users to create an account, log in, and access protected resources based on their authentication status.
The authentication system will consist of three main components: the Flask application, the user database, and the JWT implementation.

The Flask application will provide a user interface for registering new users, logging in existing users, and accessing protected resources. The user interface will be built using HTML, CSS, and JavaScript, and will communicate with the Flask application using HTTP requests.

The user database will store user account information, including usernames, email addresses, and hashed passwords. The database will be implemented using a relational database management system (RDBMS) like MySQL or PostgreSQL.

The JWT implementation will provide a secure and efficient way to authenticate users and manage user sessions. When a user logs in, the Flask application will generate a JWT containing the user's identity and other information, and send it to the client. The client will then include the JWT in all subsequent requests to the Flask application, allowing the application to verify the user's identity and grant access to protected resources.

# Setup
`#pip install flask`

`#pip install flask_jwt_extended`

`#pip install protected`

`#pip install flask_sqlalchemy`

`#python app.py`

# Components

`/register` > Create a user > `#curl -i -H "Content-Type: application/json" -X POST -d '{"username":"test", "password":"test"}' http://localhost:5001/register
`

`/login` > Login to the system to get a JWT > `#curl -X POST http://localhost:5001/login -H 'Content-Type: application/json' -d '{"username": "test", "password": "test"}'`

`/protected` > Use your JWT token to access to the protected resource! > `#curl -X GET http://127.0.0.1:5001/protected  -H "Authorization: Bearer <Access Token>"`


