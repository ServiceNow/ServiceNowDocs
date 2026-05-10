---
title: Define a cross-origin resource sharing rule \(CORS\) to access ServiceNow API endpoints from AEM
description: Define a cross-origin resource sharing \(CORS\) rule on your ServiceNow instance to access endpoints of the Knowledge Management REST API, Case API, or CSM Attachment API from your Adobe Experience Manager \(AEM\) instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Define a cross-origin resource sharing rule \(CORS\) to access ServiceNow API endpoints from AEM

Define a cross-origin resource sharing \(CORS\) rule on your ServiceNow instance to access endpoints of the Knowledge Management REST API, Case API, or CSM Attachment API from your Adobe Experience Manager \(AEM\) instance.

## Before you begin

Ensure that you have configured the API for which you are defining the CORS rule.

-   Activate the Knowledge API plugin \(sn\_km\_api\) to use the Knowledge Management REST API endpoints for knowledge articles. For more information, see [Knowledge Management REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/knowledge-api.md).
-   Activate the Customer Service plugin \(com.sn\_customerservice\) to use the Case API endpoints for customer service cases. For more information, see [Case API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/case-api.md).
-   Configure the **glide.rest.attachment\_csm\_api.allowed\_tables** system property and include the Case \[sn\_customerservice\_case\] table to use the CSM Attachment API end points for case attachments. For more information, see [CSM Attachment API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/attachment_csm-api.md).

Role required: web\_service\_admin

## About this task

## Procedure

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


