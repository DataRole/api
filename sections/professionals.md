Professionals
=============

Professional records with related permit and property data.


GET PROFESSIONAL
------------

* `GET /professional/{Id}` will return a professional object with all related data.

```shell
curl -u api_token:X https://api.datarole.com/building/v1/professional/1052
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
}
```


POST PROFESSIONALS
---------------

* `POST /professionals` will return a collection of professional objects with all related data.

```shell
curl -u api_token:X \
  -H 'Content-Type: application/json' \
  -d '{ "Region": "TX_Dallas" }' \
  https://api.datarole.com/building/v1/professionals
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
          "Properties":[
            {
              "Id":"integer",
              "Region":"string",
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
  ]
}
```
