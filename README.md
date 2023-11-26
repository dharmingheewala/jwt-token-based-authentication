# jwt-token-based-authentication

This is a basic implementation of JWT token-based authentication in a .NET Core Web API. The authentication is achieved using the `Microsoft.AspNetCore.Authentication.JwtBearer` package for handling JWT tokens and `Microsoft.IdentityModel.Tokens` for token validation.

## Prerequisites

- [.NET Core SDK 8.0](https://dotnet.microsoft.com/download/dotnet-core/3.1)
- Your favorite code editor (e.g., Visual Studio, Visual Studio Code)

## Getting Started

1. Clone this repository:
   ```bash
   git clone https://github.com/dharmingheewala/jwt-token-based-authentication.git jwt-token-based-authentication
   cd jwt-token-based-authentication
2. Open the project in your preferred code editor.
3. Configure JWT settings in appsettings.json: Update JWT settings in appsettings.json with your secret key, issuer, audience, and other relevant information.
4. Build and Run:
	```bash
	dotnet build
	dotnet run
The API should now be running at http://localhost:5093 (or another port if specified).

## Usage

1. Obtaining a JWT Token: Make a POST request to the /api/AutheticateUser endpoint with valid credentials in the request body.

```
POST http://localhost:5093/api/AuthenticateUser
Content-Type: application/json

{
  "username": "your-username",
  "password": "your-password"
}
```

If the credentials are valid, the response will include a JWT token.

## Dependencies

	Microsoft.AspNetCore.Authentication.JwtBearer
	Microsoft.IdentityModel.Tokens
