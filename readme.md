# fatsecret Platform API

For detailed information on the API refer directly to the online [documentation](https://platform.fatsecret.com/api/Default.aspx?screen=rapih)

## Getting started

1. Ensure you have created a fatsecret Platform API account [here](https://platform.fatsecret.com/api/) and sign in.

![fatsecret Platform API](/images/platform.png)

2. Navigate to "Generate / View API Keys".

![Login Menu](/images/login_menu.png)

3. Navigate to "IP Restrictions".

![Manage API Keys](/images/view_api_keys.png)

<<<<<<< HEAD
4. In the "IP Restrictions" section, whitelist your desired IP Address. We block requests to fatsecret API for OAuth2.0 for a Key/Secret if the source IP is not white listed. Up to 15 ranges of IP addresses can be whitelisted.
=======
4. In the "IP Restrictions" section, whitelist your desired IP Address. We block requests to FatSecret API for OAuth2.0 for a Key/Secret if the source IP is not white listed. Up to 15 IP addresses can be whitelisted. Up to 15 IP address ***ranges*** can be whitelisted for premier users.
>>>>>>> 9a99d8403dbd6f2867ca3316b5374f748c07830e

![IP Whitelist](/images/ip_whitelist.png)

5. Now head to Postman and fork the collection by clicking the "Run in Postman" button:

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/25958240-f307c228-34ed-42bb-8866-79dae97523a6?action=collection%2Ffork&collection-url=entityId%3D25958240-f307c228-34ed-42bb-8866-79dae97523a6%26entityType%3Dcollection%26workspaceId%3D97960a9b-5292-4c02-89c1-ded0c29c0641)

6. In your newly forked collection, copy your Consumer Key and Consumer Secret into the collection variables as consumer_key and consumer_secret. Copy your Client ID and Client Secret into the collection variables as client_id and client_secret.

![Variables](/images/variables.png)

## Using OAuth 1.0 with fatsecret Platform API in Postman:

1. Navigate to API Reference (OAuth 1.0) section in postman.

![Postman OAuth1](/images/oauth1.png)

2. You can now access all endpoints not marked as "Profile".

3. For access to "Profile" endpoints, Navigate to Profile - Authentication folder and call the "Create" endpoint to create a profile and receive an oauth key and oauth secret.

4. Copy your newly created OAuth Key and OAuth Secret into the collection variables as `access_key` and `access_secret`.

## Using OAuth 2.0 with fatsecret Platform API in Postman:

1. Navigate to API Reference (OAuth 2.0) section in postman.

![Postman OAuth2](/images/oauth2.png)

2. In the "Configure New Token" section ensure that the correct variables are set and click "Get New Access Token".

3. Use the newly created token.

## Using 3-Legged OAuth with fatsecret Platform API in Postman:

1. Navigate to 3-Legged OAuth section in postman.

![3-Legged OAuth](/images/leg.png)

2. Use the "Request Token" endpoint to request a new oauth token and oauth secret

3. Copy the `oauth_token` and `oauth_secret` received into the collection variables.

4. Use the "Authorize" endpoint to authorize the `oauth_token` received. You will need to log in to your fatsecret account to do this. A link should return the verifier value, copy this into the collection variable `oauth_verifier`.

NOTE: You may need to send the authorize request using a browser in order to login and open the callback url response.

6. Finally, Use the "Access Token" endpoint to get the access token and access secret.

7. Copy the received oauth token and oauth token secret from the "Request Token" end point to the `access_token` and `access_secret` collection variables.

8. You can now access endpoints in the OAuth1.0 section.

Enjoy the API!
