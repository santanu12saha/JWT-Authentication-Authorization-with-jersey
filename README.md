# JWT-Authentication-with-roles

A restful web service implementation in jersey framework with asynchronous processing. The primary objective of the project is use to authenticate the rest endpoints for a valid user with proper access token and segregate the endpoint consumer for different level of organisation people such as admin, user etc. Technology stack include Rxjava, jersey with jax-rs specification, JWT Auth for authentication and authorization. 
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

The JWT authentication and authorization has two specific components. One is for validating user request with jwt valid access token and other defined the principal roles allowed for users for each request, means some endpoints is only valid for particular people of organization. 
