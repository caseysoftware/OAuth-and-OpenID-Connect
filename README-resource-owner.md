## Session 5.3: Using the Resource Owner Password Grant Type

### Using the Resource Owner Password Grant Type with PHP

Before running the following command, ensure your PHP environment is configured as descibed in `php_oauth_server\README.md`. You may optionally add `| jq .` to the end of this command to pretty print the JSON response.

```
curl -X "POST" "http://localhost:4444/password.php/access_token" \
	-H "Content-Type: application/x-www-form-urlencoded" \
	-H "Accept: 1.0" \
	--data-urlencode "grant_type=password" \
	--data-urlencode "client_id=myawesomeapp" \
	--data-urlencode "client_secret=abc123" \
	--data-urlencode "username=linkedin" \
	--data-urlencode "password=learning" \
	--data-urlencode "scope=basic email"
```

The result should be a `token_type` which is Bearer, the `expires_in` listing 3600 seconds (one hour), the `access_token`, and the `refresh_token`. Copy and paste the `access_token` into jwt.io to see the decoded JWT.

### Using the Resource Owner Password Grant Type with Javascript

Before running the following command, ensure your node environment is configured as descibed in `js_oauth_server\README.md`. You may optionally add `| jq .` to the end of this command to pretty print the JSON response.

```
curl -X "POST" "http://localhost:3000/oauth/token" \
	-H "Content-Type: application/x-www-form-urlencoded" \
	-H "Accept: 1.0" \
	--data-urlencode "grant_type=password" \
	--data-urlencode "client_id=abc123" \
	--data-urlencode "client_secret=ssh-secret" \
	--data-urlencode "username=bob" \
	--data-urlencode "password=secret"
```

The result should be a `token_type` which is Bearer, an `access_token`, and the `refresh_token`. In this case, the access token is opaque and therefore can not be decoded with jwt.io