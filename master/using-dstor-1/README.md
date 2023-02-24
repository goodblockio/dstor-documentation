---
description: dStor API access is available through Swagger.
---

# Start with the API

[You may access swagger here. ](https://api.dstor.cloud/v1/docs/index.html#/)

## Introduction to dStor API Keys

Many APIs require an API key for authentication purposes. However, sending the API key directly in API requests can be insecure as it can be intercepted by attackers. Instead, it is recommended to use an access token which can be used to authorize API requests.

The purpose of using the temporary access token model is to reduce reads to the dStor database, thereby ensuring that the system is able to remain performant even with a large number of users and dapps uploading content.

Swapping an API key for an access token is a secure way of authenticating API requests. By following the steps outlined in this documentation, you can easily obtain an access token and use it to authorize your API requests.

