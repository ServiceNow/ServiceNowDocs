---
title: Configure other integration options
description: Configure the Other integration type to create work items in any external system using a custom payload script and basic authentication.The following leading practices are guidelines for creating other integration type scripts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/configure-other-integration-options.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-05-05"
reading_time_minutes: 2
breadcrumb: [Scan Engine integrations, Configure the Impact Store Application, Configuring Impact, Impact]
---

# Configure other integration options

Configure the Other integration type to create work items in any external system using a custom payload script and basic authentication.

## Before you begin

Confirm the API endpoint URL and request body format required by your external system. The payload script must produce a request body in the format your system expects.

Role required: Scan Engine admin \(sn\_se.scan\_engine\_admin\)

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties** and select the **User Story Integration** properties tab.

2.  Set **Integration Type** to `Other`.

3.  Populate the following fields.

    |Field|Value|
    |-----|-----|
    |Integration name|A descriptive name for this integration.|
    |Endpoint|The full URL of the API to call. Determine what the API expects in the request body to format the payload correctly.|
    |Content type|The content type required by the external API \(for example, `application/json`\).|
    |Issue type|The work item type to create in the external system.|

4.  In the **Payload** field, enter the script that builds the request body.

    The credentials provided on the form are used in a basic authentication authorization header. See [Other integration leading practices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-other-integration-options.md) for available script variables and leading practices.

5.  Enter the **Username** and **API token** for authentication.


**Parent Topic:**[Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/instance-integration-scan-engine.md)

## Other integration leading practices

The following leading practices are guidelines for creating other integration type scripts.

### Script variables

The payload script runs on the ServiceNow instance when a work item is created. Use the `payload` variable to build the request body in the format your external system requires. The script output is sent as the request body to the configured endpoint using basic authentication.

|Variable|Description|
|--------|-----------|
|`payload`|The content to send in the request body. Structure this object to match the format expected by your external API.|
|`grFinding`|GlideRecord of the finding. Use this to read finding data for the request body.|
|`workItemType`|The work item type selected for this integration.|

### Leading practices

-   **Review your target API documentation before writing the script**

    The external system's API determines the required request body format, field names, and data types. Review the API documentation for your target system before building the `payload` object to avoid silent mapping failures.

-   **Match the payload structure to the API's expected format**

    Set the **Content type** field and the structure of `payload` to match what the API expects. For a JSON API, build `payload` as a plain JavaScript object — it will be serialized automatically. For other formats, construct the payload string directly.

-   **Use grFinding to include finding context**

    Read finding fields using standard GlideRecord methods on `grFinding` and map them to the fields your external system expects. For example, `grFinding.getValue('short_description')` can populate a title or summary field.

-   **Enable ES12 mode for modern JavaScript**

    To use modern JavaScript syntax, enable **ECMAScript 2021 \(ES12\) mode** in Scan Engine Properties before writing your payload script.


