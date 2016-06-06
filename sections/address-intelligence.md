DataRole Address Intelligence API
====================

This is a RESTful API that uses JSON for serialization and API tokens for authentication.


REST
----

We do our best to have all our URLs be [RESTful](http://en.wikipedia.org/wiki/Representational_state_transfer). Every endpoint (URL) may support one of four different http verbs. GET requests fetch information about a single object, POST requests create a new object, PUT requests update an existing object, and finally DELETE requests will remove an existing object.

To enable improved searching capability some endpoints will allow POST requests to fetch information utilizing advanced queries. 


No XML, Just JSON
-----------------

We only support [JSON](https://en.wikipedia.org/wiki/JSON) for serialization of data. Our response format has no root element and we use lowercase formatting to describe attribute keys (except for the data attributes themselves, which are [CamelCase](https://en.wikipedia.org/wiki/CamelCase)). 

This means that you have to send `Content-Type: application/json; charset=utf-8` when you're POSTing or PUTing data to DataRole.


Authentication
--------------

Please ensure you're making a private (server-side) integration with DataRole for your authentication to guard against  your API token being compromised. You can use HTTP Basic authentication, query or header authentication. This is secure since all requests in the DataRole APIs use SSL.

We suggest you do not implement public (client-side) integrations with DataRole as this will compromise your API token.

Read the [authentication guide](https://github.com/DataRole/api/blob/master/sections/authentication.md) to get started.


Rate limiting
-------------

Be nice. If you're sending too many requests too quickly, we'll send back a [429 Too Many Requests](http://tools.ietf.org/html/draft-nottingham-http-new-status-02#section-4) response for subsequent requests. Check the `Retry-After` header to see how many seconds to wait before retrying the request.

Your limits will be based upon predetermined usage quotas for your tier of service. 


Making a request
----------------

All URLs start with `https://api.datarole.com/building/v1/`  **for security purposes all endpoints are only accessible via https**. 

The path is prefixed with the product and the API version. If we change the API in backward-incompatible ways, we will incremement the version number and maintain stable support for the old URLs.

To make a request for a dataset, you need to append the dataset's index and the dataset id to the path to form something like https://api.datarole.com/building/v1/permit/1000. In curl, that looks like:

```shell
curl -u api_token:X https://api.datarole.com/building/v1/permit/1000
```

To conduct a more advanced search for data, it's the same concept except you have to use the plural for the dataset and include the `Content-Type` header, as well as, the JSON search data:

```shell
curl -u api_token:X \
  -H 'Content-Type: application/json' \
  -d '{ "Region": "TX_Dallas" }' \
  https://api.datarole.com/building/v1/permits
```

That's all!


Response Structure
------------------

Every response is wrapped in an envelope. That is, each response has a predictable set of keys with which you can expect to interact:

```json
{
    "response": { },
    "meta": { },
    "pagination": { },
    "data": { }
}
```


Handling Errors
---------------

If DataRole is having trouble, you might see a 5xx error. `500` means that the app is entirely down, but you might also see `502 Bad Gateway`, `503 Service Unavailable`, or `504 Gateway Timeout`. It's your responsibility in all of these cases to retry your request later. 

The *response* attribute is used to communicate extra information about the response to the developer. If all goes well, you should only ever see a *response code* of 200.  However, sometimes things do go wrong, and in that case you might see a response like:

```json
{
    "response": {
        "code": 401,
        "error": "Unauthorized",
        "message": "You do not have access to this resource."
    }
}
```


Meta
----
This *meta* attribute is used to communicate additional information about the request.  Please see below for an example:

```json
{
    "meta": {
        "datatype": "permit",
        "datetime": {
            "date": "2016-03-24 10:16:54.000000",
            "timezone_type": 3,
            "timezone": "America/Chicago"
        },
        "request": {
            "Region": "TX_Dallas"
        }
    }
}
```


Pagination
----------

Sometimes you just want more. For this reason, we've provided a convenient way to access more data from any request for sequential data. Simply call the url in the *next* parameter and we'll respond with the next set of data.

```json
{
    "pagination": {
        "next": "https://api.datarole.com/building/v1/permits/25/1000",
        "limit": 25,
        "offset": "1000"
    }
}
```


Data
----
The data key is the meat of the response. It may be a single model, dictionary or collection of models; either way this is where you'll find the information that you requested.  Please see the **Available Datasets** section for more details.


Available Datasets
------------------

* [Permits](https://github.com/DataRole/api/blob/master/sections/permits.md)
* [Properties](https://github.com/DataRole/api/blob/master/sections/properties.md)
* [Professionals](https://github.com/DataRole/api/blob/master/sections/professionals.md)

API Software Development Kits
-----------------------------

* [Official DataRole Address Intelligence PHP SDK](https://github.com/datarole/api-client-php)
* More coming soon!

Help us make it better
----------------------

Please tell us how we can make the API better. If you have a specific feature request or if you found a bug, please use GitHub issues. Fork these docs and send a pull request with improvements.

To talk with us and other developers about the API, [post a question on StackOverflow](http://stackoverflow.com/questions/ask) tagged `datarole-address-intelligence`.
