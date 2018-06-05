---
title: DELING API
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - javascript--nodejs: Node.JS
  - ruby: Ruby
  - python: Python
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<h1 id="DELING-API">DELING API v1.0.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

A REST API for sharing economy

Base URLs:

* <a href="http://localhost:5000/">http://localhost:5000/</a>

# Authentication

* API Key (JWT_token)
    - Parameter Name: **Authorization**, in: header. Copy 'Bearer ' + valid JWT token into field

<h1 id="DELING-API-Car">Car</h1>

## Car_GetAll

<a id="opIdCar_GetAll"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:5000//api/Car \
  -H 'Accept: application/json' \
  -H 'Authorization: API_KEY'

```

```http
GET http://localhost:5000//api/Car HTTP/1.1
Host: localhost:5000

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'http://localhost:5000//api/Car',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'Authorization':'API_KEY'

};

fetch('http://localhost:5000//api/Car',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'http://localhost:5000//api/Car',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'API_KEY'
}

r = requests.get('http://localhost:5000//api/Car', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://localhost:5000//api/Car");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://localhost:5000//api/Car", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/Car`

> Example responses

> 200 Response

```json
[
  {
    "registrationNumber": "string",
    "id": "string",
    "userToken": "string",
    "platformToken": "string",
    "transactionId": "string",
    "amount": 0.01,
    "startTime": "2018-06-05T11:07:30Z",
    "endTime": "2018-06-05T11:07:30Z",
    "paymentTime": "2018-06-05T11:07:30Z",
    "createdAt": "2018-06-05T11:07:30Z",
    "updatedAt": "2018-06-05T11:07:30Z"
  }
]
```

<h3 id="car_getall-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="car_getall-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[allOf]|false|none|none|
|» registrationNumber|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
JWT_token
</aside>

## Car_Post

<a id="opIdCar_Post"></a>

> Code samples

```shell
# You can also use wget
curl -X POST http://localhost:5000//api/Car \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: API_KEY'

```

```http
POST http://localhost:5000//api/Car HTTP/1.1
Host: localhost:5000
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'http://localhost:5000//api/Car',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "registrationNumber": "string",
  "id": "string",
  "userToken": "string",
  "platformToken": "string",
  "transactionId": "string",
  "amount": 0.01,
  "startTime": "2018-06-05T11:07:30Z",
  "endTime": "2018-06-05T11:07:30Z",
  "paymentTime": "2018-06-05T11:07:30Z",
  "createdAt": "2018-06-05T11:07:30Z",
  "updatedAt": "2018-06-05T11:07:30Z"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'API_KEY'

};

fetch('http://localhost:5000//api/Car',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'API_KEY'
}

result = RestClient.post 'http://localhost:5000//api/Car',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'API_KEY'
}

r = requests.post('http://localhost:5000//api/Car', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://localhost:5000//api/Car");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://localhost:5000//api/Car", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/Car`

> Body parameter

```json
{
  "registrationNumber": "string",
  "id": "string",
  "userToken": "string",
  "platformToken": "string",
  "transactionId": "string",
  "amount": 0.01,
  "startTime": "2018-06-05T11:07:30Z",
  "endTime": "2018-06-05T11:07:30Z",
  "paymentTime": "2018-06-05T11:07:30Z",
  "createdAt": "2018-06-05T11:07:30Z",
  "updatedAt": "2018-06-05T11:07:30Z"
}
```

<h3 id="car_post-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CarFiling](#schemacarfiling)|true|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="car_post-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
JWT_token
</aside>

## Car_GetUserFilings

<a id="opIdCar_GetUserFilings"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:5000//api/Car/user/{userId} \
  -H 'Accept: application/json' \
  -H 'Authorization: API_KEY'

```

```http
GET http://localhost:5000//api/Car/user/{userId} HTTP/1.1
Host: localhost:5000

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'http://localhost:5000//api/Car/user/{userId}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'Authorization':'API_KEY'

};

fetch('http://localhost:5000//api/Car/user/{userId}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'http://localhost:5000//api/Car/user/{userId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'API_KEY'
}

r = requests.get('http://localhost:5000//api/Car/user/{userId}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://localhost:5000//api/Car/user/{userId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://localhost:5000//api/Car/user/{userId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/Car/user/{userId}`

<h3 id="car_getuserfilings-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|userId|path|string|true|none|

> Example responses

> 200 Response

```json
[
  {
    "registrationNumber": "string",
    "id": "string",
    "userToken": "string",
    "platformToken": "string",
    "transactionId": "string",
    "amount": 0.01,
    "startTime": "2018-06-05T11:07:30Z",
    "endTime": "2018-06-05T11:07:30Z",
    "paymentTime": "2018-06-05T11:07:30Z",
    "createdAt": "2018-06-05T11:07:30Z",
    "updatedAt": "2018-06-05T11:07:30Z"
  }
]
```

<h3 id="car_getuserfilings-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="car_getuserfilings-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[allOf]|false|none|none|
|» registrationNumber|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
JWT_token
</aside>

## Car_Get

<a id="opIdCar_Get"></a>

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:5000//api/Car/{id} \
  -H 'Accept: application/json' \
  -H 'Authorization: API_KEY'

```

```http
GET http://localhost:5000//api/Car/{id} HTTP/1.1
Host: localhost:5000

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'http://localhost:5000//api/Car/{id}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'Authorization':'API_KEY'

};

