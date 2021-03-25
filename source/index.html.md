---
title: PODFather API v1.1.0
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="podfather-api">PODFather API v1.1.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

The PODFather API connects you to the data you need to create jobs in the [PODFather](https://thepodfather.com) system.<br><br>The API also allows you to check the state of various resources within the system, such as customers/sites/drivers. See the list on the left for the available API endpoints, and the code on the right for some examples on how to use them.<br><br>If you have any questions, or ideas - contact your account manager and they'll be able to assist you with your enquiry.

Base URLs:

* <a href="https://external-api.aws.thepodfather.com/">https://external-api.aws.thepodfather.com/</a>

Email: <a href="mailto:helpdesk@podfather.com">Support</a> 

<h1 id="podfather-api-default">Default</h1>

## post__sample

> Code samples

```shell
# You can also use wget
curl -X POST https://external-api.aws.thepodfather.com/sample \
  -H 'Content-Type: application/json'

```

```http
POST https://external-api.aws.thepodfather.com/sample HTTP/1.1
Host: external-api.aws.thepodfather.com
Content-Type: application/json

```

```javascript
const inputBody = '{
  "alpha": "string",
  "bravo": "string"
}';
const headers = {
  'Content-Type':'application/json'
};

fetch('https://external-api.aws.thepodfather.com/sample',
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
  'Content-Type' => 'application/json'
}

result = RestClient.post 'https://external-api.aws.thepodfather.com/sample',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.post('https://external-api.aws.thepodfather.com/sample', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://external-api.aws.thepodfather.com/sample', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://external-api.aws.thepodfather.com/sample");
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
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://external-api.aws.thepodfather.com/sample", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /sample`

*Create sample*

> Body parameter

```json
{
  "alpha": "string",
  "bravo": "string"
}
```

<h3 id="post__sample-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|Schema to create a sample|
|» name|body|string|true|none|
|» *anonymous*|body|object|false|none|
|»» alpha|body|string|false|none|
|»» bravo|body|string|false|none|
|» *anonymous*|body|object|false|none|
|»» charlie|body|string|false|none|
|»» delta|body|string|false|none|

<h3 id="post__sample-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
None
</aside>

