---
title: HR REST API
description: The HR REST API provides endpoints that return information about employees that work or live in the United States.Returns employee profile information for employees based in the United States.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# HR REST API

The HR REST API provides endpoints that return information about employees that work or live in the United States.

To access this API you must have the sn\_hr\_core.usa\_employee\_only role and the Human Resources Scoped App: Core \(com\_sn\_hr\_core\) plugin activated.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## HR REST - GET /get\_usa\_employee\_profile

Returns employee profile information for employees based in the United States.

The returned information can be either:

-   Employee profile information for a specified employee ID.
-   Information for employees that have been added, or whose information has been updated, on or after a specified date.

**Note:** Employees must either have their work or home country specified as the United States for this endpoint to include them in the return results.

In addition, the endpoint sends the following parameters to the integrated CIC Plus application \(see the Returns section for descriptions\):

-   EmployeeIdentifier
-   FirstName
-   MiddleName
-   LastName
-   Email
-   WorkAddress
-   WorkCity
-   WorkState
-   WorkPostalCode
-   WorkCountry
-   HomeAddress
-   HomeCity
-   HomeState
-   HomePostalCode
-   HomeCountry
-   BirthDate
-   HireDate

### URL format

Default URL: `/api/sn_hr_core/hr_rest_api/get_usa_employee_profile`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

employee\_identifier

</td><td>

Unique identifier of an employee. The calling system generates this value and can be in whatever format is consistent with their system. To obtain this value, first call the endpoint using the **updated\_after** parameter.**Note:** This parameter is mutually exclusive with the **updated\_after** parameter. This parameter defines a unique employee, whereas **updated\_after** returns a group of employees created/updated after a specified date.

Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. Data type: Number

Default: 1000

</td></tr><tr><td>

sysparm\_offset

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

</td></tr><tr><td>

updated\_after

</td><td>

Date to use to determine the employee data to return. All United States-based employees \(work or home\) that were added to your instance, or whose information was updated on or after this date, are included in the return results.**Note:** This parameter is mutually exclusive with the **employee\_identifier** parameter.

Data type: String

Format: YYYY-MM-DD HH:MM:SS or YYYY-MM-DD \(time defaults to 00:00:00\)

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Next-Page

</td><td>

Flag that indicates whether there is additional data to obtain in a subsequent call. For example, if there are a total of 120 employee records that match the search criteria, and sysparm\_limit is set to 100, then **Next-Page** is true. If no additional results are available, **Next-Page** is false.Valid values:

-   true: Additional data is available, another call must be made to obtain the next chunk of data.
-   false: No additional data.

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

BirthDate

</td><td>

Employee's birth date.Data type: String

</td></tr><tr><td>

Company

</td><td>

Company name.Data type: String

</td></tr><tr><td>

Email

</td><td>

Employee's email address.Data type: String

</td></tr><tr><td>

EmployeeIdentifier

</td><td>

Unique employee identifier.Data type: String

</td></tr><tr><td>

FirstName

</td><td>

Employee's first name.Data type: String

</td></tr><tr><td>

HireDate

</td><td>

Date on which the employee was hired.Data type: String

</td></tr><tr><td>

LastName

</td><td>

Employee's last name.Data type: String

</td></tr><tr><td>

MiddleName

</td><td>

Employee's middle name.Data type: String

</td></tr><tr><td>

ReHire

</td><td>

For future use.Data type: String

</td></tr><tr><td>

ResidenceAddress

</td><td>

Employee's home street address.Data type: String

</td></tr><tr><td>

ResidenceCity

</td><td>

Employee's home city.Data type: String

</td></tr><tr><td>

ResidenceCountry

</td><td>

Employee's home country.Data type: String

</td></tr><tr><td>

ResidencePostalCode

</td><td>

Employee's home zip code.Data type: String

</td></tr><tr><td>

ResidenceState

</td><td>

Employee's home state.Data type: String

</td></tr><tr><td>

Suffix

</td><td>

Employee's suffix, such as Mr., Mrs., or Dr.Data type: String

</td></tr><tr><td>

WorkAddress

</td><td>

Employee's work street address.Data type: String

</td></tr><tr><td>

WorkCity

</td><td>

Employee's work cityData type: String

</td></tr><tr><td>

WorkCountry

</td><td>

Employee's work country.Data type: String

</td></tr><tr><td>

WorkPostalCode

</td><td>

Employee's work zip code.Data type: String

</td></tr><tr><td>

WorkState

</td><td>

Employee's work state.Data type: String

</td></tr></tbody>
</table>### Sample cURL request for a specific employee's information

```
curl -X GET "https://instance.servicenow.com/api/sn_hr_core/V1/hr_rest_api/get_usa_employee_profile?employee_identifier=231"
-H "accept: application/json" \
-u "username":"password"
```

```
{"result": [
 {
  "EmployeeIdentifier": "231",
  "FirstName": "Harold",
  "MiddleName": "William",
  "LastName": "Lewis",
  "Suffix": "Mr.",
  "Email": "Howard.Lewis@example.com",
  "BirthDate": "",
  "HireDate": "2021-02-18",
  "Company": "ServiceNow Inc",
  "ResidenceAddress": "",
  "ResidenceCity": "SD",
  "ResidenceState": "CA",
  "ResidencePostalCode": "",
  "ResidenceCountry": "",
  "WorkAddress": "2617 South Robinson Avenue, Oklahoma City",
  "WorkCity": "Oklahoma",
  "WorkState": "OK",
  "WorkPostalCode": "73109",
  "WorkCountry": "USA",
  "ReHire": ""
 }
]}
```

### Sample cURL request for a list of employees added/updated on or after 05/18/2019

```
curl -X GET "https://instance.servicenow.com/api/sn_hr_core/V1/hr_rest_api/get_usa_employee_profile?update_after=2019-05-18"
-H "accept: application/json" \
-u "username":"password"
```

```
{"result": [
 {
  "EmployeeIdentifier": "2345",
  "FirstName": "Cheryl",
  "MiddleName": "Lynn",
  "LastName": "Smith",
  "Suffix": "Mrs.",
  "Email": "Cheryl.Smith@example.com",
  "BirthDate": "",
  "HireDate": "2019-06-18",
  "Company": "ServiceNow Inc",
  "ResidenceAddress": "",
  "ResidenceCity": "SD",
  "ResidenceState": "CA",
  "ResidencePostalCode": "",
  "ResidenceCountry": "",
  "WorkAddress": "2617 South Robinson Avenue, Oklahoma City",
  "WorkCity": "Oklahoma",
  "WorkState": "OK",
  "WorkPostalCode": "73109",
  "WorkCountry": "USA",
  "ReHire": ""
  },
  {
  "EmployeeIdentifier": "1111",
  "FirstName": "Thomas",
  "MiddleName": "",
  "LastName": "Doe",
  "Suffix": "Mr.",
  "Email": "Thomas.Doe@example.com",
  "BirthDate": "1978-05-22",
  "HireDate": "2019-08-14",
  "Company": "",
  "ResidenceAddress": "",
  "ResidenceCity": "San Jose",
  "ResidenceState": "CA",
  "ResidencePostalCode": "",
  "ResidenceCountry": "",
  "WorkAddress": "13308 Midland Road, Poway",
  "WorkCity": "Poway",
  "WorkState": "CA",
  "WorkPostalCode": "",
  "WorkCountry": "USA",
  "ReHire": ""
  }
]}   
```

