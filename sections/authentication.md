DataRole APIs Authentication
===========================

> Whats the password?

All DataRole product API requests can be authenticated by passing access credentials.  Your access credentials consist of an *account name* and *secret key*.

DataRole API Basic Auth
-----------------------

To hit the ground running with the DataRole APIs, just use HTTP Basic Authentication by suppling your access credentials:

```shell
curl -u account:secret https://api.datarole.com/building/v2/
```


DataRole API Header Authentication
---------------------------------

DataRole allows header authentication as well:

```shell
curl -H "X-DataRole-Account: account" -H "X-DataRole-Secret: secret" https://api.datarole.com/building/v2/
```


Remember that anyone who has your access credentials can access our data from your account. To prevent unwanted charges please guard against distrubution of your access credentials.

If you feel your authentication may have been compromised, please contact us immediately to have it updated.
