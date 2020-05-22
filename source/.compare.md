---
title: API Reference

language_tabs:
- bash
- javascript
- php

includes:

search: true

toc_footers:
- <a href='http://github.com/mpociot/documentarian'>Documentation Powered by Documentarian</a>
---
<!-- START_INFO -->
# Info

Welcome to the generated API reference.

<!-- END_INFO -->

#general


<!-- START_d3239640ae5864ff035c414fc55cec07 -->
## api/member/login
> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/member/login" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/member/login"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/member/login',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/member/login`


<!-- END_d3239640ae5864ff035c414fc55cec07 -->

<!-- START_3dfd7ee9b5e95298d25bc66dc6df230a -->
## api/member/login/resend
> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/member/login/resend" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/member/login/resend"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/member/login/resend',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/member/login/resend`


<!-- END_3dfd7ee9b5e95298d25bc66dc6df230a -->

<!-- START_7f9ce7de04bf36ad95659d9492207b7f -->
## api/member/validate-login
> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/member/validate-login" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/member/validate-login"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/member/validate-login',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/member/validate-login`


<!-- END_7f9ce7de04bf36ad95659d9492207b7f -->

<!-- START_6f44038473222c8d1b00a372d018c4a3 -->
## api/member/logout
> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/member/logout" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/member/logout"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/member/logout',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/member/logout`


<!-- END_6f44038473222c8d1b00a372d018c4a3 -->

<!-- START_506a18a86f3fcc84c6a5ae4756db04bd -->
## Member views his own details

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/member/details" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/member/details"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/member/details',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/member/details`


<!-- END_506a18a86f3fcc84c6a5ae4756db04bd -->

<!-- START_128738027c92b4a3ece971441800199c -->
## Member updates his own information

> Example request:

```bash
curl -X PATCH \
    "https://parasdham.websitex.co/api/member/edit" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/member/edit"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "PATCH",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->patch(
    'https://parasdham.websitex.co/api/member/edit',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`PATCH api/member/edit`


<!-- END_128738027c92b4a3ece971441800199c -->

<!-- START_a925a8d22b3615f12fca79456d286859 -->
## Get a JWT via given credentials.

> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/auth/login" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/auth/login"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/auth/login',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/auth/login`


<!-- END_a925a8d22b3615f12fca79456d286859 -->

<!-- START_a47210337df3b4ba0df697c115ba0c1e -->
## Get the authenticated User.

> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/auth/me" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/auth/me"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/auth/me',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/auth/me`


<!-- END_a47210337df3b4ba0df697c115ba0c1e -->

<!-- START_19ff1b6f8ce19d3c444e9b518e8f7160 -->
## Log the user out (Invalidate the token).

> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/auth/logout" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/auth/logout"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/auth/logout',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/auth/logout`


<!-- END_19ff1b6f8ce19d3c444e9b518e8f7160 -->

<!-- START_2b59239cd44bb1881a9ca7965bb588e6 -->
## Send a reset link to the given user.

> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/auth/forgot-password" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/auth/forgot-password"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/auth/forgot-password',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/auth/forgot-password`


<!-- END_2b59239cd44bb1881a9ca7965bb588e6 -->

<!-- START_6bb16641f04d0d720a043916b998ae0d -->
## Display the password reset view for the given token.

If no token is present, display the link request form.

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/auth/password/reset/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/auth/password/reset/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/auth/password/reset/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET api/auth/password/reset/{token}`


<!-- END_6bb16641f04d0d720a043916b998ae0d -->

<!-- START_b24783c060b90093f81dc015cbcd068f -->
## Reset the given user&#039;s password.

> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/auth/password/reset" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/auth/password/reset"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/auth/password/reset',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/auth/password/reset`


<!-- END_b24783c060b90093f81dc015cbcd068f -->

<!-- START_cb3250c5c19304a0a3add35bed6e692f -->
## Display all without pagination

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/industries/getAll" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/industries/getAll"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/industries/getAll',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (200):

