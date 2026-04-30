---
title: REST and SOAP API analytics collection and cleanup
description: API analytics uses scheduled jobs to collect and clean up analytics data.The API Name used when tracking API analytics is determined by the type of API being described, such as a REST API or a Scripted SOAP service.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Analyze REST and SOAP API usage, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# REST and SOAP API analytics collection and cleanup

API analytics uses scheduled jobs to collect and clean up analytics data.

The instance tracks all web service transactions for APIs on the inclusion list and maintains a daily history, aggregated by resource and HTTP action combination. Requester information is aggregated per requester, resource, and HTTP action combination and tracked up to the daily limit defined by the property **com.glide.api.stats.daily\_ limit**.

Refer to the following table to determine which requests are logged.

<table id="table_mdt_fkr_2x"><thead><tr><th>

API name

</th><th>

Example resource

</th><th>

Response code

</th><th>

Description

</th><th>

Logged

</th></tr></thead><tbody><tr><td>

now/table

</td><td>

/api/now/table/incident

</td><td>

Any except 401

</td><td>

Valid resource and table

</td><td>

Yes

</td></tr><tr><td>

now/table

</td><td>

/api/now/table/invalidResource

</td><td>

400

</td><td>

Valid resource but an invalid table

</td><td>

Yes

</td></tr><tr><td>

now/table

</td><td>

/api/now/table/incident

</td><td>

403

</td><td>

Requesting user has insufficient privileges

</td><td>

Yes

</td></tr><tr><td>

now/table

</td><td>

/api/now/table/incident

</td><td>

401

</td><td>

Requesting user is not authenticated

</td><td>

No

</td></tr><tr><td>

myApp/myScriptedApi

</td><td>

myApp/myScriptedApi/myResource

</td><td>

Any except 401

</td><td>

Valid resource

</td><td>

Yes

</td></tr><tr><td>

myApp/invalidApiName

</td><td>

-   myApp/invalidApiName
-   myApp/invalidApiName/myResource

</td><td>

400

</td><td>

Invalid API, even with a matching inclusion list entry

</td><td>

No

</td></tr></tbody>
</table>On the 2nd of each month, the API Monthly Stats scheduled job calculates the monthly total for each resource and HTTP action combination. Each day the API Monthly Requestor Stats scheduled job calculates the monthly total for each resource, requester, and HTTP action combination based on daily scores older than 2 days.

Daily statistics are maintained for 33 days. Monthly totals are maintained for 13 months. Table cleaners for the sys\_api\_stats, sys\_api\_stats\_requestor, and sys\_api\_stats\_requestor\_monthly tables remove analytics records older than these limits.

**Parent Topic:**[Analyze REST and SOAP API usage](c_APIAnalytics.md)

## REST &amp; SOAP API analytics naming

The **API Name** used when tracking API analytics is determined by the type of API being described, such as a REST API or a Scripted SOAP service.

<table id="table_dnf_n3b_55"><thead><tr><th>

API type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

REST

</td><td>

The API namespace and the first part of the URI following the namespace is used as the API name. For example, for the Table API endpoints `api/now/table/incident`and `api/now/table/problem`, the namespace and ID are **now/table**.

</td></tr><tr><td>

Direct SOAP \(table does not extend Import Set Row table\)

</td><td>

If the direct SOAP request accesses a table, Direct SOAP is used as the API name.

</td></tr><tr><td>

SOAP import \(table extends Import Set Row table\)

</td><td>

Import Set SOAP is used as the API name.

</td></tr><tr><td>

Scripted SOAP Services

</td><td>

The SOAP request endpoint page is used as the API name, such as my\_service.do.

</td></tr></tbody>
</table>