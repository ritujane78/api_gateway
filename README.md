# API Gateway

## Project Overview
This is a **Gateway** for securely routing requests to APIs in the following microservices:
- **ResourceServer**
- **Photos**
- **Albums**

Authentication is handled using **OAuth2**.

This project contains basic APIs that can only be accessed by providing an **authorized access token** in the request headers.

**Keycloak** authorization server is used to:
1. Generate a token from user credentials.
2. Exchange the token for an access token.
3. Use the access token to access protected APIs.

---

## Ports
- **API Gateway:** `8084`
- **Keycloak Server:** `8081`
- **Spring Boot Resource Server:** `8082`
- **Spring Boot Photos Server:** `8090`
- **Spring Boot Albums Server:** `8091`

---

## Keycloak Server Startup
To start the Keycloak server, run:

- **Windows:**
```bash
kc.bat start-dev --http-port=8820