```json
[
    {
        "id": 1,
        "name": "Sipes, Huels and Kris"
    },
    {
        "id": 2,
        "name": "Kerluke-Nolan"
    },
    {
        "id": 3,
        "name": "Brekke, Kris and Marquardt"
    },
    {
        "id": 4,
        "name": "Hirthe Ltd"
    },
    {
        "id": 5,
        "name": "Fisher, Bogan and Toy"
    }
]
```

### HTTP Request
`GET api/industries/getAll`


<!-- END_cb3250c5c19304a0a3add35bed6e692f -->

<!-- START_2f54a24cef2ad26c18be041da2fa7329 -->
## Get all tags for form

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/tags/getAll" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/tags/getAll"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/tags/getAll',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (200):

```json
[
    {
        "id": 1,
        "name": "Innovative bottom-line attitude"
    },
    {
        "id": 2,
        "name": "Focused maximized challenge"
    },
    {
        "id": 3,
        "name": "Universal upward-trending complexity"
    },
    {
        "id": 4,
        "name": "Intuitive homogeneous collaboration"
    },
    {
        "id": 5,
        "name": "Managed didactic standardization"
    }
]
```

### HTTP Request
`GET api/tags/getAll`


<!-- END_2f54a24cef2ad26c18be041da2fa7329 -->

<!-- START_92d4d8dfa245a50a7143129bdf071bef -->
## api/member/store
> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/member/store" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/member/store"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/member/store',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/member/store`


<!-- END_92d4d8dfa245a50a7143129bdf071bef -->

<!-- START_bbcc142cd49fac752f86cf88014951ee -->
## Dashboard stats

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/dashboard" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/dashboard"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/dashboard',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/dashboard`


<!-- END_bbcc142cd49fac752f86cf88014951ee -->

<!-- START_9792377865465dfd12bebd73e7326925 -->
## api/search
> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/search" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/search"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/search',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/search`


<!-- END_9792377865465dfd12bebd73e7326925 -->

<!-- START_f62d434079dff3acd53aa774d160d2ad -->
## Display a listing of the resource.

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/addresses" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/addresses"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/addresses',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/addresses`


<!-- END_f62d434079dff3acd53aa774d160d2ad -->

<!-- START_25f4303d28e06d127578df97937cdb67 -->
## Display the specified resource.

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/addresses/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/addresses/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/addresses/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/addresses/{address}`


<!-- END_25f4303d28e06d127578df97937cdb67 -->

<!-- START_e5d3d7a19170fe1ef6901a6ddf8eaeae -->
## Remove the specified resource from storage.

> Example request:

```bash
curl -X DELETE \
    "https://parasdham.websitex.co/api/addresses/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/addresses/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "DELETE",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->delete(
    'https://parasdham.websitex.co/api/addresses/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`DELETE api/addresses/{address}`


<!-- END_e5d3d7a19170fe1ef6901a6ddf8eaeae -->

<!-- START_a345dcad04836b8b7c20fe7a8b2a4942 -->
## Display a listing of the resource.

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/industries" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/industries"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/industries',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/industries`


<!-- END_a345dcad04836b8b7c20fe7a8b2a4942 -->

<!-- START_5c57faa90b52dad5da0becef8f39534e -->
## Store a newly created resource in storage.

> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/industries" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/industries"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/industries',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/industries`


<!-- END_5c57faa90b52dad5da0becef8f39534e -->

<!-- START_6c59cae8552120abc23f50c64dfc650d -->
## Display the specified resource.

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/industries/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/industries/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/industries/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/industries/{industry}`


<!-- END_6c59cae8552120abc23f50c64dfc650d -->

<!-- START_7d2632452c3201f8f5ac44795e8f2c43 -->
## Update the specified resource in storage.

> Example request:

```bash
curl -X PUT \
    "https://parasdham.websitex.co/api/industries/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/industries/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "PUT",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->put(
    'https://parasdham.websitex.co/api/industries/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`PUT api/industries/{industry}`

