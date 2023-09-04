# PHP OAuth 2 Server 

## Configuration and Setup

0. Ensure you have PHP 8+ installed
0. Ensure you have Composer installed from https://getcomposer.org/
0. Run `composer install` (or your equivalent) in this directory to install dependencies
0. Create a private key `openssl genrsa -out private.key 2048`
0. Create a public key `openssl rsa -in private.key -pubout > public.key`
0. `cd` into the public directory
0. Start the PHP server with `php -S localhost:4444`

## Caveats and Warnings

0. Our only user is hardcoded in `examples\Repositories\UserRepository.php` on line 27. In a real implementation, that method would call a database or other user store for password verification.
0. Our only OAuth Client is hardcoded in `examples\Repositories\ClientRepository.php` on line 42. In a real implementation, that method would call a database or other list of OAuth clients to validate the client_id and client_secret.
0. Our allowed scopes are hardcoded in `examples\Repositories\ScopeRepository.php` starting on line 21. In a real implementation, that method would call a database or other list of scopes to grant.
