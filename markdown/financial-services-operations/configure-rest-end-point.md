---
title: Configure the REST End Point
description: The REST Endpoint record in ServiceNow stores the base URL, API version header, and connection properties for the Verifi API. Create two endpoint records: one for UAT testing and one for Production.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-02"
reading_time_minutes: 2
breadcrumb: [Configure, Verifi, Integrate, Financial Services Operations \(FSO\)]
---

# Configure the REST End Point

The REST Endpoint record in ServiceNow® stores the base URL, API version header, and connection properties for the Verifi API. Create two endpoint records: one for UAT testing and one for Production.

## Before you begin

Role required: admin

## Procedure

1.  Create the UAT Endpoint.

    1.  Navigate to System Web Services &gt; Outbound &gt; REST messages.

    2.  Select **New**.

    3.  Populate the following fields as shown:

        |Field|Value|
        |-----|-----|
        |Name|Verifi CDRN API — UAT.|
        |Description|Verifi CDRN — UAT / Integration Testing.|
        |Endpoint|https://verifiapitest.visa.com|
        |Authentication type|No Authentication \(JWT is included via the scripted header.|

    4.  Under HTTP Request, add the following default headers \(these apply to ALL methods\):

        |Header Name|Value|Notes|
        |-----------|-----|-----|
        |Accept|application/json|Required on all calls \(GET, POST, PATCH\).|
        |x-verifi-api-version|4.0|Must match the API version supported by your integration.|
        |x-verifi-issuer|$\{verifi\_issuer\_id\}|Populated at runtime from the Credential Store — see Section 5.|

        **Note:**

        Do not add Content-Type: application/json as a default header on the REST Message record. The Verifi guide specifies Content-Type is required on POST and PATCH requests only and not on GET requests. Set Content-Type at the individual HTTP Method level for each POST and PATCH method \(see Section 3.4\). Sending Content-Type on GET calls may cause the request to get rejected.

    5.  Select **Submit** to save the record.

    6.  Add HTTP Methods \(POST, GET, PATCH\)

    **Note:**

    The Verifi Issuer API supports HTTP/1.0 calls over HTTPS only. ServiceNow outbound REST defaults to HTTP/1.1. Confirm with your ServiceNow platform administrator whether HTTP version can be restricted at the REST Message or MID Server level, or verify with Verifi that HTTP/1.1 is accepted in practice before going live.

    |UAT / Test|https://verifiapitest.visa.com|4.0|
    |----------|------------------------------|---|
    |Environment|Base URL|API Version Header|
    |Production|https://verifiapi.visa.com|4.0|

2.  Create the production endpoint.

    |**Field**|**UAT Value**|**Production Value**|
    |---------|-------------|--------------------|
    |Name|Verifi CDRN API — UAT|Verifi CDRN API — Production|
    |Endpoint|https://verifiapitest.visa.com|https://verifiapi.visa.com|
    |Description|UAT / Integration Testing|Production environment — live transactions|

    **Note:** Do not point a UAT Issuer ID or Shared Secret at the Production endpoint. Doing so will result in rejected API calls and may generate alerts in the Verifi production environment.

3.  Enter HTTP Methods per Endpoint.

    Each REST Message record requires individual HTTP Method entries. Create the following methods under both the UAT and Production endpoint records.

    |HTTP Method|ServiceNow Method Name|Relative URL|Used For|
    |-----------|----------------------|------------|--------|
    |POST|Create Case|/issuers/cases|Submit a new CDRN dispute or inquire.|
    |GET|Get Case|/issuers/cases/$\{case\_id\}|Poll for status on a single case.|
    |GET|Get Multiple Cases|/issuers/cases?caseId=$\{case\_ids\}|Poll status for multiple cases in one call.|
    |PATCH|Update Case|/issuers/cases/$\{case\_id\}|Close or revoke a case.|
    |GET|Get Descriptor List|/issuers/descriptors|Retrieve eligible merchant descriptors \(optional\).|

    **Note:** The Authorization header containing the encoded JWT is set dynamically at runtime per call, not at the HTTP Method level.


**Parent Topic:**[Configuring Financial Services Operations Integration with Verifi](configure-financial-services-integration-with-verifi-cdrn.md)