`PATCH api/industries/{industry}`


<!-- END_7d2632452c3201f8f5ac44795e8f2c43 -->

<!-- START_ba58d0a1ec10bcae90eedcb631c821fc -->
## Remove the specified resource from storage.

> Example request:

```bash
curl -X DELETE \
    "https://parasdham.websitex.co/api/industries/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/industries/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "DELETE",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->delete(
    'https://parasdham.websitex.co/api/industries/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`DELETE api/industries/{industry}`


<!-- END_ba58d0a1ec10bcae90eedcb631c821fc -->

<!-- START_fc1e4f6a697e3c48257de845299b71d5 -->
## Display a listing of the resource.

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/users" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/users"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/users',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/users`


<!-- END_fc1e4f6a697e3c48257de845299b71d5 -->

<!-- START_12e37982cc5398c7100e59625ebb5514 -->
## Store a newly created resource in storage.

> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/users" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/users"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/users',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/users`


<!-- END_12e37982cc5398c7100e59625ebb5514 -->

<!-- START_8653614346cb0e3d444d164579a0a0a2 -->
## Display the specified resource.

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/users/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/users/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/users/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/users/{user}`


<!-- END_8653614346cb0e3d444d164579a0a0a2 -->

<!-- START_48a3115be98493a3c866eb0e23347262 -->
## Update the specified resource in storage.

> Example request:

```bash
curl -X PUT \
    "https://parasdham.websitex.co/api/users/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/users/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "PUT",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->put(
    'https://parasdham.websitex.co/api/users/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`PUT api/users/{user}`

`PATCH api/users/{user}`


<!-- END_48a3115be98493a3c866eb0e23347262 -->

<!-- START_d2db7a9fe3abd141d5adbc367a88e969 -->
## Remove the specified resource from storage.

> Example request:

```bash
curl -X DELETE \
    "https://parasdham.websitex.co/api/users/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/users/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "DELETE",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->delete(
    'https://parasdham.websitex.co/api/users/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`DELETE api/users/{user}`


<!-- END_d2db7a9fe3abd141d5adbc367a88e969 -->

<!-- START_6530efaa8e15f42f14944713771e6ae8 -->
## Get all roles

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/roles/getAll" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/roles/getAll"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/roles/getAll',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/roles/getAll`


<!-- END_6530efaa8e15f42f14944713771e6ae8 -->

<!-- START_6470e6b987921f5c45bf7a2d8e674f57 -->
## Display a listing of the resource.

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/roles" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/roles"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/roles',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/roles`


<!-- END_6470e6b987921f5c45bf7a2d8e674f57 -->

<!-- START_90c780acaefab9740431579512d07101 -->
## Store a newly created resource in storage.

> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/roles" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/roles"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/roles',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/roles`


<!-- END_90c780acaefab9740431579512d07101 -->

<!-- START_eb37fe1fa9305b4b78850dd87031670b -->
## Show the form for editing the specified resource.

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/roles/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/roles/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/roles/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/roles/{role}`


<!-- END_eb37fe1fa9305b4b78850dd87031670b -->

<!-- START_cccebfff0074c9c5f499e215eee84e86 -->
## Update the specified resource in storage.

> Example request:

```bash
curl -X PUT \
    "https://parasdham.websitex.co/api/roles/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/roles/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "PUT",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->put(
    'https://parasdham.websitex.co/api/roles/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`PUT api/roles/{role}`

`PATCH api/roles/{role}`


<!-- END_cccebfff0074c9c5f499e215eee84e86 -->

<!-- START_9aab750214722ffceebef64f24a2e175 -->
## Remove the specified resource from storage.

> Example request:

