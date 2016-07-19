Address
=======

Property records with related auditor, permit and professional data.


GET ADDRESS
----------

* `GET /address/[postal+address]` will return a permit object with all related data.

```shell
curl -u account:secret https://api.datarole.com/building/v2/address/776+Buena+Vista+Ave+Alameda+CA+94501
```

```json
{
    "Property": {
        "Address": {
            "OriginalAddress1": "776 Buena Vista Ave",
            "OriginalAddress2": null,
            "OriginalAddress3": "Alameda CA 94501-2156",
            "Components": {
                "PrimaryNumber": "776",
                "StreetName": "Buena Vista",
                "StreetSuffix": "Ave",
                "CityName": "Alameda",
                "StateAbbreviation": "CA",
                "Zipcode": "94501",
                "Plus4Code": "2156",
                "DeliveryPoint": "76",
                "DeliveryPointCheckDigit": "4"
            },
            "MetaData": {
                "RecordType": "S",
                "ZipType": "Standard",
                "CountyFips": "06001",
                "CountyName": "Alameda",
                "CarrierRoute": "C073",
                "CongressionalDistrict": "13",
                "Rdi": "Residential",
                "ElotSequence": "0207",
                "ElotSort": "D",
                "Latitude": 37.77703,
                "Longitude": -122.27385,
                "Precision": "Zip9",
                "TimeZone": "Pacific",
                "UtcOffset": -8,
                "Dst": true
            },
            "Analysis": {
                "DpvMatchCode": "Y",
                "DpvFootnotes": "AABB",
                "DpvCmra": "N",
                "DpvVacant": "N",
                "Active": "Y"
            }
        },
        "Auditor": null,
        "Permits": {
            "3637018": {
                "Id": 3637018,
                "DateModified": {
                    "date": "2016-07-11 10:34:03.000000",
                    "timezone_type": 3,
                    "timezone": "America\/Chicago"
                },
                "DateModifiedTimestamp": 1468251243,
                "Description": "SEWER LATERAL REPLACEMENT\/EXISTING KELLY CLEANOUT",
                "EstProjectCost": "3500.00",
                "IssuedDate": {
                    "date": "2014-04-07 00:00:00.000000",
                    "timezone_type": 3,
                    "timezone": "America\/Chicago"
                },
                "IssuedDateTimestamp": 1396846800,
                "LastUpdated": {
                    "date": "2014-04-08 11:39:36.000000",
                    "timezone_type": 3,
                    "timezone": "America\/Chicago"
                },
                "LastUpdatedTimestamp": 1396975176,
                "PermitClass": null,
                "PermitNum": "SLR14-0055",
                "PermitType": "Other",
                "Region": "CA_Alameda",
                "StatusCurrent": "FINALED",
                "Professionals": {
                    "250483": {
                        "Id": 250483,
                        "ContractorCompanyName": "SING SING CONSTRUCTION CO",
                        "ContractorEmail": "KARENANDCHEE@HOTMAIL.COM",
                        "ContractorLicNum": "519536",
                        "ContractorPhone": "5107480699",
                        "DateModified": {
                            "date": "2016-07-17 05:18:07.000000",
                            "timezone_type": 3,
                            "timezone": "America\/Chicago"
                        },
                        "DateModifiedTimestamp": 1468750687,
                        "Region": "CA_Alameda"
                    }
                }
            },
            "3638810": {
                "Id": 3638810,
                "DateModified": {
                    "date": "2016-07-11 10:34:17.000000",
                    "timezone_type": 3,
                    "timezone": "America\/Chicago"
                },
                "DateModifiedTimestamp": 1468251257,
                "Description": "INSTALLATION OF AN AUTOMATIC EARTHQUAKE SHUT-OFF VALVE:  LITTLE FIREFIGHTER, MODEL #AGV-075, 3\/4\u0022 PIPE SIZE, HORIZONTAL",
                "EstProjectCost": "500.00",
                "IssuedDate": {
                    "date": "2014-04-01 00:00:00.000000",
                    "timezone_type": 3,
                    "timezone": "America\/Chicago"
                },
                "IssuedDateTimestamp": 1396328400,
                "LastUpdated": {
                    "date": "2014-04-07 07:32:34.000000",
                    "timezone_type": 3,
                    "timezone": "America\/Chicago"
                },
                "LastUpdatedTimestamp": 1396873954,
                "PermitClass": null,
                "PermitNum": "P14-0163",
                "PermitType": "Plumbing",
                "Region": "CA_Alameda",
                "StatusCurrent": "FINALED",
                "Professionals": {
                    "250483": {
                        "Id": 250483,
                        "ContractorCompanyName": "SING SING CONSTRUCTION CO",
                        "ContractorEmail": "KARENANDCHEE@HOTMAIL.COM",
                        "ContractorLicNum": "519536",
                        "ContractorPhone": "5107480699",
                        "DateModified": {
                            "date": "2016-07-17 05:18:07.000000",
                            "timezone_type": 3,
                            "timezone": "America\/Chicago"
                        },
                        "DateModifiedTimestamp": 1468750687,
                        "Region": "CA_Alameda"
                    }
                }
            },
            "3638895": {
                "Id": 3638895,
                "DateModified": {
                    "date": "2016-07-11 10:34:17.000000",
                    "timezone_type": 3,
                    "timezone": "America\/Chicago"
                },
                "DateModifiedTimestamp": 1468251257,
                "Description": "SEWER LATERAL TEST\/INSTALL KELLY CLEAN-OUT",
                "EstProjectCost": "1100.00",
                "IssuedDate": {
                    "date": "2014-04-01 00:00:00.000000",
                    "timezone_type": 3,
                    "timezone": "America\/Chicago"
                },
                "IssuedDateTimestamp": 1396328400,
                "LastUpdated": {
                    "date": "2014-04-07 07:32:12.000000",
                    "timezone_type": 3,
                    "timezone": "America\/Chicago"
                },
                "LastUpdatedTimestamp": 1396873932,
                "PermitClass": null,
                "PermitNum": "SLT14-0054",
                "PermitType": "Other",
                "Region": "CA_Alameda",
                "StatusCurrent": "FAILED",
                "Professionals": {
                    "250483": {
                        "Id": 250483,
                        "ContractorCompanyName": "SING SING CONSTRUCTION CO",
                        "ContractorEmail": "KARENANDCHEE@HOTMAIL.COM",
                        "ContractorLicNum": "519536",
                        "ContractorPhone": "5107480699",
                        "DateModified": {
                            "date": "2016-07-17 05:18:07.000000",
                            "timezone_type": 3,
                            "timezone": "America\/Chicago"
                        },
                        "DateModifiedTimestamp": 1468750687,
                        "Region": "CA_Alameda"
                    }
                }
            },
            "3859179": {
                "Id": 3859179,
                "DateModified": {
                    "date": "2016-07-11 11:56:33.000000",
                    "timezone_type": 3,
                    "timezone": "America\/Chicago"
                },
                "DateModifiedTimestamp": 1468256193,
                "Description": "R\/R 8 WINDOWS IN-KIND (ALUMINUM CASEMENTS TO SLIDING VINYL)",
                "EstProjectCost": "3363.00",
                "IssuedDate": {
                    "date": "2013-09-23 00:00:00.000000",
                    "timezone_type": 3,
                    "timezone": "America\/Chicago"
                },
                "IssuedDateTimestamp": 1379912400,
                "LastUpdated": {
                    "date": "2013-10-30 11:22:23.000000",
                    "timezone_type": 3,
                    "timezone": "America\/Chicago"
                },
                "LastUpdatedTimestamp": 1383150143,
                "PermitClass": "Residential",
                "PermitNum": "B13-0979",
                "PermitType": "Building",
                "Region": "CA_Alameda",
                "StatusCurrent": "FINALED"
            },
            "4177758": {
                "Id": 4177758,
                "DateModified": {
                    "date": "2016-07-11 13:20:15.000000",
                    "timezone_type": 3,
                    "timezone": "America\/Chicago"
                },
                "DateModifiedTimestamp": 1468261215,
                "Description": "REMODEL KITCHEN: ELECTRICAL UPGRADES OF GFCI RECEPTACLES \u0026 LIGHTING (NO PERMIT REQUIRED FOR CABINETS AND\/OR COUNTERS)",
                "EstProjectCost": "500.00",
                "IssuedDate": {
                    "date": "2011-09-19 00:00:00.000000",
                    "timezone_type": 3,
                    "timezone": "America\/Chicago"
                },
                "IssuedDateTimestamp": 1316408400,
                "LastUpdated": {
                    "date": "2011-11-22 12:38:22.000000",
                    "timezone_type": 3,
                    "timezone": "America\/Chicago"
                },
                "LastUpdatedTimestamp": 1321987102,
                "PermitClass": null,
                "PermitNum": "E11-0237",
                "PermitType": "Electrical",
                "Region": "CA_Alameda",
                "StatusCurrent": "FINALED"
            },
            "5681622": {
                "Id": 5681622,
                "DateModified": {
                    "date": "2016-07-15 14:12:52.000000",
                    "timezone_type": 3,
                    "timezone": "America\/Chicago"
                },
                "DateModifiedTimestamp": 1468609972,
                "Description": "UPGRADE ELECTRICAL SERVICE TO 200 AMPS (LOCATED AT ATTACHED GARAGE); AND INSTALL NEW SUBPANEL ON INTERIOR OF GARAGE",
                "EstProjectCost": "1000.00",
                "IssuedDate": {
                    "date": "2014-04-29 00:00:00.000000",
                    "timezone_type": 3,
                    "timezone": "America\/Chicago"
                },
                "IssuedDateTimestamp": 1398747600,
                "LastUpdated": {
                    "date": "2015-03-30 15:57:18.000000",
                    "timezone_type": 3,
                    "timezone": "America\/Chicago"
                },
                "LastUpdatedTimestamp": 1427749038,
                "PermitClass": null,
                "PermitNum": "E14-0122",
                "PermitType": "Electrical",
                "Region": "CA_Alameda",
                "StatusCurrent": "FINALED"
            }
        }
    }
}
```
