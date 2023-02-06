# React and Keycloak integration

This project is a simple example of how to integrate React with Keycloak.
Keycloak is an open source identity and access management solution,
which allows you to secure your applications and services with little effort.
It makes it easy to implement a login/register flow, also with OAuth2 and OpenID Connect.

## How to run

```bash
# Install dependencies
npm install

# Start keycloak docker container
docker-compose up -d

# Configure keycloak :)

# Start React app
npm start
```

## How to configure Keycloak
- Go to http://localhost:4300 and login with admin/admin credentials 
(You can change them in [docker-compose.yml](docker-compose.yml))
- Create a new realm called `keycloack-react`.
- Create a new client called `react-client`.
- Create a new user called and then set a password for it.
- Go to `react-client` client settings and set `Valid Redirect URIs` to `http://localhost:3000/*`
- Go to `react-client` client settings and set `Web Origins` to `http://localhost:3000`
