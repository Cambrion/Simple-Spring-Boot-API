# Simple-Spring-Boot-API
Simple Spring boot API with basic security linked to MySQL database.


# Database
Roles are initialised with two basic roles:
- USER (Limited permissions)
- ADMIN (All access permission)

Roles migration file can be found at: src/main/resources/db/migration/V1.01_init_roles.sql

# Endpoints
- localhost:5500/api/auth/register  (POST)
Example body:
```
{
	"firstName": "John",
	"lastName": "Doe",
	"username": "johndoe",
	"email": "johndoe@test.com",
	"password": "123456"
}
```
Example Response:
```
{
    "success": true,
    "message": "User registered successfully"
}
```

- localhost:5500/api/auth/login     (POST)
Example body:
```
{
	"usernameOrEmail": "testusername",
	"password": "123456"
}
```
Example Response:
```
{
    "accessToken": "eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiIyIiwiaWF0IjoxNTQ4MDE4OTEyLCJleHAiOjE1NDg2MjM3MTJ9.JafFrznRzInlNWh6hLILyD3pvPXSRq862vVHKaq5ATwP6wGF_S-pS9RuZ2XwZKATlwDeEIlMzHfcLLusdHSriQ",
    "tokenType": "Bearer"
}
```
