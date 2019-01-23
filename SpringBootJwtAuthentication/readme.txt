Step 1: Install the db script(tables.sql available in resources folder).

Step 2: Build the project and run the application.
Step 3: Test using below steps.
	Signup:
		uri: http://localhost:8080/api/auth/signup
		Method: POST
		Object:    {
						"name": "User",
						"username":"userone",
						"email":"useradmin@spring.com",
						"role": ["user","pm"],
						"password":"123456"
					}
	Login:
		uri: http://localhost:8080/api/auth/signin
		Method: POST
		Object:    {
						"username":"userone",
						"password":"123456"
					}
	
	User:
		uri: http://localhost:8080/api/test/user
		Method: GET
		Headers:
			Authorization: Bearer  <jwt token>
		