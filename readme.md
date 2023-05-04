# FatSecret Platform API

For detailed information on the API refer directly to the online [documentation](https://platform.fatsecret.com/api/Default.aspx?screen=rapih)

## Getting started

1. Ensure you have created a FatSecret Platform API account [here](https://platform.fatsecret.com/api/)

![FatSecret Platform API](/images/platform.png)

2. Sign into your account and navigate to "Manage API Keys" and then your application.

![Manage API Keys](/images/manage_keys.png)

3. In the "Allowed IP Addresses" section, whitelist your desired IP Address. We block requests to FatSecret API for a Key/Secret if the source IP is not white listed. Up to 15 ranges of IP addresses can be set.

4. Fork the collection: 

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/25958240-f307c228-34ed-42bb-8866-79dae97523a6?action=collection%2Ffork&collection-url=entityId%3D25958240-f307c228-34ed-42bb-8866-79dae97523a6%26entityType%3Dcollection%26workspaceId%3D97960a9b-5292-4c02-89c1-ded0c29c0641)

5. In your newly forked collection, copy your Consumer Key and Consumer Secret into the collection variables as consumer_key and consumer_secret. Copy your Client ID and Client Secret into the collection variables as client_id and client_secret.

![Variables](/images/variables.png)

## Using OAuth 1.0 with FatSecret Platform API in Postman:

1. Navigate to API Reference (OAuth 1.0) section in postman.

![Postman OAuth1](/images/oauth1.png)

2. You can now access all endpoints not marked as "Profile".

3. For access to "Profile" endpoints, Navigate to Profile - Authentication folder and call the "Create" endpoint to create a profile and receive an oauth key and oauth secret.

4. Copy your newly created OAuth Key and OAuth Secret into the collection variables as access_key and access_secret.

## Using OAuth 2.0 with FatSecret Platform API in Postman:

1. Navigate to API Reference (OAuth 2.0) section in postman.

![Postman OAuth2](/images/oauth2.png)

2. In the "Configure New Token" section ensure that the correct variables are set and click "Get New Access Token".

3. Use the newly created token.

## Using 3-Legged OAuth with FatSecret Platform API in Postman:

1. Navigate to 3-Legged OAuth section in postman.

![3-Legged OAuth](/images/leg.png)

2. Use the "Request Token" endpoint to request a new oauth token and oauth secret

3. Copy the oauth_token received into the request_token query parameter of the "Authorize" endpoint. Then authorize the oauth token with the auth server.

4. Use the "Access Token" endpoint to get the access token and access secret.

5. Copy the access token and access secret to the access_token and access_secret collection variables.

6. You can now access endpoints in the OAuth1.0 section.

Enjoy the API!
