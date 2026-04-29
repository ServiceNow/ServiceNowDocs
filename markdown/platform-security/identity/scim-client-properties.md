---
title: SCIM Client properties, tables, scriptable APIs, and logs
description: The SCIM v2 - ServiceNow Cross-domain Identity Management Client \(com.snc.integration.scim2.client\) plugin includes the following system properties, tables, scriptable APIs, and logs.
locale: en-US
release: australia
product: Identity
classification: identity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [SCIM Client, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# SCIM Client properties, tables, scriptable APIs, and logs

The SCIM v2 - ServiceNow Cross-domain Identity Management Client \(com.snc.integration.scim2.client\) plugin includes the following system properties, tables, scriptable APIs, and logs.

## Properties

SCIM Client adds the following system properties.

<table id="table_zyl_dyx_ctb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**com.snc.integration.scim2.client.log.request.status**

</td><td>

This property determines whether to write all the log records or just the error log records. The possible values are **FAILURE** or **ALL**.Default value: **ALL**

</td></tr><tr><td>

**com.snc.integration.scim2.client.log.cleanup.duration**

</td><td>

This property determines the number of days for clearing the logs.Default value: **180**

</td></tr></tbody>
</table>To set the properties, navigate to **All** &gt; **SCIM** &gt; **SCIM Client Properties**.

## Tables

The SCIM Client adds the following tables.

|Name|Description|
|----|-----------|
|SCIM Provider \(sys\_scim\_provider\)|Stores data for each SCIM provider, such as the name, REST message resource definitions, and so on.|
|SCIM Provider Resource Mapping \(sys\_scim\_provider\_resource\_mapping\)|Stores the primary table information for each provider and resource name.|
|SCIM Attribute Mapping \(sys\_scim\_attribute\_mapping\)|Stores the source details where each SCIM attribute value should come from, such as the table field, script, and so on.|
|SCIM Client Log \(sys\_scim\_client\_logs\)|Stores the statuses of each call triggered to SCIM Provider.|

## Scriptable API

The SCIM2Client API calls the System for Cross-domain Identity Management \(SCIM\) Provider \(server role\) to create, update, or delete data in a service provider \(SP\). The scriptable API of the SCIM Client should be used in the scripts that are running in the system context or by a system admin user.

For example, you can use the script while running the integration hub workflow as a system user, while running the scheduled jobs, and so on.

The following are some of the use cases for using the scriptable APIs:

-   As an admin, provision identity information from background scripts, business rules, script include calls, workflows, and so on.
-   As an admin, run a scheduled job or an on-demand job for identity provisioning.
-   Run a workflow or sub-workflow with the Script step using the provision scriptable API call.
-   Add the provision script directly in a business rule or script include. The script can be triggered by non-admin users. This use-case works in the following situations:
    -   The user has access to the token, meaning that the user has the role to generate the token from the REST template.
    -   The user has access to retrieve the SCIM attribute values from the mapped tables.

To know more about the scriptable API, see [SCIM2Client API](https://www.servicenow.com/docs/access?context=SCIM2ClientAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).

## SCIM Client Logs

The SCIM Client Logs display the provisioning status about the SCIM APIs. To view the provisioning status, navigate to **All** &gt; **SCIM** &gt; **SCIM Client Logs**.

