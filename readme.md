# FatSecret Platform API

## Getting started

1. Ensure you have created a FatSecret Platform API account here: https://platform.fatsecret.com/api/

![FatSecret Platform API](/images/platform.png)

2. Sign into your account and navigate to "Manage API Keys" and then your application.

![Manage API Keys](/images/manage_keys.png)

3. In the "Allowed IP Addresses" section, set your desired IP Address.

4. For OAuth1.0, copy your Consumer Key and Consumer Secret into postman globals as consumer_key and consumer_secret.

5. For OAuth2.0, copy your Client ID and Client Secret into postman globals as client_id and client_secret.

![Globals](/images/globals.png)

## Using OAuth 1.0 with FatSecret Platform API in Postman:

1. Navigate to API Reference (OAuth 1.0) section in postman.

![Postman OAuth1](/images/oauth1.png)

2. Navigate to Profile - Authentication in postman and call the "Create" endpoint to create a profile and receive an oauth key and oauth secret.

3. Copy your newly created OAuth Key and OAuth Secret into postman globals as access_key and access_secret.

## Using OAuth 2.0 with FatSecret Platform API in Postman:

1. Navigate to API Reference (OAuth 2.0) section in postman.

![Postman OAuth2](/images/oauth2.png)

2. In the "Configure New Token" section ensure that the correct variables are set and click "Get New Access Token".

3. Use the newly created token.


Enjoy the API!
