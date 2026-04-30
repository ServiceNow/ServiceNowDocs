---
title: Sample configuration for integrating external knowledge content
description: You can integrate content from multiple external sources so your users can acquire and search knowledge from a single location. Use this sample configuration to create a connection to your external account, configure external knowledge sources, and import content to enable search results for unified content.Create authentication credentials and a connection alias to connect your external knowledge source to the ServiceNow Knowledge Management application. Define import parameters for your external source to import integrated content.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Integration with external knowledge sources, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Sample configuration for integrating external knowledge content

You can integrate content from multiple external sources so your users can acquire and search knowledge from a single location. Use this sample configuration to create a connection to your external account, configure external knowledge sources, and import content to enable search results for unified content.

## Requirements for integrating external content

Make sure the Knowledge Management -- External Content Integration plugin \(com.snc.knowledge.external\_integration\) is enabled and your external source is WebDAV- compliant.

**Parent Topic:**[Integration with external knowledge sources](knowledge-external-content-integration.md)

## Integrate external knowledge sources into the Knowledge Management application

Create authentication credentials and a connection alias to connect your external knowledge source to the ServiceNow Knowledge Management application. Define import parameters for your external source to import integrated content.

### Before you begin

Role required: admin

### Procedure

1.  Enable basic authentication on your external account.

    **Note:** Your external account password is not affected when you enable basic authentication.

2.  Create the connection to your external account using the basic authentication credentials.

    1.  Navigate to **Connections and Credentials** &gt; **Credentials**.

    2.  Click **New**.

    3.  Click **Basic Auth Credentials**.

        Fill in the following fields:

        |Field|Description|
        |-----|-----------|
        |Name|Name for the credential. For example, `Demo_Auth`.|
        |User name|The external account user name created for basic authentication.|
        |Password|The external account password for the user name.|

    4.  Click **Submit**.

3.  Create an HTTP connection to your external account.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    2.  Select **New**.

    3.  In the **Name** field, enter the name of the connection alias.

        For example, `Demo_Account`.

    4.  Right-click the form header and click **Save**.

    5.  In the **Connections** related list, click **New**.

        Fill in the following fields:

<table id="table_kjk_wyn_b2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the HTTP connection. For example, `Demo_Connection`.

</td></tr><tr><td>

Credential

</td><td>

Credential created to connect to the external account. For example, `Demo_Auth`.

</td></tr><tr><td>

Connection URL

</td><td>

WebDAV URL to your external account. This is the WebDAV end point of your external account.**Note:** You can also import contents from a specific folder by appending the folder path to the URL. For example, https://&lt;web link to your extermal\_account&gt;/KnowledgeIT.

</td></tr></tbody>
</table>    6.  Click **Submit**.

4.  Configure the external knowledge source for importing content.

    1.  Navigate to **Knowledge** &gt; **Administration** &gt; **External Knowledge Sources**.

    2.  Click **New** and fill in the following fields:

        |Field|Description|
        |-----|-----------|
        |Name|Unique name for the external source. For example, `Demo_knowledge`.|
        |Target Knowledge Base|Knowledge base in which you want to create articles for the external content. For example, `IT`.|
        |Connection Alias|Connection alias to connect to the external source. For example, `Demo_Account`.|

    3.  Right-click the form header and select **Save**.

    4.  In the Parameter related list, click **New**.

    5.  On the Parameter form, select the name of the import parameter that you want to configure for your external source and then set the value for the parameter.

        The table below lists the parameters and the corresponding values that can be set for the external source.

        |Parameter name|Value|
        |--------------|-----|
        |Maximum size limit \(in MB\) for this source|Maximum allowable content size to import from your external source. For example, `250 MB`.|
        |Maximum size limit \(in KB\) per file/content in this source|Maximum allowable size for each article, including attachments, that you can import from this external source. For example, `2000 KB`.|
        |Open search results in the original source system|Opens search results in the external source system if this value is set to **true**.|
        |Include folders with names that match these regex patterns|Comma-separated list of regular expressions for folder names to include from this external source. For example, to include all folders names that start with the letters a and b, enter `a.*,b.*`.|
        |Exclude folders with names that match these regex patterns|Comma-separated list of regular expressions for folder names to exclude from this external source. For example, to exclude all folders names that start with the letters a and b, enter `a.*,b.*`.|
        |Create articles when file names match these regex patterns|Comma-separated list of regular expressions for file names that to include when creating articles. For example, to include all file names have `.docx` and `.pdf`extensions, enter `.*\.docx,.*\.pdf`.|
        |Do not create articles when file names match these regex patterns|Comma-separated list of regular expressions for file names to exclude when creating articles. For example, to exclude file names have `.docx` and `.pdf`extensions, enter `.*\.docx,.*\.pdf`.|
        |Maximum retry limit|Maximum limit for the number of times a connection request can be sent to the external source. For example, `5`.|


### What to do next

[Import content from an external knowledge source](../task/run-import-job-external-content-integration.md).

**Related topics**  


[Open knowledge search results in source system](../task/open-search-results-ext-content.md)

[Knowledge Management Service portal search results page](knowledge-service-portal-search.md)

