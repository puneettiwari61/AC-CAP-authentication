## BLOCK-writeTextAnswer

Write a detailed article here about authentication and authorization. It should include all these at minimum -

- The flow of authentication along with code samples.
- The best practices to be kept in mind while doing authentication.
- Difference between authorization and authentication.
- Difference between cookies/sessions and JWT. Write about their pros and cons as well.

# Authentication

Authentication plays a very important role in making of any web app. So, its important to understand its flow. Any loop holes in authentication process can put whole app on risk and even the company using it.

### Let's understand its flow

Getting details of user by signup/login form or from postman is not at all a big task. The challenge is to identifying user and retaining its login information.

#### Using JWT

- JSON WEB TOKEN(JWT) as the name suggests, it provides a token which we can store in client side like in local storage.

- Token consists of payload of user, in encrypted form.

- Its upto us what we want to store in payload of token, generally we store user id and the details required in client side.

- At the time of login in response from server client side receives a token and store it.

- To identify the logged in user we send token in a key called authorization of request headers and validate it at backend.

- If token is valid user is considered as logged in.

- Its really simple to logout by deleting the token from local storage.

Thats how JWT authentication process works.

#### Using session-cookies

- Unlike JWT we dont have token here, instead we keep our user details in session.

- At the time of login we put user id or any unique user information in request session.

- To identify whether user is logged in or not, we have to check if session has user id of the logged in user.

- If it has valid id of, user is considered as logged in.

- Logout can easily be done by destroying session.
  `req.session.destroy()`

### Authorization and Authentication

- Authentication means confirming your own identity, whereas authorization means being allowed access to the system.

- The process of verifying oneself is authentication.

- Authorization is a process of deciding the access of different things to different users or putting things safe by not letting them access by everyone.
