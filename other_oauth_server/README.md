# Using Auth0 as your OAuth 2 Server 

## Configuration and Setup

0. Create an Auth0 account. 
0. You will need to create at least one user so visit User Management > Users
0. Select Create User then specify your email address and a password and save. Keep this password for later.

## Setup for Authorization Code Flow

0. Select Applications > Applications and choose the Default App
0. Select Settings for the values to use in most of this course
0. On the Settings tab, find the Allowed Callback URLs section, add `https://127.0.0.1`, and scroll to the bottom to Save Changes

## Setup for Client Credential Flow

0. Select Applications > APIs and choose Create API
0. Give the API a Name and set an Identifier and save. I chose `linkedin-learning-api` 
0. On the Machine to Machine Applications tab, scroll down to the available clients
0. Select the available client