```bash
curl -X DELETE \
    "https://parasdham.websitex.co/api/roles/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/roles/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "DELETE",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->delete(
    'https://parasdham.websitex.co/api/roles/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`DELETE api/roles/{role}`


<!-- END_9aab750214722ffceebef64f24a2e175 -->

<!-- START_09aef685476adfb11849f9d8107e640a -->
## Get all permissions

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/permissions/getAll" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/permissions/getAll"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/permissions/getAll',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/permissions/getAll`


<!-- END_09aef685476adfb11849f9d8107e640a -->

<!-- START_48f3ca23d373fe3e0478ae453b3bbcad -->
## Delete associated media

> Example request:

```bash
curl -X DELETE \
    "https://parasdham.websitex.co/api/members/1/media/delete" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/members/1/media/delete"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "DELETE",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->delete(
    'https://parasdham.websitex.co/api/members/1/media/delete',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`DELETE api/members/{member}/media/delete`


<!-- END_48f3ca23d373fe3e0478ae453b3bbcad -->

<!-- START_5314ea934eb76099bbf90d72fec19548 -->
## Display a listing of unverified member.

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/members/unverified" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/members/unverified"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/members/unverified',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/members/unverified`


<!-- END_5314ea934eb76099bbf90d72fec19548 -->

<!-- START_0a11460e85473cd9a35d34a7b8f885da -->
## Member&#039;s Tag wise list

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/members/tag/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/members/tag/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/members/tag/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/members/tag/{tag}`


<!-- END_0a11460e85473cd9a35d34a7b8f885da -->

<!-- START_13a1d00de1f4bad56cb690c8a662353d -->
## Mark member as verified,
Remove unverified relation.

> Example request:

```bash
curl -X PATCH \
    "https://parasdham.websitex.co/api/members/1/mark-verified" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/members/1/mark-verified"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "PATCH",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->patch(
    'https://parasdham.websitex.co/api/members/1/mark-verified',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`PATCH api/members/{member}/mark-verified`


<!-- END_13a1d00de1f4bad56cb690c8a662353d -->

<!-- START_f70df2097618c953919af7352f6998ad -->
## api/member/{member}/attach/missions
> Example request:

```bash
curl -X PATCH \
    "https://parasdham.websitex.co/api/member/1/attach/missions" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/member/1/attach/missions"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "PATCH",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->patch(
    'https://parasdham.websitex.co/api/member/1/attach/missions',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`PATCH api/member/{member}/attach/missions`


<!-- END_f70df2097618c953919af7352f6998ad -->

<!-- START_b6eb123caf6f46590b9a5b28b66649fe -->
## api/member/{member}/detach/mission/{id}
> Example request:

```bash
curl -X PATCH \
    "https://parasdham.websitex.co/api/member/1/detach/mission/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/member/1/detach/mission/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "PATCH",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->patch(
    'https://parasdham.websitex.co/api/member/1/detach/mission/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`PATCH api/member/{member}/detach/mission/{id}`


<!-- END_b6eb123caf6f46590b9a5b28b66649fe -->

<!-- START_a5364d4ba67fe723bb5481ddd4322fd0 -->
## Display a listing of deleted resource.

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/members/destroyed" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/members/destroyed"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/members/destroyed',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/members/destroyed`


<!-- END_a5364d4ba67fe723bb5481ddd4322fd0 -->

<!-- START_585aea61b529137990dc57765c06a142 -->
## Restore Soft deleted members

> Example request:

```bash
curl -X PATCH \
    "https://parasdham.websitex.co/api/members/destroyed/1/restore" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/members/destroyed/1/restore"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "PATCH",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->patch(
    'https://parasdham.websitex.co/api/members/destroyed/1/restore',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`PATCH api/members/destroyed/{id}/restore`


<!-- END_585aea61b529137990dc57765c06a142 -->

<!-- START_943cf49269a4bcbfb6dfd33f4c34120f -->
## Restore Soft deleted members

> Example request:

```bash
curl -X DELETE \
    "https://parasdham.websitex.co/api/members/destroyed/1/ForceDelete" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/members/destroyed/1/ForceDelete"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "DELETE",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->delete(
    'https://parasdham.websitex.co/api/members/destroyed/1/ForceDelete',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`DELETE api/members/destroyed/{id}/ForceDelete`


