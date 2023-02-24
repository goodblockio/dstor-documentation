# Obtain an Access Token

To obtain an access token, you must send a request to the dStor Developer Token endpoint. The request should include your API key and the appropriate authentication parameters.



**Note:** \


The endpoint for the <mark style="color:purple;">**Testing**</mark> environment is:&#x20;

```
https://api.testnet.dstor.cloud/v1/dev/temp-token
```

The endpoint for the <mark style="color:blue;">**Production**</mark> environment is:&#x20;

```
https://api.dstor.cloud/v1/dev/temp-token
```



To acquire a temporary token with an API key, send a `GET` request to the following endpoint:\
[https://api.dstor.cloud/v1​/dev​/temp-token](https://api.dstor.cloud/v1/docs/index.html#/Token/get\_v1\_dev\_temp\_token)

You will need to add the following as headers:

```
"api-key": "your-api-key" // required (64 characters)
"x-expiration": 1664349827 // optional, defaults to one year
```

Below are code snippets to use for the dStor <mark style="color:purple;"></mark> <mark style="color:purple;"></mark><mark style="color:purple;">**Testing**</mark> environment.
