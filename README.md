# JWT-Authentication-with-roles

A restful web service implementation in jersey framework with asynchronous processing. The primary objective of the project is use to authenticate the rest endpoints for a valid user with proper access token and segregate the endpoint consumer for different level of organisation people such as admin, user etc. Technology stack include Rxjava, jersey with jax-rs specification, JWT Auth for authentication and authorization. 
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

The JWT authentication and authorization has two specific components. One is for validating user request with jwt valid access token and second defined the principal roles allowed for users for each request, means endpoints has authorization valid for specific role of people in organization. ie (Admin and User of a particular company can access specific resource for which their role is defined).

For the authentication and authorization, we have to secure the endpoints with two runtime filters:
- [x] @RolesAllowed : use for specific principal roles who can only access the endpoints.
- [x] @JWTTokenNeeded : use for validating the user request with jwt access token for each endpoints. 

The rest web service has several end points:

1. The end point is used for creating user. The user can choose the roles based on their organization policy.Roles can be multiple also.
- [x] http://ipaddress:portno/jwt-authentication/api/users/create

Method: POST
Request body: 
{
    "firstName" : "Santa",
    "lastName" : "Banta",
    "emailId": "santaBanta@gmail.com",
    "password": "santa@123",
    "company": "Bantan Cloud Lending",
    "roles"		 : ["User"]
}

Response body:
{
    "success": 1,
    "message": "santaBanta@gmail.com created successfully"
}

2. After creating user, the user need to be authenticate with jwt access token for accessing end points. The access token is valid for only 30 minutes after creation time.
- [x] http://ipaddress:portno/jwt-authentication/api/authenticate

Method: POST
Request body:
{
	"username":"saha.santanu0217@gmail.com",
	"password":"santanu@123"
}

Response body:

{
    "success": 1,
    "message": "login success",
    "accessToken": "eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJzYWhhLnNhbnRhbnUwMjE3QGdtYWlsLmNvbSIsImlzcyI6Imh0dHA6Ly9qd3MtYXBwLWp3dC1hdXRoLmEzYzEuc3RhcnRlci11cy13ZXN0LTEub3BlbnNoaWZ0YXBwcy5jb20vand0LWF1dGhlbnRpY2F0aW9uL2FwaS9hdXRoZW50aWNhdGUiLCJpYXQiOjE1Mzc4MDI4NTksImV4cCI6MTUzNzgwNDY1OX0.YV2ufQDZ9vT4jOnzReiFYPC0yTRLW6QZoMvFt_XPZva1Utw7Oqq1XgSSorAXcHArGQoLGTiNnNH_vW_jtmDVNA"
}

The Jwt access token consists of 
-[x] Header: ALGORITHM & TOKEN TYPE.
-[x] Payload: DATA
-[x] Verify Signature




