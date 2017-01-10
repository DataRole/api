Address
=======

Property records with related auditor, permit and professional data.


GET ADDRESS
----------

* `GET /address/[postal+address]` will return a property object with all related data.

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
                "PermitNum": "E14-0122",
                "PermitType": "Electrical",
                "Region": "CA_Alameda",
                "StatusCurrent": "FINALED"
            }
        }
    }
}
```

<br>
Data Dictionary
===
Description of the contents, format, and structure of the response from an *Address* request.

## Address
Field Name | Type | Definition
--- | --- | ---
OriginalAddress1 | varchar(50) | Contains the first delivery line (usually the street address). This can include any of the following: Primary Number, Street Name, Street Predirection, Street Postdirection, Street Suffix, Secondary Number, Secondary Designator, PMB Designator, PMB Number
OriginalAddress2 | varchar(50) | The second delivery line (if needed). It is common for this field to remain empty, but it may contain a private mailbox number.
OriginalAddress3 | varchar(50) | City, State, and ZIP Code combined

## Address: Components
Field Name | Type | Definition
--- | --- | ---
PrimaryNumber | varchar(30) | The Property, PO Box, or Building Number
StreetName | varchar(64) | The name of the street
StreetPredirection | char(16) |	Directional information before a street name (N, SW, etc.)
StreetPostdirection | char(16) | Directional information after a street name (N, SW, etc.)
StreetSuffix | char(16) | Abbreviated value describing the street (St, Ave, Blvd, etc.)
SecondaryNumber | varchar(32) |	Apartment or suite number, if any
SecondaryDesignator | varchar(16) |	Describes location within a complex/building (Ste, Apt, etc.)
ExtraSecondaryNumber | varchar(32) | Descriptive information about the location of a building within a campus (e.g., E-5 in "5619 Loop 1604, Bldg E-5, Ste. 101 San Antonio TX")
ExtraSecondaryDesignator | varchar(16) | Description of the location type within a campus (e.g., Bldg, Unit, Lot, etc.)
PmbDesignator |	varchar(16) | Private mailbox unit designator (assigned by a CMRA)
PmbNumber |	varchar(16) | The private mailbox number, assigned by a CMRA
CityName | varchar(64) | The accepted/proper name of the city
DefaultCityName | varchar(64) |	The default city name for the address. This field will not be present if the default city name is equal to the value of the city name field.
StateAbbreviation |	char(2)	| The two-letter state abbreviation
Zipcode | char(5) |	The 5-digit ZIP Code
Plus4Code | char(4) | The 4-digit add-on code (more specific than 5-digit ZIP)
DeliveryPoint |	char(2) | The last two digits of the house/box number, unless an "H" record is matched, in which case this is the secondary unit number representing the delivery point information to form the delivery point barcode (DPBC).
DeliveryPointCheckDigit | char(1) |	Correction character, or check digit, for the 11-digit barcode

## Address: MetaData
Field Name | Type | Definition
--- | --- | ---
RecordType | char(1) |	Indicates the type of record that was matched. Only given if a DPV match is made.<br><br><ul><li>F — Firm; the finest level of match available for an address</li><li>G — General Delivery; for mail to be held at local post offices</li><li>H — High-rise; address contains apartment or building sub-units.</li><li>P — Post Office box; address is a PO Box record type.</li><li>R — Rural Route or Highway Contract; may have box number ranges.</li><li>S — Street; address contains a valid primary number range.</li><li>[blank] — No record type because address did not make a valid DPV match</li></ul>
ZipType | varchar(32) |	Indicates the type of the ZIP Code for the address that was matched. Only given if a 5-digit match is made.<br><br><ul><li>Unique — The ZIP Code consists of a single delivery point, pertaining to a United States Postal Service customer (like a large business or government agency) that routes all of its own mail internally.</li><li>Military — The ZIP Code pertains to military units, often deployed to foreign locations.</li><li>POBox — The ZIP Code is assigned to a collection of Post Office Boxes.</li><li>Standard — The ZIP Code does not pertain to any of the above categories.</li></ul>
CountyFips | char(5) |	The 5-digit county FIPS (Federal Information Processing Standards) code. It is a combination of a 2-digit state FIPS code and a 3-digit county code assigned by the NIST (National Institute of Standards and Technology).
CountyName | varchar(64) |	The name of the county the address is in
CarrierRoute |	char(4) | The postal carrier route for the address
CongressionalDistrict |	char(2) | The congressional district to which the address belongs. Output will be two digits from 01 - 53 or "AL." "AL" means that the entire state (or territory) is covered by a single congressional district. These include Alaska, Delaware, Montana, North Dakota, South Dakota, Vermont, Wyoming, Washington DC, Virgin Islands, and other territories.
BuildingDefaultIndicator |	char(1) | Indicates whether the address is the "default" address for a building; for example, the main lobby
Rdi | varchar(12) |	Residential Delivery Indicator (residential or commercial)<br><br><ul><li>Residential — The address is a residential address.</li><li>Commercial — The address is a commercial address.</li><li>[blank] — This happens when the address is invalid and we don't have enough information to ascertain RDI status.</li></ul>Note: For some reason, known only to the US Postal Service, PO Boxes are always marked as "Residential".
ElotSequence |	varchar(4) | eLOT (Enhanced Line of Travel) 4-digit sequence number
ElotSort |	varchar(4) | eLOT (Enhanced Line of Travel) product was developed to give mailers the ability to sort their mailings by line of travel sequence.<br><br><ul><li>A — Ascending</li><li>D — Descending</li><li>[blank] — Address not submitted for eLOT</li></ul>
Latitude |	decimal(12,9) |	The horizontal component used for geographic positioning. It is the angle between 0° (the equator) and ±90° (north or south) at the poles. It is the first value in an ordered pair of (latitude, longitude). A negative number denotes a location below the equator; a positive number is above the equator. Combining lat/long values enables you to pinpoint an addresses on a map.
Longitude |	decimal(12,9) |	The vertical component used for geographic positioning. It is the angle between 0° (the Prime Meridian) and ±180° (westward or eastward). It is the second number in an ordered pair of (latitude, longitude). A negative number indicates a location west of Greenwich, England; a positive number east. Combining lat/long values enables you to pinpoint addresses on a map.
Precision | varchar(18) | Indicates the precision of the latitude and longitude values.<br><br><ul><li>Unknown — Coordinates not known, possibly because address is invalid</li><li>None — Coordinates are not provided for this address. Military addresses such as APO, FPO, and DPO do not provide coordinates.</li><li>State — Reserved for future use</li><li>SolutionArea — Reserved for future use</li><li>City — Reserved for future use</li><li>Zip5 — Accurate to a 5-digit ZIP Code level (least precise)</li><li>Zip6 — Accurate to a 6-digit ZIP Code level</li><li>Zip7 — Accurate to a 7-digit ZIP Code level</li><li>Zip8 — Accurate to an 8-digit ZIP Code level</li><li>Zip9 — Accurate to a 9-digit ZIP Code level (most precise but NOT rooftop level)</li><li>Structure — Reserved for future use</li></ul>Note: Concerning addresses for which the ZIP9 precision is not available, the ZIP# precision is interpolated based on neighboring addresses. Thus, ZIP7 is an average of all the lat/long coordinates of nearby ZIP Codes that share those first 7 digits.
TimeZone | varchar(48) | Indicates the common name of the time zone associated with the address.**Valid Responses** <br>Alaska, Atlantic, Central, Eastern, Hawaii, Mountain, None, Pacific, Samoa, UTC+9, UTC+10, UTC+11, UTC+12
UtcOffset |	decimal(4,2) |	Indicates the number of hours the time zone is offset from Universal Time Coordinated (UTC), the international time standard, also known as Greenwich Meridian Time (GMT).<br><br>**Valid Responses**<br>-11, -10, -9, -8, -7, -6, -5, -4, 0, 9, 10, 11, 12
Dst	| char(5) |	Indicates if the time zone "obeys," or, in other words, adjusts their clocks forward and back with the seasons. This information is particularly useful to determine time in other time zones with areas that may or may not use daylight saving time - for example, Arizona, Hawaii, and, of all places, Indiana.<br><br>**true** — Time zone observes daylight saving time.<br><br>If dst is absent from the response, then time zone does not observe daylight saving time.

## Address: Analysis
Field Name | Type | Definition
--- | --- | ---
DpvMatchCode |	varchar(1) | Status of the Delivery Point Validation (DPV). This lets you know if the USPS delivers mail to the address.<br><br><ul><li>Y — Confirmed; entire address was DPV confirmed deliverable. (e.g., 1600 Amphitheatre Pkwy Mountain View, CA)</li><li>N — Not Confirmed; address could not be DPV confirmed as deliverable.</li><li>S — Confirmed By Dropping Secondary; address was DPV confirmed by dropping secondary info (apartment, suite, etc.). (e.g., 62 Ea Darden Dr Apt 298 Anniston, AL)</li><li>D — Confirmed - Missing Secondary Info; the address was DPV confirmed, but it is missing secondary information (apartment, suite, etc.). (e.g., 122 Mast Rd Lee, NH)</li><li>[blank] — The address was not submitted for DPV. This is usually because the address does not have a ZIP Code and a +4 add-on code, or the address has already been determined to be Not Deliverable (only returned as part of the XML response).</li></ul>
DpvFootnotes |	varchar(32) | Indicates why the address was given its DPV value and potentially the type of ZIP Code that was matched. All these footnotes have a length of 2 characters, and there may be up to 14 footnotes.<br><br><ul><li>AA — City/state/ZIP + street are all valid. (e.g., 2335 S State St Ste 300 Provo UT)</li><li>A1 — ZIP+4 not matched; address is invalid. (City/state/ZIP + street don't match.) (e.g., 3214 N University Ave New York NY)</li><li>BB — ZIP+4 matched; confirmed entire address; address is valid. (e.g., 2335 S State St Ste 300 Provo UT)</li><li>CC — Confirmed address by dropping secondary (apartment, suite, etc.) information. (e.g., 2335 S State St Ste 500 Provo UT)</li><li>F1 — Matched to military address. (e.g., Unit 2050 Box 4190 APO AP 96278)</li><li>G1 — Matched to general delivery address. (e.g., General Delivery Provo UT 84604)</li><li>M1 — Primary number (e.g., house number) is missing. (e.g., N University Ave Provo UT)</li><li>M3 — Primary number (e.g., house number) is invalid. (e.g., 16 N University Ave Provo UT)</li><li>N1 — Confirmed with missing secondary information; address is valid but it also needs a secondary number (apartment, suite, etc.). (e.g., 2335 S State St Provo UT)</li><li>P1 — PO, RR, or HC box number is missing. (e.g., RR 5 Cadiz KY)</li><li>P3 — PO, RR, or HC box number is invalid. (e.g., RR 5 Box 1000 Cadiz KY)</li><li>RR — Confirmed address with private mailbox (PMB) info. (e.g., 3214 N university ave #409 Provo UT)</li><li>R1 — Confirmed address without private mailbox (PMB) info. (e.g., 3214 N university ave Provo UT)</li><li>U1 — Matched a unique ZIP Code. (e.g., 100 North Happy Street 12345)</li></ul>
DpvCmra | varchar(1) |	Indicates whether the address is associated with a Commercial Mail Receiving Agency (CMRA), also known as a private mailbox (PMB) operator. A CMRA is a business through which USPS mail may be sent or received, for example the UPS Store and Mailboxes Etc.<br><br><ul><li>Y — Address is associated with a valid CMRA.</li><li>N — Address is not associated with a valid CMRA.</li><li>[blank] — Address was not submitted for CMRA verification.</li></ul>
DpvVacant |	varchar(1) | Indicates that a delivery point was active in the past but is currently vacant (in most cases, unoccupied over 90 days) and is not receiving deliveries. This status is often obtained when mail receptacles aren't being emptied and are filling up, so mail is held at the post office for a certain number of days before the delivery point is marked vacant.<br><br><ul><li>Y — Address is vacant.</li><li>N — Address is not vacant.</li><li>[blank] — Address was not submitted for vacancy verification.</li></ul>
Active | varchar(1) | Indicates whether the address is active, or "in-service" according to the USPS. Examples: New developments may have addresses but will be "inactive" until somebody moves in. Or, after Hurricane Katrina, addresses in the affected area were marked as inactive for a time. Residents may also mark their own mailboxes as inactive for privacy and other reasons.<br><br><ul><li>Y — Address is active.</li><li>N — Address is inactive.</li><li>[blank] — Activity status is not known by the USPS.</li></ul>
EwsMatch |	char(5) | Early warning system flag; a positive result indicates the street of the address is not yet ready for mail delivery and that the address will soon be added to the master ZIP+4 file in the coming weeks or months. This commonly occurs for new streets or streets undergoing a name change.<br><br><ul><li>true — The address was flagged by EWS, preventing a ZIP+4 match.</li><li>[blank] — Address was not flagged by EWS.</li></ul>
Footnotes |	varchar(12) | Indicates which changes were made to the input address. Footnotes are delimited by a # character. See the **[footnotes](https://smartystreets.com/docs/us-street-api#footnotes)** table for details.
LacslinkCode |	varchar(2) | The reason for the LACSLink indication that was given (below)<br><br><ul><li>A — Match: Address provided. LACSLink record match was found, and a converted address was provided.</li><li>00 — No Match. No converted address. No soup for you!</li><li>09 — Match: No new address. LACSLink matched an input address to an old address which is a "high-rise default" address; no new address was provided.</li><li>14 — Match: No conversion. Found a LACSLink record, but couldn't convert the data to a deliverable address.</li><li>92 — Match: Dropped secondary number. LACSLink record was matched after dropping the secondary number from input.</li><li>[blank] — No LACSLink lookup attempted.</li></ul>
LacslinkIndicator |	varchar(1) | Indicates whether there is an address match in the LACSLink database.<br><br><ul><li>Y — LACS record match; a new address could be furnished because the input record matched a record in the master file.</li><li>S — LACS record - secondary number dropped; the record is a ZIP+4 street level or high-rise match. The input record matched a master file record, but the input address had a secondary number and the master file record did not.</li><li>N — No match; a new address could not be furnished; the input record could not be matched to a record in the master file.</li><li>F — False positive; a false positive record was detected.</li><li>[blank] — No LACSLink lookup attempted.</li><\ul>
SuitelinkMatch | varchar(5) | Indicates a match (or not) to the USPS SuiteLink data. SuiteLink attempts to provide secondary information such as "suite" or "apartment" whenever there is a match based on address and Firm Name (Company) input.<br><br><ul><li>true — There was a SuiteLink match and the result is provided.</li><li>false — There was no SuiteLink match.</li></ul>

## Auditor
Coming Soon

## Permits
Field Name | Type | Definition
--- | --- | ---
Id | integer | Internal identification number
DateModified | datetime | Date/Time value indicating date, timezone type and timezone of last internal update
DateModifiedTimestamp | integer | Unix timestamp of date modified
Description | string | Context of work performed for the permit
EstProjectCost | float | Estimated value of the work performed
IssuedDate | datetime | Date/Time value indicating date, timezone type and timezone of the date the permit was issued
IssuedDateTimestamp | integer | Unix timestamp of issued date
PermitNum | string | Source identification number ( Permit filing number )
PermitType | string | Category of work performed (e.g. Roof, Plumbing, HVAC, Electrical )
Region | string | Internal classification for provenance of data
StatusCurrent | string | Current status of the permit (e.g. Applied, Issued, Finaled, Pending )

## Permits: Professionals
Field Name | Type | Definition
--- | --- | ---
Id | integer | Internal identification number
ContractorCompanyName | string | Name of the business that performed the work
ContractorEmail | string | Contact email for the business that performed the work 
ContractorLicNum | string | License number of the business that performed the work
ContractorPhone | integer | Phone number of the business that performed the work
DateModified | datetime | Date/Time value indicating date, timezone type and timezone of last internal update
DateModifiedTimestamp | integer | Unix timestamp of date modified
Region | string | Internal classification for provenance of data
