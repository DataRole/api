Permits
=======

Building permit records with related property and professional data.


GET PERMIT
----------

* `GET /permit/{Id}` will return a permit object with all related data.

```shell
curl -u api_token:X https://api.datarole.com/building/v1/permit/2013
```

```json
{
  "data": {
    "Id": "integer",
    "Region": "string",
    "PermitNum": "string",
    "IssuedDate": "datetime",
    "PermitType": "string",
    "Properties": [
      {
        "Id": "integer",
        "Region": "string",
        "Latitude": "integer",
        "Longitude": "integer",
        "OriginalZip": "integer",
        "DateModified": "datetime",
        "OriginalCity": "string",
        "OriginalState": "string",
        "OriginalCounty": "string",
        "OriginalCountry": "string",
        "OriginalAddress1": "string",
        "OriginalAddress2": "string",
        "OriginalNeighborhood": "string",
        "DateLastModifiedTimestamp": "integer"
      }
    ],
    "Professionals": [
      {
        "Id": "integer",
        "Region": "string",
        "DateModified": "datetime",
        "ContractorZip": "integer",
        "ContractorCity": "string",
        "ContractorEmail": "string",
        "ContractorPhone": "string",
        "ContractorState": "string",
        "ContractorCounty": "string",
        "ContractorLicNum": "string",
        "ContractorCountry": "string",
        "ContractorLicType": "string",
        "ContractorAddress1": "string",
        "ContractorAddress2": "string",
        "ContractorCompanyName": "string",
        "DateModifiedTimestamp": "string"
      }
    ],
    "Description": "string",
    "LastUpdated": "datetime",
    "PermitClass": "string",
    "DateModified": "datetime",
    "StatusCurrent": "string",
    "EstProjectCost": "integer",
    "IssuedDateTimestamp": "integer",
    "LastUpdatedTimestamp": "integer",
    "DateModifiedTimestamp": "integer"
  }
}
```


POST PERMITS
------------

* `POST /permits` will return a collection of permit objects with all related data.

```shell
curl -u api_token:X \
  -H 'Content-Type: application/json' \
  -d '{ "Region": "TX_Dallas" }' \
  https://api.datarole.com/building/v1/permits
```

```json
{
  "data": [
    {
      "Id": "integer",
      "Region": "string",
      "PermitNum": "string",
      "IssuedDate": "datetime",
      "PermitType": "string",
      "Properties": [
        {
          "Id": "integer",
          "Region": "string",
          "Latitude": "integer",
          "Longitude": "integer",
          "OriginalZip": "integer",
          "DateModified": "datetime",
          "OriginalCity": "string",
          "OriginalState": "string",
          "OriginalCounty": "string",
          "OriginalCountry": "string",
          "OriginalAddress1": "string",
          "OriginalAddress2": "string",
          "OriginalNeighborhood": "string",
          "DateLastModifiedTimestamp": "integer"
        }
      ],
      "Professionals": [
        {
          "Id": "integer",
          "Region": "string",
          "DateModified": "datetime",
          "ContractorZip": "integer",
          "ContractorCity": "string",
          "ContractorEmail": "string",
          "ContractorPhone": "string",
          "ContractorState": "string",
          "ContractorCounty": "string",
          "ContractorLicNum": "string",
          "ContractorCountry": "string",
          "ContractorLicType": "string",
          "ContractorAddress1": "string",
          "ContractorAddress2": "string",
          "ContractorCompanyName": "string",
          "DateModifiedTimestamp": "string"
        }
      ],
      "Description": "string",
      "LastUpdated": "datetime",
      "PermitClass": "string",
      "DateModified": "datetime",
      "StatusCurrent": "string",
      "EstProjectCost": "integer",
      "IssuedDateTimestamp": "integer",
      "LastUpdatedTimestamp": "integer",
      "DateModifiedTimestamp": "integer"
    }
  ]
}
```