fetch('http://localhost:5000//api/Car/{id}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'API_KEY'
}

result = RestClient.get 'http://localhost:5000//api/Car/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'API_KEY'
}

r = requests.get('http://localhost:5000//api/Car/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://localhost:5000//api/Car/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://localhost:5000//api/Car/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/Car/{id}`

<h3 id="car_get-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="car_get-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
JWT_token
</aside>

## Car_Put

<a id="opIdCar_Put"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT http://localhost:5000//api/Car/{id} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: API_KEY'

```

```http
PUT http://localhost:5000//api/Car/{id} HTTP/1.1
Host: localhost:5000
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'http://localhost:5000//api/Car/{id}',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "registrationNumber": "string",
  "id": "string",
  "userToken": "string",
  "platformToken": "string",
  "transactionId": "string",
  "amount": 0.01,
  "startTime": "2018-06-05T11:07:30Z",
  "endTime": "2018-06-05T11:07:30Z",
  "paymentTime": "2018-06-05T11:07:30Z",
  "createdAt": "2018-06-05T11:07:30Z",
  "updatedAt": "2018-06-05T11:07:30Z"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'API_KEY'

};

fetch('http://localhost:5000//api/Car/{id}',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'API_KEY'
}

result = RestClient.put 'http://localhost:5000//api/Car/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'API_KEY'
}

r = requests.put('http://localhost:5000//api/Car/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://localhost:5000//api/Car/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "http://localhost:5000//api/Car/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/Car/{id}`

> Body parameter

```json
{
  "registrationNumber": "string",
  "id": "string",
  "userToken": "string",
  "platformToken": "string",
  "transactionId": "string",
  "amount": 0.01,
  "startTime": "2018-06-05T11:07:30Z",
  "endTime": "2018-06-05T11:07:30Z",
  "paymentTime": "2018-06-05T11:07:30Z",
  "createdAt": "2018-06-05T11:07:30Z",
  "updatedAt": "2018-06-05T11:07:30Z"
}
```

<h3 id="car_put-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|
|body|body|[CarFiling](#schemacarfiling)|true|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="car_put-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
JWT_token
</aside>

## Car_Delete

<a id="opIdCar_Delete"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE http://localhost:5000//api/Car/{id} \
  -H 'Accept: application/json' \
  -H 'Authorization: API_KEY'

```

```http
DELETE http://localhost:5000//api/Car/{id} HTTP/1.1
Host: localhost:5000

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'Authorization':'API_KEY'

};

$.ajax({
  url: 'http://localhost:5000//api/Car/{id}',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'Authorization':'API_KEY'

};

fetch('http://localhost:5000//api/Car/{id}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'API_KEY'
}

result = RestClient.delete 'http://localhost:5000//api/Car/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'API_KEY'
}

r = requests.delete('http://localhost:5000//api/Car/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("http://localhost:5000//api/Car/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "http://localhost:5000//api/Car/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/Car/{id}`

<h3 id="car_delete-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|string|true|none|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="car_delete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
JWT_token
</aside>

# Schemas

<h2 id="tocScarfiling">CarFiling</h2>

<a id="schemacarfiling"></a>

```json
{
  "registrationNumber": "string",
  "id": "string",
  "userToken": "string",
  "platformToken": "string",
  "transactionId": "string",
  "amount": 0.01,
  "startTime": "2018-06-05T11:07:30Z",
  "endTime": "2018-06-05T11:07:30Z",
  "paymentTime": "2018-06-05T11:07:30Z",
  "createdAt": "2018-06-05T11:07:30Z",
  "updatedAt": "2018-06-05T11:07:30Z"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|registrationNumber|string|true|none|none|

<h2 id="tocSfiling">Filing</h2>

<a id="schemafiling"></a>

```json
{
  "id": "string",
  "userToken": "string",
  "platformToken": "string",
  "transactionId": "string",
  "amount": 0.01,
  "startTime": "2018-06-05T11:07:30Z",
  "endTime": "2018-06-05T11:07:30Z",
  "paymentTime": "2018-06-05T11:07:30Z",
  "createdAt": "2018-06-05T11:07:30Z",
  "updatedAt": "2018-06-05T11:07:30Z"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|false|none|none|
|userToken|string|true|none|none|
|platformToken|string|true|none|none|
|transactionId|string|true|none|none|
|amount|number(decimal)|true|none|none|
|startTime|string(date-time)|true|none|none|
|endTime|string(date-time)|true|none|none|
|paymentTime|string(date-time)|true|none|none|
|createdAt|string(date-time)|true|none|none|
|updatedAt|string(date-time)|true|none|none|

