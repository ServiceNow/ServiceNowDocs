---
title: Activate Adobe Sign spoke catalog items
description: Trigger events in Adobe Sign when an item is requested in Service Catalog. For example, the Adobe Sign - Statement of Work Demo catalog item triggers a sample flow that sends a Adobe Sign document to a designated recipient.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Adobe Sign Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Activate Adobe Sign spoke catalog items

Trigger events in Adobe Sign when an item is requested in Service Catalog. For example, the Adobe Sign - Statement of Work Demo catalog item triggers a sample flow that sends a Adobe Sign document to a designated recipient.

## Before you begin

-   [Synchronize Adobe Sign group with ServiceNow](setup-adobe-sign.md#)
-   Role required: admin

## About this task

The Adobe Sign spoke adds catalog items for use with the Adobe Sign spoke sample flows. Before triggering a sample flow, activate these catalog items.

|Catalog item|Description|
|------------|-----------|
|Adobe Sign - Statement of Work Demo|Sends a statement of work for digital signature using a Adobe Sign library document.|
|Adobe Sign - Send NDA Demo|Sends a non-disclosure agreement for digital signature using a Adobe Sign library document.|

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Service Catalog**.

2.  Click the add content icon ![Add Content icon](../image/add-content-icon.png).

3.  Search for and select **Adobe Sign - Statement of Work Demo**.

4.  Click **Add here**.

5.  Search for and select **Adobe Sign - Send NDA Demo**.

6.  Click **Add here**.


## Result

When one of these items is requested in the Service Catalog, the associated Adobe Sign spoke sample flow is triggered and necessary actions are performed in Adobe Sign.

