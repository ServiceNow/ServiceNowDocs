---
title: REST APIs for third-party integration with Security Operations
description: The Security Operations base system includes a series of scripted REST APIs that allow customers and partners to easily integrate with an existing Security Operations deployment. The APIs allow you to gather data from outside of your system \(for example, a Python script is used to receive data from VirusTotal\) and send it back to your instance.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# REST APIs for third-party integration with Security Operations

The Security Operations base system includes a series of scripted REST APIs that allow customers and partners to easily integrate with an existing Security Operations deployment. The APIs allow you to gather data from outside of your system \(for example, a Python script is used to receive data from VirusTotal\) and send it back to your instance.

Scripts written in almost any language \(Python, for example\) can be used with the APIs to perform customer-specific processes. The scripts must be written in a language able to make an outside-facing HTTP Post call. For example, if you have a Java application, you must use a library, such as the `java.net.HttpUrlConnection` package, to construct an HTTP call and pass in a JSON string as Body for the message.

The API is solely used to add data that was gathered outside of our system. For example, if you entered VT python script and received data from VT, you could send that data back to the SN instance.

## Authentication

All operations within the API definitions use platform authentication provided by the [Scripted REST APIs](https://www.servicenow.com/docs/access?context=c_CustomWebServices&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) operation feature. To access, navigate to **System Web Services** &gt; **Scripted Web Services** &gt; **Scripted REST APIs** and locate the **SecOps Integration Capabilities** API.

![Scripted REST Service](../../../common/image/Scripted_REST_Service.png "Scripted REST Service")

The user and the user’s domain are readily available within the context of the API. Records can be tied to a user, an audit path to be established, and domain separation accomplished. Also, since you are authenticated as a specific user, you can use [Using GlideRecordSecure](https://www.servicenow.com/docs/access?context=p_GlideServerAPIs&version=xanadu&pubname=xanadu-application-development&section=c_UsingGlideRecordSecure&ft:locale=en-US) to prevent any unauthorized access to data.

## Authorization

To protect the record creation process from users outside of the Security Operations application, you must have the sn\_sec\_cmn.api\_write role. Only users with this role can access the APIs.

## Configuration request parameters

The following request parameters are available.

|Name|Default|Description|
|----|-------|-----------|
|ignore\_mandatory\_fields|false|If set to true, the record persists even if mandatory fields are not filled in.|
|include\_wrap|false|If set to true, the response includes the instance-provided standard wrapper for Scripted REST APIs.|
|simple\_response|false|If set to true, the response includes only whether the operation was successful.|

## Error responses

The following error responses may occur.

|Error message|When does it occur?|Solution|
|-------------|-------------------|--------|
|Insufficient access|User does not have the sn\_sec\_cmn.api\_write role.|Add the role to the user.|
|Invalid post body|Request body is empty or an empty object.|Conform to the API definition.|
|No fields supplied|Data fields provided to persist are empty.|Conform to the API definition.|
|Mandatory fields missing: x,y,z|Mandatory fields are missing.|Conform to the table definition of the target table or set **ignore\_mandatory\_fields** to true.|
|Unable to persist record|Unable to persist parsed record.|GlideRecord insert\(\) failed, further analysis is required.|
|Unknown error|Occurs if no known error path has been followed.|Further analysis is required.|

## CI enrichment use case

Using your third-party scripts, you can write to the Configuration Item Enrichment \[sn\_sec\_cmn\_ci\_enrichment\_result\] table for CI enrichment. The enrichment records are based on existing capabilities that provide detailed information about a record from a third-party source.

Sample request and responses for the CI enrichment use case are shown here.

![CI Enrichment: Create –Request](../image/CreateRequestForCIEnrichment.png "Create-Request for CI enrichment")

![CI Enrichment: Create –Response](../image/CIEnrichmentCreateResponse.png "Create-Response for CI enrichment")

## Observable enrichment use case

Using your third-party scripts, you can write to the Observable Enrichment Result `[sn_ti_observable_enrichment_result]` table for observable enrichment. The enrichment records are based on existing capabilities that provide detailed information about a record from a third-party source.

Sample request and responses for the observable enrichment use case are shown here.

![Observable Enrichment: Create–Request](../image/ObservableEnrichmentCreateRequest.png "Create-Request for observable enrichment")

![Observable Enrichment: Create Response](../image/ObservableEnrichmentCreateResponse.png "Create-Response for observable enrichment")

**Note:** In addition to enriching existing records, you can also use [Security Operations enrichment data mapping](enrichment-data-mapping.md) to add new records to tables by passing in an **enrichment\_mapping\_id** for an existing enrichment mapping and a corresponding **raw\_data** string that can be parsed by the mapping process.

## Threat lookup use case

Using your third-party scripts, you can write to the Threat Lookup Result \[sn\_ti\_lookup\_result\] table for threat lookup results. The lookup records are based on existing capabilities that provide detailed information about a record from a third-party source.

Sample request and responses for the threat lookup use case are shown here.

![Create-Request for threat lookups](../image/ThreatLookupCreateRequest.png "Create-Request for threat lookups")

![Create-Response for threat lookups](../image/ThreatLookupCreateResponse.png "Create-Response for threat lookups")

**Parent Topic:**[Security Operations Integration Reference](../../secops-integration-reference/concept/secops-integ-ref.md)

