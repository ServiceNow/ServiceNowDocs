---
title: Configuring integration settings for ServiceNow services and components in AEM
description: You have to set up your ServiceNow services and components to integrate with your Adobe Experience Manager \(AEM\) instance.Define OSGi configuration settings for ServiceNow services used by ServiceNow components in Adobe Experience Manager \(AEM\).Configure log file settings for ServiceNow services in Adobe Experience Manager \(AEM\) to generate debug logs to help identify issues in the authentication process.Define a cross-origin resource sharing \(CORS\) rule on your ServiceNow instance to access endpoints of the Knowledge Management REST API, Case API, or CSM Attachment API from your Adobe Experience Manager \(AEM\) instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integrating with Adobe Experience Manager, Integrate, Customer Service Management]
---

# Configuring integration settings for ServiceNow services and components in AEM

You have to set up your ServiceNow services and components to integrate with your Adobe Experience Manager \(AEM\) instance.

## Settings to enable use of ServiceNow services in AEM

You can define the following types of configuration settings for ServiceNow services in AEM:

-   Authentication settings with a third-party OIDC provider \(see [Configure OIDC provider details in Adobe Experience Manager](../task/aem-setup-servicenow-authentication.md#)\).
-   Specific settings for ServiceNow services \(see [Define OSGi configuration settings for ServiceNow services](aem-integration-setup.md#)\).
-   Log file settings for ServiceNow services \(see [Configure log file settings for ServiceNow services in Adobe Experience Manager](aem-integration-setup.md#)\).

## Settings for using ServiceNow components in AEM

To use the Knowledge API endpoint on your AEM instance, you have to define the cross-origin resource sharing \(CORS\) rule on your ServiceNow instance. For more information, see [Define a cross-origin resource sharing rule \(CORS\) to access ServiceNow API endpoints from AEM](aem-integration-setup.md#).

## Define OSGi configuration settings for ServiceNow services

Define OSGi configuration settings for ServiceNow services used by ServiceNow components in Adobe Experience Manager \(AEM\).

### Before you begin

Role required: AEM administrator

### Procedure

1.  Access the web console in AEM using a URL in the following format: `https://<AEM_hostname>:<AEM_port>/system/console/configMgr`.

2.  Search for `ServiceNow Configuration`.

3.  In the **Name** column, click the **ServiceNow Configuration** link.

4.  Provide values for the configuration settings.

<table id="table_hxt_1zj_vkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base Instance URL

</td><td>

Complete URL of your ServiceNow instance.

</td></tr><tr><td>

Knowledge Bases

</td><td>

System identifier \(sys\_id\) of a knowledge base that contains associated knowledge articles. For multiple entries, separate the knowledge bases with commas. **Note:** A blank value indicates articles from all knowledge bases in your ServiceNow instance are accessible to a user with appropriate permissions.

</td></tr><tr><td>

Show Articles in All Languages

</td><td>

Option to show knowledge articles in all languages for ServiceNow components.

</td></tr></tbody>
</table>5.  Click **Save**.


## Configure log file settings for ServiceNow services in Adobe Experience Manager

Configure log file settings for ServiceNow services in Adobe Experience Manager \(AEM\) to generate debug logs to help identify issues in the authentication process.

### Before you begin

Role required: AEM administrator

### Procedure

1.  Access the web console in AEM using a URL in the following format: `https://<AEM_hostname>:<AEM_port>/system/console/configMgr`.

2.  Navigate to **OSGi** &gt; **Configuration**.

3.  Search for and select **logs/project-servicenow-components.log: info**.

4.  Verify the default field values, or fill in your own values for a custom configuration.

    |Field|Value|
    |-----|-----|
    |Log Level|Debug|
    |Log File|Path of the ServiceNow log file.|
    |Message Pattern|Message-format pattern for formatting log messages.|
    |Logger|Logger name for ServiceNow login services.|
    |Additivity|Option to disable sending logs to an appender attached higher in the hierarchy.|

5.  Click **Save**.


## Define a cross-origin resource sharing rule \(CORS\) to access ServiceNow API endpoints from AEM

Define a cross-origin resource sharing \(CORS\) rule on your ServiceNow instance to access endpoints of the Knowledge Management REST API, Case API, or CSM Attachment API from your Adobe Experience Manager \(AEM\) instance.

### Before you begin

Ensure that you have configured the API for which you are defining the CORS rule.

-   Activate the Knowledge API plugin \(sn\_km\_api\) to use the Knowledge Management REST API endpoints for knowledge articles. For more information, see [Knowledge Management REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/knowledge-api.md).
-   Activate the Customer Service plugin \(com.sn\_customerservice\) to use the Case API endpoints for customer service cases. For more information, see [Case API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/case-api.md).
-   Configure the **glide.rest.attachment\_csm\_api.allowed\_tables** system property and include the Case \[sn\_customerservice\_case\] table to use the CSM Attachment API end points for case attachments. For more information, see [CSM Attachment API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/attachment_csm-api.md).

Role required: web\_service\_admin

### About this task

### Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **CORS Rules**.

2.  Click **New**.

3.  On the CORS Rule form, fill in the fields.

<table id="table_o13_rs3_ls"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for identifying your CORS rule.

</td></tr><tr><td>

REST API

</td><td>

REST API this CORS rule applies to. -   For knowledge articles, select **Knowledge Management REST API \[sn\_km\_api/knowledge\]**.
-   For customer service cases, select **Case \[sn\_customerservice/case\]**.
-   For case attachments, select **CSM Attachment API \[now/attachment\_csm\]**


</td></tr><tr><td>

Domain

</td><td>

AEM instance that this CORS rule applies to.

</td></tr><tr><td>

Max age

</td><td>

Number of seconds to cache the client session.

</td></tr></tbody>
</table>4.  In the HTTP Methods related list, select HTTP methods to send a request to a web service provider.

    -   For knowledge articles, select **GET**.
    -   For customer service cases, select **GET**, **PUT**, **POST**.
    -   For case attachments, select **GET**, **POST**, **DELETE**.
5.  For Case API, in the **Exposed headers** field of the HTTP Headers related list, enter `X-Total-Count`.

6.  Click **Submit**.


