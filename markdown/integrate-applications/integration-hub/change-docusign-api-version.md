---
title: Change the Docusign API version
description: By default, the Docusign spoke sends REST API requests to Docusign API v2. For forward compatibility and to take advantage of Docusign's newer API, you can update a connection attribute to send API requests to Docusign API v2.1.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Docusign eSignature Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Change the Docusign API version

By default, the Docusign spoke sends REST API requests to Docusign API v2. For forward compatibility and to take advantage of Docusign's newer API, you can update a connection attribute to send API requests to Docusign API v2.1.

## Before you begin

Role required: admin

## About this task

To understand the difference between the two APIs, see the [Docusign Developer](https://developers.docusign.com/) site.

## Procedure

1.  Navigate to **All** &gt; **Docusign** &gt; **Connection Aliases**.

2.  Open the connection alias that you want to update the version for.

    Only requests sent using this alias use the new API version. For example, if you want to update the API version for all requests and your implementation uses multiple connection aliases, you must update each connection alias.

3.  In the **Connection Attributes** related list, add or edit the **API Version** record.

    |Field|Value|
    |-----|-----|
    |Type|String|
    |Label|API Version|
    |Column name|api\_version|
    |Default value|v2.1|

4.  Save or submit the record.


## Result

When the Docusign spoke makes an API request, it uses the API version designated in the connection attribute **Default value** field.

