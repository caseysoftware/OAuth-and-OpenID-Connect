## Session 4.3: Using the Authorization Code Grant Type

Before using the following setup, ensure your Auth0 environment is configured as descibed in `other_oauth_server\README.md`. Because this Grant Type includes an interactive step, I recommend you use Postman or another visual client.

### Setting up Postman for Auth Code Flow using Auth0

For the Settings in this section, on your Auth0 Dashboard vist Applications > Applications and your specific application.

0. In the Postman request editor, immediately below the URL box, select Authorization.
0. For Type, select `OAuth 2.0`
0. For Auth URL, set it to your Auth0 domain (from the Settings tab) and append `/oauth/authorize`
0. For Access Token URL, use your Auth0 domain and append `/oauth/access_token`
0. For Client ID, use your Auth0 Client ID
0. For Client Secret, use your Auth0 Client Secret
0. For Scope, set `openid email`
0. Click "Get New Access Token"

If all goes well, you should see a redirect to your Auth0 login page. Log in with the credentials you created at setup and you should get back an `access_token` and `id_token`. Copy and paste either into jwt.io to see the decoded JWT.

Note: You may see an empty payload for the `access_token` which is okay. It depends on your configuration. The `id_token` will have your email information as specified by the `openid email` scopes. Change this to other OIDC scopes - like `openid profile` - to see how it changes.