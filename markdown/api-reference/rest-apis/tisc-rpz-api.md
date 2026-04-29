---
title: TISC RPZ API
description: The TISC RPZ API provides an endpoint to export domains and IP addresses in Response Policy Zone \(RPZ\) format.Exports domains and IP addresses in Response Policy Zone \(RPZ\) format.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# TISC RPZ API

The TISC RPZ API provides an endpoint to export domains and IP addresses in Response Policy Zone \(RPZ\) format.

Use this API to retrieve filtered threat intelligence data in RPZ format for use in firewalls, DNS servers, or other security systems that support RPZ policies. RPZ is used to block, allow, or redirect domains and IP addresses. The API response is served as **text/plain** to facilitate straightforward integration into security workflows.

This API requires the Threat Intelligence Security Center application, which is available on the ServiceNow Store.

For additional information about TISC, see [Threat Intelligence Security Center](https://www.servicenow.com/docs/access?context=tisc-landing-page&version=australia&pubname=australia-security-management&ft:locale=en-US).

This API runs in the `sn_sec_tisc` namespace. The calling user must have the sn\_sec\_tisc.api\_obs\_read\_access role.

The current version of this API is `v1`.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## TISC RPZ - POST /sn\_sec\_tisc/rpz\_export

Exports domains and IP addresses in Response Policy Zone \(RPZ\) format.

**Note:** You can generate a wildcard entry \(`*.<domain_name>`\) for a domain in the export. A wildcard entry provides the flexibility to block or allow all subdomains of a domain. To enable this functionality, navigate to the domain record in Threat Intelligence Security Center. In the TISC Tags &amp; Taxonomies section of the Details tab, fill in the Taxonomy fields.

-   In the **Select Taxonomy** field, select **RPZ Domain**.
-   In the **Add Taxonomy Values** field, select **Add Wildcard Entry**.

Click **Add** to save the taxonomy for the domain.

![Domain record in TISC with the Taxonomy fields highlighted.](../image/TISC-RPZ-domain.png "Domain record in TISC")

### URL format

Versioned URL: `/api/sn_sec_tisc/{api_version}/rpz_export`

Default URL: `/api/sn_sec_tisc/rpz_export`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

feed\_type

</td><td>

Required. Type of observables to export. Valid values \(case-insensitive\):

-   `IP` – Include only IP addresses \(IPv4 address, IPv4 CIDR, IPv6 address, and IPv6 CIDR\).
-   `Domain` – Include only domain names.
-   `IP_Domain` – Include both IP addresses and domain names.

Data type: String

</td></tr><tr><td>

observable\_filters

</td><td>

Filters to apply to the observables. Only observables that match the filter criteria are returned in the response.Data type: Object

```
"observable_filters": {
   "boolean_operator": "String", 
   "filters": [Array]
}
```

Default: Empty object \(no filters applied\)

</td></tr><tr><td>

observable\_filters.boolean\_operator

</td><td>

Boolean operator to use for the filter conditions.Valid values:

-   AND: Return observables that meet all filter conditions.
-   OR: Return observables that meet at least one of the filter conditions.

Data type: String

</td></tr><tr><td>

observable\_filters.filters

</td><td>

Filters to apply to the observables. Each filter object can be simple or complex.

-   Simple filters contain a field name, operator, and value.
-   Complex filters contain a Boolean operator and an array of simple filters. The Boolean operator is applied to the array of simple filters.

Data type: Array of Objects

```
"filters": [ 
   //Simple filter 
   { 
      "field_name": "String", 
      "operator": "String", 
      "field_value": "String" 
   }, 
   //Complex filter 
   {
      "boolean_operator": "String", 
      "filters": [
         {
	     "field_name": "String",
	     "operator": "String",
	     "field_value": "String"
         }  
      ]
   }
]
```

</td></tr><tr><td>

observable\_filters.filters.field\_name

</td><td>

Name of the field to use to filter the observables. Valid values:

-   confidence
-   reputation
-   security\_type
-   status
-   sys\_created\_on
-   sys\_updated\_on
-   tags
-   taxonomies
-   threat\_score
-   value
-   watch\_list

Data type: String

</td></tr><tr><td>

observable\_filters.filters.field\_value

</td><td>

Value of the field.For choice fields, the value must be the internal value, not the display value. For date-time fields, the value must be in ISO format in the UTC timezone.

**Note:** This parameter isn’t required when using the ISEMPTY or ISNOTEMPTY operators.

Data type: String

</td></tr><tr><td>

observable\_filters.filters.operator

</td><td>

Operator to use for the filter.For more information about operators, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

The data type of the filter field determines the valid operators. The following operators are valid for each data type.

-   **Boolean**

Applicable field: watch\_list

    -   !=
    -   =
    -   ISEMPTY
    -   ISNOTEMPTY
-   **Choice**

Applicable fields: reputation, security\_type, status

    -   !=
    -   =
    -   ENDSWITH
    -   IN
    -   LIKE
    -   NOT IN
    -   NOT LIKE
    -   STARTSWITH
-   **Date-time**

Applicable fields: sys\_created\_on, sys\_updated\_on

    -   &lt;
    -   &lt;=
    -   &gt;
    -   &gt;=
    -   ISEMPTY
    -   ISNOTEMPTY
    -   NOTON
    -   ON
-   **GlideList**

Applicable fields: tags, taxonomies

    -   IN
    -   NOT IN

**Note:** Must use a single valid, existing value for the filter condition, and empty observable field values aren't considered a match.

    -   ISEMPTY
    -   ISNOTEMPTY
    -   LIKE

**Note:** Must use a single value for the filter condition.

    -   NOT LIKE

**Note:** Must use a single value for the filter condition, and empty observable field values aren't considered a match.

-   **Number**

Applicable fields: confidence, threat\_score

    -   !=
    -   &lt;=
    -   =
    -   &gt;=
    -   ISEMPTY
    -   ISNOTEMPTY
-   **String**

Applicable field: value

    -   !=
    -   &lt;=
    -   =
    -   &gt;=
    -   ENDSWITH
    -   IN
    -   ISEMPTY
    -   ISNOTEMPTY
    -   LIKE
    -   NOT LIKE
    -   STARTSWITH

Data type: String

</td></tr><tr><td>

page\_size

</td><td>

Limits the number of observables that are returned in the API response. Used for pagination.Data type: Number

Default: 1000

Maximum value: 10,000

</td></tr><tr><td>

page\_token

</td><td>

Used to get observables data for the current page.To get the first page, this parameter can be omitted or the value for this parameter must be an empty string. To get the next page in the following request, use the **X-Next-Page-Token** value from the response header as the value for this parameter.

Data type: String

Default: Empty string

</td></tr><tr><td>

policy

</td><td>

Required. Action to take for the domains or IP addresses. Valid values \(case-insensitive\):

-   `NXDOMAIN` – Returns an NXDOMAIN response \(non-existent domain\).
-   `DROP` – Silently drops the query without a response.
-   `NODATA` – Returns a NOERROR response with no data.
-   `PASSTHRU` – Allows the query to proceed normally \(no action taken\).
-   `LOCAL-DATA` – Responds with locally defined DNS data. This can be used for sinkholing \(redirecting malicious domains or IPs to a safe internal address for monitoring or blocking outbound connections\).
-   `TCP-ONLY` – Forces the client to retry the query over TCP.

Data type: String

</td></tr><tr><td>

soa\_email

</td><td>

Required. Admin contact email for the zone. Use a dot \(.\) instead of the @ symbol to separate the username and domain, such as `admin.example.com.` instead of `admin@example.com.`. This parameter is included in the DNS SOA record.Data type: String

</td></tr><tr><td>

soa\_expiry

</td><td>

Required. Expiration time. Determines the maximum amount of time a secondary server continues to use zone data if the primary server becomes unreachable. Data type: Number

Unit: Seconds

Minimum: 0

Maximum: 4294967295

</td></tr><tr><td>

soa\_minimum\_ttl

</td><td>

Required. Minimum time to live for negative responses. Determines how long resolvers cache negative responses.**Note:** This parameter is always required for a valid request body, but the value is only used if the policy is NXDOMAIN, NODATA, or LOCAL-DATA. For other policies, this parameter has no effect.

Data type: Number

Unit: Seconds

Minimum: 0

Maximum: 4294967295

</td></tr><tr><td>

soa\_named\_server

</td><td>

Required. Primary name server for the zone. Must be a fully qualified domain name \(FQDN\) ending with a dot \(.\), such as `ns1.example.com.`. This parameter is the first field in the DNS SOA record.Data type: String

</td></tr><tr><td>

soa\_named\_server\_alt

</td><td>

Alternate name server for redundancy. Data type: String

</td></tr><tr><td>

soa\_refresh

</td><td>

Required. Refresh interval. Determines how often secondary DNS servers check the primary server for updates to the zone.Data type: Number

Unit: Seconds

Minimum: 0

Maximum: 4294967295

</td></tr><tr><td>

soa\_retry

</td><td>

Required. Retry interval. Determines how long a secondary server waits before retrying a failed zone transfer.Data type: Number

Unit: Seconds

Minimum: 0

Maximum: 4294967295

</td></tr><tr><td>

soa\_ttl

</td><td>

Required. Time to live \(TTL\) for RPZ records. Determines how long resolvers cache the records before checking for updates.Data type: Number

Unit: Seconds

Minimum: 0

Maximum: 4294967295

</td></tr><tr><td>

walled\_garden

</td><td>

IP address or domain name to use as the redirect target. Used to redirect users to a walled garden \(a controlled page or network location, typically for security, compliance, or informational purposes\).

**Note:** Required when **policy** is `LOCAL-DATA`. Don't use this parameter for any other policy types.

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr id="accept-row-RESTAPI"><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **text/plain** or **application/json**. Success responses are returned as plain text while error responses are returned as JSON.

Default: **text/plain**

</td></tr><tr><td>

Authorization

</td><td>

Basic. For more information about API authentication and authorization, see the REST API security section in [REST APIs](c_RESTAPI.md).

</td></tr><tr><td>

Content-Type

</td><td id="content_type-JSON-only-entry-RESTAPI">

Data format of the request body. Only supports **application/json**.

</td></tr></tbody>
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

X-Next-Page-Token

</td><td>

Use this value in the next API request to get the next page of results. Provide this value in the **page\_token** parameter in the request body. If this header is not present, no further pages are available.

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|429|Too many requests. The number of API requests exceeds the rate limit for the API. By default, the limit is 500 requests per hour.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

errorCode

</td><td>

HTTP status code for the request.

</td></tr><tr><td>

result

</td><td>

Details about the request. This parameter is only returned if the request failed.Data type: Object

```
"result": {
   "error": {Object},
   "status": "String" 
}
```

</td></tr><tr><td>

result.error

</td><td>

Error information.Data type: Object

```
"error": {   
   "detail": "String",
   "message": "String"
}
```

</td></tr><tr><td>

result.error.detail

</td><td>

Additional details about why the request failed.Data type: String

</td></tr><tr><td>

result.error.message

</td><td>

Error message containing the reason the request failed.Data type: String

</td></tr><tr><td>

result.status

</td><td>

Status of the API request. This parameter is only returned if the request failed so the only possible value is **failure**.Data type: String

</td></tr></tbody>
</table>### cURL request

This example exports selected domains in RPZ format and sets the policy as NXDOMAIN.

```
curl --location 'https://instance.service-now.com/api/sn_sec_tisc/v1/rpz_export' \ 
--header 'Authorization: Basic YWJlbC50dXRlcjpTbm93QDEyMw==' \
--data '{
    "policy": "nxdomain", 
    "feed_type": "DOMAIN", 
    "soa_retry": 85, 
    "soa_expiry": 1, 
    "soa_minimum_ttl": 7, 
    "soa_refresh": 3600, 
    "soa_ttl": 7678, 
    "soa_named_server": "localhost.", 
    "soa_email": "root.localhost.",
    "page_size": 100, 
    "page_token": "", 
    "observable_filters": { 
        "boolean_operator": "AND", 
        "filters": [ 
            { 
                "field_name": "status", 
                "operator": "=", 
                "field_value": "active" 
            }, 
            { 
                "boolean_operator": "OR", 
                "filters": [ 
                    { 
                        "field_name": "threat_score", 
                        "operator": ">=", 
                        "field_value": "70" 
                    }, 
                    { 
                        "field_name": "confidence", 
                        "operator": ">=", 
                        "field_value": "50" 
                    } 
                ] 
            } 
        ] 
    } 
}'
```

Response body containing the domains that match the filter criteria.

```
$TTL 7678;  
@ SOA localhost. root.localhost. (1759835257654 3600 85 1 7)
 IN NS localhost.  

; The following Domain records will be blocked (NXDOMAIN):
domain autuo.xicp.net CNAME .
microsofta.byinter.net CNAME .
www.webserver.freetcp.com CNAME .
mongoles.3322.org CNAME .
imddos.my03.com CNAME .
weile3322b.3322.org CNAME .
*.weile3322b.3322.org CNAME .
```

### cURL request

This example shows a request that uses an invalid policy value.

```
curl --location 'https://instance.service-now.com/api/sn_sec_tisc/v1/rpz_export' \ 
--header 'Authorization: Basic YWJlbC50dXRlcjpTbm93QDEyMw==' \
--data '{
    "policy": "LocalData", 
    "feed_type": "DOMAIN", 
    "soa_retry": 85, 
    "soa_expiry": 1, 
    "soa_minimum_ttl": 7, 
    "soa_refresh": 3600, 
    "soa_ttl": 7678, 
    "soa_named_server": "localhost.", 
    "soa_email": "root.localhost.",
    "page_size": 100, 
    "page_token": "", 
    "observable_filters": { 
        "boolean_operator": "AND", 
        "filters": [ 
            { 
                "field_name": "status", 
                "operator": "=", 
                "field_value": "active" 
            }, 
            { 
                "boolean_operator": "OR", 
                "filters": [ 
                    { 
                        "field_name": "threat_score", 
                        "operator": ">=", 
                        "field_value": "70" 
                    }, 
                    { 
                        "field_name": "confidence", 
                        "operator": ">=", 
                        "field_value": "50" 
                    } 
                ] 
            } 
        ] 
    } 
}'
```

Response body containing error information for a failed request.

```
{
   "result": {
      "status": "failure",
      "error": {
         "message": "Error occurred while processing request body.",
         "detail": "Invalid policy: 'LocalData'. Supported values are: NXDOMAIN, DROP, NODATA, PASSTHRU, LOCAL-DATA, TCP-ONLY"
      }
   },
   "errorCode": 400
}
```

