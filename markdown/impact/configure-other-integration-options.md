---
title: Configure other integration options
description: Configure the Other integration to create work items in any external system by using a payload script, an endpoint, a username, and an API token.The following leading practices are guidelines for creating other integration type scripts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/configure-other-integration-options.html
release: australia
topic_type: task
last_updated: "2026-11-12"
reading_time_minutes: 3
breadcrumb: [Scan Engine integrations, Configuring Impact, Impact]
---

# Configure other integration options

Configure the Other integration to create work items in any external system by using a payload script, an endpoint, a username, and an API token.

## Before you begin

The API endpoint URL, the username, and the API token for your external system must be available. The request body format that the external system expects must also be known, because the payload script must produce it.

**Note:** See [Other integration leading practices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-other-integration-options.md) for available script variables and leading practices.

Configure this integration on the instance where Scan Engine runs and the findings are generated. You don't select a target instance, and no My SN Instances record is required.

Role required: Scan Engine admin \(`sn_se.scan_engine_admin`\). Only users with this role can edit the Payload script.

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties** and select the **User Story Integration** properties tab.

2.  Set **Integration** to `Other`.

3.  Populate the fields.

<table><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Integration

</td><td>

Read-only field that autopopulate the integration type as Other.

</td></tr><tr><td>

Integration Name

</td><td>

A descriptive name for this integration.

</td></tr><tr><td>

End Point

</td><td>

The full URL of the API end point to call. **Note:** Select the lock icon next to the field to enter the URL.

</td></tr><tr><td>

Content Type

</td><td>

The content type required by the external API with a maximum string of 100. For example, `application/json`\).

</td></tr><tr><td>

Issue Type

</td><td>

The issue type for the work item required by the external API with a maximum string of 100 to create in the external system.

</td></tr><tr><td>

Payload

</td><td>

-   The script that builds the request body.
-   Turn on ECMAScript 2021 \(ES12 mode: Enables the latest supported JavaScript features for this script; otherwise the application's JavaScript features will be used.


</td></tr><tr><td>

Username

</td><td>

The username for the external system.

</td></tr><tr><td>

API Token

</td><td>

The API token for the external system. The username and API token are used in a basic authentication authorization header. See the security note that follows these steps.**Important:** The API token field is a text field, so the platform doesn't encrypt its value by default. If your organization uses Edge Encryption, you can encrypt this field. Restrict access to Scan Engine Properties to users who need it, and use a token with the narrowest access your external system allows.

</td></tr></tbody>
</table>4.  Select **Update** to save the configuration.


**Parent Topic:**[Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/instance-integration-scan-engine.md)

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


