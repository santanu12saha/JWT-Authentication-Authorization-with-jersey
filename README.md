# JWT-Authentication-with-roles

A restful web service implementation in jersey framework with asynchronous processing. The primary objective of the project is use to authenticate the rest endpoints for a valid user with proper access token and segregate the endpoint consumer for different level of organisation people such as admin, user etc. Technology stack include Rxjava, jersey with jax-rs specification, JWT Auth for authentication and authorization. 
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

The JWT authentication and authorization has two specific components. One is for validating user request with jwt valid access token and second defined the principal roles allowed for users for each request, means endpoints has authorization valid for specific role of people in organization. ie (Admin and User of a particular company can access specific resource for which their role is defined).

For the authentication and authorization, we have to secure the endpoints with two runtime filters:
- [x] @RolesAllowed : use for specific principal roles who can only access the endpoints.
- [x] @JWTTokenNeeded : use for validating the user request with jwt access token for each endpoints. 


