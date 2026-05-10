---
title: Define an external knowledge source
description: Before you import content, create and configure the connection between the a Web Distributed Authoring and Versioning \(WebDAV\) - compliant external knowledge source and the ServiceNow knowledge base into which you want to import content. Define import parameters for the external knowledge source.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration with external knowledge sources, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Define an external knowledge source

Before you import content, create and configure the connection between the a Web Distributed Authoring and Versioning \(WebDAV\) - compliant external knowledge source and the ServiceNow knowledge base into which you want to import content. Define import parameters for the external knowledge source.

## Before you begin

Define [Basic authentication credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_BasicAuthCredentialsForm.md) and [Getting started with connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/connection-information.md) to the external source.

**Caution:**

This feature expects that the external source endpoint is a publicly accessible endpoint. Mid-server configuration is not supported.

Role required: admin

## About this task

Only basic authentication is supported for the external content integration feature.

## Procedure

1.  Define the connection from the external source and the target knowledge base.

    1.  Navigate to **Knowledge** &gt; **Administration** &gt; **External Knowledge Sources**.

    2.  Click **New**.

    3.  Fill in the following fields:

        |Field|Instruction|
        |-----|-----------|
        |Name|Enter unique name for the external source.|
        |Target Knowledge Base|Select the knowledge base in which you want to create articles for the external content.|
        |Connection Alias|Select the connection alias to connect to the external source.|

    4.  Right-click the form header and click **Save**.

2.  Set import parameters for the external content.

    1.  In the **Parameter** related list, click **New**.

    2.  In the **Name** field, select the name of the parameter from the drop-down list.

    3.  In the **Value** field, enter the desired value for the parameter.

        The table below lists the parameters and the corresponding values that can be set for the external source.

        |Parameter Name|Instructions|
        |--------------|------------|
        |Maximum size limit \(in MB\) for this source|Set maximum allowed content size for this source. Once this limit is reached, no further content is processed. Default value is 400 MB.|
        |Maximum size limit \(in KB\) per file/content in this source|Set maximum allowed size limit for each file from this external source. If a file exceeds this limit, that file is not processed. Default value is 4000 KB.|
        |Open search results in the original source system|Set value to **true** to open search results in the external source system. Set value to **false** to open search results in the target knowledge base. Default value is set to **false**.|
        |Include folders with names that match these regex patterns|Enter a comma-separated list of regular expressions for folder names that need to be included from this external source.|
        |Exclude folders with names that match these regex patterns|Enter a comma-separated list of regular expressions for folder names that need to be excluded from this external source.|
        |Create articles when file names match these regex patterns|Enter a comma-separated list of regular expressions for file names that need to be included to create articles.|
        |Do not create articles when file names match these regex patterns|Enter a comma-separated list of regular expressions for file names that need to be excluded to create articles.|
        |Maximum retry limit|Maximum number of retries to send request to the external source.|

    4.  Click **Submit**.


**Parent Topic:**[Integration with external knowledge sources](../concept/knowledge-external-content-integration.md)

