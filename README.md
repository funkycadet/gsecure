# GSecure 🔐

This is a backend API service in Golang that handles authorization and authentication for a web app.
The details of the web app are as follows:
- A simple web app where users in an organization can signin and list all other users in their organization
- Logging in is performed by supplying a `username, password` combination
- Note that all passwords should be hashed when stored in a database for security purposes
- For simplicity, assume that the existing users have already been registered and we are not concerned about a user registration flow here.
- The user should be logged in with a JWT token, with a one hour expiry.
- The user should be able to receive a new access token using a 'Refresh token' with a validity of 24 hours.
- The user should be able to logout as well.
- There are admin privileges assigned to a few users, which gives them the ability to add new user accounts or delete existing user accounts from their organization.
- All non-admin users should be able to see other user accounts but shouldn't be able to add/delete any user accounts.
- Note that any user shouldn't be able to view/add/delete user accounts into any other organization.

This API follows REST API conventions and covers the following functionalities:
- User Login
- User Logout
- Admin user adds a new user account (by providing the username & password)
- Admin user deletes an existing user account from their organization
- List all users in their organization

## Task Expectations

- [ ] Instructions in the README to setup the API & the relevant database
- [ ] Addition of test cases to handle the various endpoints available
- [ ] Postman/Swagger/OpenAPI spec so that the APIs can be tested
More tasks would be added to the list during the course of development
