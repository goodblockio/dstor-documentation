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

{% tabs %}
{% tab title="Curl" %}
{% code overflow="wrap" lineNumbers="true" %}
```shell
curl --location 'https://api.testnet.dstor.cloud/v1/dev/temp-token' \
--header 'api-key: 5xikF8a5wcJeqVrtQE8OffKvtR9qaRxPXXJAedhIiNFWJbNsGqsdPfJ5eDYY7n92' \
--header 'x-expiration: 1677336539'
```
{% endcode %}
{% endtab %}

{% tab title="Node.Js" %}
{% code overflow="wrap" lineNumbers="true" %}
```javascript
var request = require('request');
var options = {
  'method': 'GET',
  'url': 'https://api.testnet.dstor.cloud/v1/dev/temp-token',
  'headers': {
    'api-key': '5xikF8a5wcJeqVrtQE8OffKvtR9qaRxPXXJAedhIiNFWJbNsGqsdPfJ5eDYY7n92',
    'x-expiration': '1677336539'
  }
};
request(options, function (error, response) {
  if (error) throw new Error(error);
  console.log(response.body);
});

```
{% endcode %}
{% endtab %}

{% tab title="Python" %}
{% code overflow="wrap" lineNumbers="true" %}
```python
import requests

url = "https://api.testnet.dstor.cloud/v1/dev/temp-token"

payload={}
headers = {
  'api-key': '5xikF8a5wcJeqVrtQE8OffKvtR9qaRxPXXJAedhIiNFWJbNsGqsdPfJ5eDYY7n92',
  'x-expiration': '1677336539'
}

response = requests.request("GET", url, headers=headers, data=payload)

print(response.text)

```
{% endcode %}
{% endtab %}

{% tab title="Go" %}
{% code overflow="wrap" lineNumbers="true" %}
```go
package main

import (
  "fmt"
  "net/http"
  "io/ioutil"
)

func main() {

  url := "https://api.testnet.dstor.cloud/v1/dev/temp-token"
  method := "GET"

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, nil)

  if err != nil {
    fmt.Println(err)
    return
  }
  req.Header.Add("api-key", "5xikF8a5wcJeqVrtQE8OffKvtR9qaRxPXXJAedhIiNFWJbNsGqsdPfJ5eDYY7n92")
  req.Header.Add("x-expiration", "1677336539")

  res, err := client.Do(req)
  if err != nil {
    fmt.Println(err)
    return
  }
  defer res.Body.Close()

  body, err := ioutil.ReadAll(res.Body)
  if err != nil {
    fmt.Println(err)
    return
  }
  fmt.Println(string(body))
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

Below are code snippets to use for the dStor <mark style="color:blue;">**Production**</mark> environment: \


{% tabs %}
{% tab title="cURL" %}
{% code overflow="wrap" lineNumbers="true" %}
```shell
curl --location 'https://api.dstor.cloud/v1/dev/temp-token' \
--header 'api-key: 5xikF8a5wcJeqVrtQE8OffKvtR9qaRxPXXJAedhIiNFWJbNsGqsdPfJ5eDYY7n92' \
--header 'x-expiration: 1677336539'
```
{% endcode %}
{% endtab %}

{% tab title="Node.Js" %}
{% code overflow="wrap" lineNumbers="true" %}
```javascript
var request = require('request');
var options = {
  'method': 'GET',
  'url': 'https://api.dstor.cloud/v1/dev/temp-token',
  'headers': {
    'api-key': '5xikF8a5wcJeqVrtQE8OffKvtR9qaRxPXXJAedhIiNFWJbNsGqsdPfJ5eDYY7n92',
    'x-expiration': '1677336539'
  }
};
request(options, function (error, response) {
  if (error) throw new Error(error);
  console.log(response.body);
});

```
{% endcode %}
{% endtab %}

{% tab title="Python" %}
{% code overflow="wrap" lineNumbers="true" %}
```python
import requests

url = "https://api.dstor.cloud/v1/dev/temp-token"

payload={}
headers = {
  'api-key': '5xikF8a5wcJeqVrtQE8OffKvtR9qaRxPXXJAedhIiNFWJbNsGqsdPfJ5eDYY7n92',
  'x-expiration': '1677336539'
}

response = requests.request("GET", url, headers=headers, data=payload)

print(response.text)

```
{% endcode %}
{% endtab %}

{% tab title="Go" %}
{% code overflow="wrap" lineNumbers="true" %}
```go
package main

import (
  "fmt"
  "net/http"
  "io/ioutil"
)

func main() {

  url := "https://api.dstor.cloud/v1/dev/temp-token"
  method := "GET"

  client := &http.Client {
  }
  req, err := http.NewRequest(method, url, nil)

  if err != nil {
    fmt.Println(err)
    return
  }
  req.Header.Add("api-key", "5xikF8a5wcJeqVrtQE8OffKvtR9qaRxPXXJAedhIiNFWJbNsGqsdPfJ5eDYY7n92")
  req.Header.Add("x-expiration", "1677336539")

  res, err := client.Do(req)
  if err != nil {
    fmt.Println(err)
    return
  }
  defer res.Body.Close()

  body, err := ioutil.ReadAll(res.Body)
  if err != nil {
    fmt.Println(err)
    return
  }
  fmt.Println(string(body))
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

### Swagger

The parameters and responses can be found here: [https://api.testnet.dstor.cloud/v1/docs/index.html#/Token/get\_v1\_dev\_temp\_token](https://api.testnet.dstor.cloud/v1/docs/index.html#/Token/get\_v1\_dev\_temp\_token)

Your temporary access token identifies you to the api and allows you to make requests to dStor.
