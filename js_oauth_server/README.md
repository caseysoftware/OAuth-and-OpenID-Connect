# Using OAuth2orize as your OAuth 2 Server 

## Configuration and Setup

0. Ensure you have npm installed
0. Run `npm install` 
0. Start the node server with `node app.js`

## Additional detail

* `http://localhost:3000/dialog/authorize` is the `authorizationURL`.
* `http://localhost:3000/oauth/token` is the `tokenURL`
* `http://localhost:3000/api/userinfo` is a protected resource that requires user permission
* `http://localhost:3000/api/clientinfo` is a protected resource that requires a token generated from the client's id and secret

## Caveats and Warnings

0. Our only users are hardcoded in `db\users.js` starting on line 3. In a real implementation, we would call a database or other user store for password verification.
0. Our only OAuth Clients are hardcoded in `db\clients.js` on line 3. In a real implementation, we would call a database or other list of OAuth clients to validate the client_id and client_secret.
0. Scopes are not implemented in this example but are available from the underlying OAuth2orize system.