<!-- END_943cf49269a4bcbfb6dfd33f4c34120f -->

<!-- START_5f0e132ac7607e1a433eb77ce44e300e -->
## Display a listing of the resource.

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/members" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/members"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/members',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/members`


<!-- END_5f0e132ac7607e1a433eb77ce44e300e -->

<!-- START_75784c962d9f7fdaa338f83a0a89c205 -->
## Store a newly created resource in db.

> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/members" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/members"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/members',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/members`


<!-- END_75784c962d9f7fdaa338f83a0a89c205 -->

<!-- START_1fe2fb6a23679d775d14e6a5af369123 -->
## Display the specified resource.

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/members/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/members/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/members/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/members/{member}`


<!-- END_1fe2fb6a23679d775d14e6a5af369123 -->

<!-- START_4bcd77e9f4025dae1dbfa53b635961ae -->
## Update the specified resource in storage.

> Example request:

```bash
curl -X PUT \
    "https://parasdham.websitex.co/api/members/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/members/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "PUT",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->put(
    'https://parasdham.websitex.co/api/members/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`PUT api/members/{member}`

`PATCH api/members/{member}`


<!-- END_4bcd77e9f4025dae1dbfa53b635961ae -->

<!-- START_0f0b7e3b65ad366ec2bd5ba9e210b4a4 -->
## Remove the specified resource from storage.

> Example request:

```bash
curl -X DELETE \
    "https://parasdham.websitex.co/api/members/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/members/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "DELETE",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->delete(
    'https://parasdham.websitex.co/api/members/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`DELETE api/members/{member}`


<!-- END_0f0b7e3b65ad366ec2bd5ba9e210b4a4 -->

<!-- START_dde6989ab5551d4fb09439f7cb2554c5 -->
## Display a listing of the resource.

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/tags" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/tags"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/tags',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/tags`


<!-- END_dde6989ab5551d4fb09439f7cb2554c5 -->

<!-- START_6b95d7d1e0e5c34dd24d290bc715dccb -->
## Store a newly created resource in storage.

> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/tags" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/tags"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/tags',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/tags`


<!-- END_6b95d7d1e0e5c34dd24d290bc715dccb -->

<!-- START_faf1227d26e1a9f94cda4bb6a688c251 -->
## Display the specified resource.

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/tags/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/tags/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/tags/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/tags/{tag}`


<!-- END_faf1227d26e1a9f94cda4bb6a688c251 -->

<!-- START_a4a8a57c60acc8638ef566d690878aca -->
## Update the specified resource in storage.

> Example request:

```bash
curl -X PUT \
    "https://parasdham.websitex.co/api/tags/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/tags/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "PUT",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->put(
    'https://parasdham.websitex.co/api/tags/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`PUT api/tags/{tag}`

`PATCH api/tags/{tag}`


<!-- END_a4a8a57c60acc8638ef566d690878aca -->

<!-- START_4a7e5df1eb6e21ac01a7ea9dbd9bf710 -->
## Remove the specified resource from storage.

> Example request:

```bash
curl -X DELETE \
    "https://parasdham.websitex.co/api/tags/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/tags/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "DELETE",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->delete(
    'https://parasdham.websitex.co/api/tags/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`DELETE api/tags/{tag}`


<!-- END_4a7e5df1eb6e21ac01a7ea9dbd9bf710 -->

<!-- START_c8db04f0fa377d55fd3ccd8cafc37ef5 -->
## api/mission/{mission}/detach/contact/{id}
> Example request:

```bash
curl -X PATCH \
    "https://parasdham.websitex.co/api/mission/1/detach/contact/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/mission/1/detach/contact/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "PATCH",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->patch(
    'https://parasdham.websitex.co/api/mission/1/detach/contact/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`PATCH api/mission/{mission}/detach/contact/{id}`


