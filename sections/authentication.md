DataRole APIs Authentication
===========================

> Whats the password?

All DataRole product API requests can be authenticated by passing an authentication token.

DataRole API Basic Auth
-----------------------

To hit the ground running with the DataRole APIs, just use HTTP Basic authentication by suppling your authentication token:

```shell
curl -u authentication_token:X https://api.datarole.com/building/v1/permit/1000
```

Your HTTP client software includes built-in support for HTTP Basic authentication.  Just provide your authetication token and 'X' for your password.


DataRole API Header Authentication
---------------------------------

DataRole allows header authentication:

```shell
curl -H "X-DataRole-Authentication: authentication_token" https://api.datarole.com/building/v1/permit/1000
```


DataRole API Query Authentication
---------------------------------

DataRole also allows usage of an authentication token to be appended to the query string for GET requests:

```shell
curl https://api.datarole.com/building/v1/permit/1000?token=authentication_token
```

Remember that anyone who has your authentication token can access our data from your account. To prevent unwanted charges please guard against distrubution of your authentication token.

If you feel your authentication may have been compromised, please contact us immediately to have it updated.