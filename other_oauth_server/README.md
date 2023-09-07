# Using Auth0 as your OAuth 2 Server 

## Configuration and Setup

0. Create an Auth0 account. 
0. You will need to create at least one user so visit User Management > Users
0. Select Create User then specify your email address and a password and save. Keep this password for later.

## Setup for Authorization Code Flow

Within the Auth0 Dashboard:

0. Select Applications > Applications and choose the Default App
0. Select Settings for the values to use in most of this course
0. On the Settings tab, find the Allowed Callback URLs section and add `https://127.0.0.1`
1. Scroll to the bottom to Save Changes

## Setup for Authorization Code with PKCE

Within the Auth0 Dashboard:

0. Select Applications > Applications and choose the Default App
1. On the Settings tab, change the Application Type to "Single Page Application"
2. Also on the Settings tab, add `http://localhost:3000` to the Allowed Callback URLs, Allowed Logout URLs, and Allowed Web Origins. If you already have entries in any of those, you will have to use commas to separate them.
3. Scroll to the bottom to Save Changes

## Setup for Client Credential Flow

Within the Auth0 Dashboard:

0. Select Applications > APIs and choose Create API
0. Give the API a Name and set an Identifier and save. I chose `linkedin-learning-api` 
0. On the Machine to Machine Applications tab, scroll down to the available clients
0. Select the available client