<!-- END_c8db04f0fa377d55fd3ccd8cafc37ef5 -->

<!-- START_2f83129ec940998544497a05d0451308 -->
## api/mission/{mission}/detach/member/{id}
> Example request:

```bash
curl -X PATCH \
    "https://parasdham.websitex.co/api/mission/1/detach/member/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/mission/1/detach/member/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "PATCH",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->patch(
    'https://parasdham.websitex.co/api/mission/1/detach/member/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`PATCH api/mission/{mission}/detach/member/{id}`


<!-- END_2f83129ec940998544497a05d0451308 -->

<!-- START_2a77fd1e5a6e1fd6633679006dc09627 -->
## api/missions/attach/members
> Example request:

```bash
curl -X PATCH \
    "https://parasdham.websitex.co/api/missions/attach/members" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/missions/attach/members"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "PATCH",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->patch(
    'https://parasdham.websitex.co/api/missions/attach/members',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`PATCH api/missions/attach/members`


<!-- END_2a77fd1e5a6e1fd6633679006dc09627 -->

<!-- START_3c2f369f1073a747d8d9655bb792359f -->
## List in a hierarchical tree view

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/missions/treeview" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/missions/treeview"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/missions/treeview',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/missions/treeview`


<!-- END_3c2f369f1073a747d8d9655bb792359f -->

<!-- START_723da4481b74eeb3bc7b67ae2e3b59cc -->
## Restructure based on new array

> Example request:

```bash
curl -X PATCH \
    "https://parasdham.websitex.co/api/missions/treeview" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/missions/treeview"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "PATCH",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->patch(
    'https://parasdham.websitex.co/api/missions/treeview',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`PATCH api/missions/treeview`


<!-- END_723da4481b74eeb3bc7b67ae2e3b59cc -->

<!-- START_0de0adddcc2d038d1d5b2610714b61b6 -->
## api/missions/getAll
> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/missions/getAll" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/missions/getAll"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/missions/getAll',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/missions/getAll`


<!-- END_0de0adddcc2d038d1d5b2610714b61b6 -->

<!-- START_06c3728b2a00dc9a99f2ec0eb08b8763 -->
## Search for member details page

> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/missions/search" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/missions/search"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/missions/search',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/missions/search`


<!-- END_06c3728b2a00dc9a99f2ec0eb08b8763 -->

<!-- START_e800217ffc20d9d43aec267623074a6a -->
## api/missions
> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/missions" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/missions"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/missions',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/missions`


<!-- END_e800217ffc20d9d43aec267623074a6a -->

<!-- START_0f8dc4f49711cd79142de64901bc1c21 -->
## api/missions
> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/missions" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/missions"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/missions',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/missions`


<!-- END_0f8dc4f49711cd79142de64901bc1c21 -->

<!-- START_e099552073676be4b0de1e996aacda78 -->
## api/missions/{mission}
> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/missions/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/missions/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/missions/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/missions/{mission}`


<!-- END_e099552073676be4b0de1e996aacda78 -->

<!-- START_b36d513567d313b7e2b332a9bbb324fa -->
## api/missions/{mission}/edit
> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/missions/1/edit" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/missions/1/edit"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/missions/1/edit',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/missions/{mission}/edit`


<!-- END_b36d513567d313b7e2b332a9bbb324fa -->

<!-- START_b7e271666213ba1607bdf6877ec9e6e5 -->
## api/missions/{mission}
> Example request:

