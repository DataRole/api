Properties
==========

Property records with related permit and professional data.


GET PROPERTY
------------

* `GET /property/{Id}` will return a property object with all related data.

```shell
curl -u api_token:X https://api.datarole.com/building/v1/property/1524
```

```json
{
  "data": {
    "Id": "integer",
    "Region": "string",
    "Permits": [
      {
        "Id": "integer",
        "Region": "string",
        "PermitNum": "string",
        "IssuedDate": "datetime",
        "PermitType": "string",
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
    ],
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
}
```


POST PROPERTIES
---------------

* `POST /properties` will return a collection of property objects with all related data.

```shell
curl -u api_token:X \
  -H 'Content-Type: application/json' \
  -d '{ "Region": "TX_Dallas" }' \
  https://api.datarole.com/building/v1/properties
```

```json
{
  "data":[
    {
      "Id":"integer",
      "Region":"string",
      "Permits":[
        {
          "Id":"integer",
          "Region":"string",
          "PermitNum":"string",
          "IssuedDate":"datetime",
          "PermitType":"string",
          "Professionals":[
            {
              "Id":"integer",
              "Region":"string",
              "DateModified":"datetime",
              "ContractorZip":"integer",
              "ContractorCity":"string",
              "ContractorEmail":"string",
              "ContractorPhone":"string",
              "ContractorState":"string",
              "ContractorCounty":"string",
              "ContractorLicNum":"string",
              "ContractorCountry":"string",
              "ContractorLicType":"string",
              "ContractorAddress1":"string",
              "ContractorAddress2":"string",
              "ContractorCompanyName":"string",
              "DateModifiedTimestamp":"string"
            }
          ],
          "Description":"string",
          "LastUpdated":"datetime",
          "PermitClass":"string",
          "DateModified":"datetime",
          "StatusCurrent":"string",
          "EstProjectCost":"integer",
          "IssuedDateTimestamp":"integer",
          "LastUpdatedTimestamp":"integer",
          "DateModifiedTimestamp":"integer"
        }
      ],
      "Latitude":"integer",
      "Longitude":"integer",
      "OriginalZip":"integer",
      "DateModified":"datetime",
      "OriginalCity":"string",
      "OriginalState":"string",
      "OriginalCounty":"string",
      "OriginalCountry":"string",
      "OriginalAddress1":"string",
      "OriginalAddress2":"string",
      "OriginalNeighborhood":"string",
      "DateLastModifiedTimestamp":"integer"
    }
  ]
}
```
