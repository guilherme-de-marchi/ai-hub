# ai-hub
It's a personal project where i plan to develop an website where i'll disponibilize access to interact with n AI models. The models will be running on microservices, and the api will communicate with them through gRPC.

## Services layout

```
+- API
    |
    +- Authenticator
    |    |
    |    +- Storage
    |
    +- AI Model A
```

## Descriptions

### API server description 

This server will handle all the requests sent to interact with the AI models availabe, and also provide the web content to browser users. 

### Authenticator service description

This service will receive requests from the API server regarding to authentication and permissions of users, and communicate with the 'Database' service.

### Storage service description

This service will provide a series of functions for other services to interact with storage servers (mongoDB, redis, ...).

### AI Model A service description

By now, this service is just a placeholder to indicate that there'll be N AI models availabe for users to interact. 

## Endpoints

These are lists with no description of the public and private availabe endpoints of each program. For a more precise description of endpoints, access the ENDPOINTS.md file inside the folder of a specific program.

### API server endpoints

#### Web content
- /home
- /auth
- /model/{modelName}

#### Auth service
- POST /api/auth
- POST /api/auth/refresh
- POST /api/auth/logout

#### AI model services
- POST /api/model/{modelName}
- GET /api/model/{modelName}

### Authenticator service endpoints

- userExists
- userPasswordMatch
- createUser
- getUserSession
- createUserSession
- deleteUserSession

### Storage service endpoints

#### (Redis, ...)
- getSession
- createSession
- deleteSession
- updateSession

#### (MongoDB, ...)
- getUser
- createUser
- deleteUser
- updateUser
