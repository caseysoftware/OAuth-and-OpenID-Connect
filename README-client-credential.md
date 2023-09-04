## Session 6.3: Using the Client Credential Grant Type

### Using the Client Credential Grant Type with PHP

Before running the following command, ensure your PHP environment is configured as descibed in `php_oauth_server\README.md`. You may optionally add `| jq .` to the end of this command to pretty print the JSON response.

```
curl -X "POST" "http://localhost:4444/client_credentials.php/access_token" \
	-H "Content-Type: application/x-www-form-urlencoded" \
	-H "Accept: 1.0" \
	--data-urlencode "grant_type=client_credentials" \
	--data-urlencode "client_id=myawesomeapp" \
	--data-urlencode "client_secret=abc123" \
	--data-urlencode "scope=machine"
```

The result should be a `token_type` which is Bearer, the `expires_in` listing 3600 seconds (one hour), and the `access_token`. Copy and paste the `access_token` into jwt.io to see the decoded JWT.

### Using the Client Credential Grant Type with Auth0

Before running the following command, ensure your Auth0 environment is configured as descibed in `other_oauth_server\README.md`. 

For the Settings in this section, on your Auth0 Dashboard vist Applications > APIs, choose your API, go to the Machine to Machine Applications tab, and select your client.

```
curl -X "POST" "[YOUR DOMAIN]/oauth/token" \
	-H "Content-Type: application/x-www-form-urlencoded" \
	-H "Accept: 1.0" \
	--data-urlencode "grant_type=client_credentials" \
	--data-urlencode "client_id=[YOUR CLIENT ID]" \
	--data-urlencode "client_secret=[YOUR CLIENT SECRET]" \
	--data-urlencode "audience=linkedin-learning-api"
```
The result should be a `token_type` which is Bearer, the `expires_in` listing 86400 seconds (one day), and the `access_token`. Copy and paste the `access_token` into jwt.io to see the decoded JWT.
