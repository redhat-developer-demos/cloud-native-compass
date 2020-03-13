# Authentication

The process of verifying an identity to make sure it has the proper rights to perform actions. For microservices, OAuth2 is the preferred method of authentication. OAuth2 will generate a JSON Web Token (JWT) that is used to authenticate the user.

By using an API Gateway, authentication can be performed at a single point. The generated token is then passed along to every microservice, which in turn uses the token to determine rights of the caller. This model centralizes the authentication while distributing the access rights.

The downside of using a API Gateway to generate a JWT occurs when user rights are changed before a JWT expires, meaning the rights will not be effective until later.