```bash
curl -X PUT \
    "https://parasdham.websitex.co/api/missions/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/missions/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "PUT",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->put(
    'https://parasdham.websitex.co/api/missions/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`PUT api/missions/{mission}`

`PATCH api/missions/{mission}`


<!-- END_b7e271666213ba1607bdf6877ec9e6e5 -->

<!-- START_c118162ba23f33e62a6474875004ec20 -->
## api/missions/{mission}
> Example request:

```bash
curl -X DELETE \
    "https://parasdham.websitex.co/api/missions/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/missions/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "DELETE",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->delete(
    'https://parasdham.websitex.co/api/missions/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`DELETE api/missions/{mission}`


<!-- END_c118162ba23f33e62a6474875004ec20 -->

<!-- START_6cca37b385778fb1ccad1113107c7c4b -->
## api/activities/logs
> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/activities/logs" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/activities/logs"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/activities/logs',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/activities/logs`


<!-- END_6cca37b385778fb1ccad1113107c7c4b -->

<!-- START_28b9d826fca10805ad1a7ce5dc5bcb42 -->
## api/activities/user/{user}/actions
> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/activities/user/1/actions" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/activities/user/1/actions"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/activities/user/1/actions',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/activities/user/{user}/actions`


<!-- END_28b9d826fca10805ad1a7ce5dc5bcb42 -->

<!-- START_f001b611d87b746f03ea4e04e725e327 -->
## Generate reports for members

> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/reports/members" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/reports/members"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/reports/members',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/reports/members`


<!-- END_f001b611d87b746f03ea4e04e725e327 -->

<!-- START_4f2a311daf38b6cbe8c036dcbcc819e3 -->
## api/reports/format
> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/reports/format" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/reports/format"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/reports/format',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/reports/format`


<!-- END_4f2a311daf38b6cbe8c036dcbcc819e3 -->

<!-- START_a26e052b8092fdfa7f6b2645d5662adc -->
## api/reports/format/{format}
> Example request:

```bash
curl -X DELETE \
    "https://parasdham.websitex.co/api/reports/format/1" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/reports/format/1"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "DELETE",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->delete(
    'https://parasdham.websitex.co/api/reports/format/1',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`DELETE api/reports/format/{format}`


<!-- END_a26e052b8092fdfa7f6b2645d5662adc -->

<!-- START_dbaadd9afdc08fd6c1b8592009869389 -->
## Pass import file

> Example request:

```bash
curl -X POST \
    "https://parasdham.websitex.co/api/imports/create" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/imports/create"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "POST",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->post(
    'https://parasdham.websitex.co/api/imports/create',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`POST api/imports/create`


<!-- END_dbaadd9afdc08fd6c1b8592009869389 -->

<!-- START_9bf8e5b4363b8a329e4a528ede4c140e -->
## Get all valid column names for file import

> Example request:

```bash
curl -X GET \
    -G "https://parasdham.websitex.co/api/imports/get_columns" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/imports/get_columns"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "GET",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'https://parasdham.websitex.co/api/imports/get_columns',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (401):

```json
{
    "message": "Unauthenticated."
}
```

### HTTP Request
`GET api/imports/get_columns`


<!-- END_9bf8e5b4363b8a329e4a528ede4c140e -->

<!-- START_c31d7032fc341f839791e3f5b5fa887c -->
## Merge duplicate entries with member models

> Example request:

```bash
curl -X PATCH \
    "https://parasdham.websitex.co/api/imports/merge-duplicates" \
    -H "Content-Type: application/json" \
    -H "Accept: application/json"
```

```javascript
const url = new URL(
    "https://parasdham.websitex.co/api/imports/merge-duplicates"
);

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
};

fetch(url, {
    method: "PATCH",
    headers: headers,
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->patch(
    'https://parasdham.websitex.co/api/imports/merge-duplicates',
    [
        'headers' => [
            'Content-Type' => 'application/json',
            'Accept' => 'application/json',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```



### HTTP Request
`PATCH api/imports/merge-duplicates`


<!-- END_c31d7032fc341f839791e3f5b5fa887c -->


