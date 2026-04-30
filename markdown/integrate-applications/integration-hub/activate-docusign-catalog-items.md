---
title: Activate Docusign eSignature spoke catalog items
description: Trigger events in Docusign when an item is requested in the Service Catalog. For example, The Send a Document for Digital Signature catalog item triggers a sample flow that sends a Docusign document to a designated recipient.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Docusign eSignature Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Activate Docusign eSignature spoke catalog items

Trigger events in Docusign when an item is requested in the Service Catalog. For example, The Send a Document for Digital Signature catalog item triggers a sample flow that sends a Docusign document to a designated recipient.

## Before you begin

-   Request IntegrationHub subscription
-   Activate Docusign eSignature spoke
-   Activate the Flow Designer support for the Service Catalog \(com.glideapp.servicecatalog.flow\_designer\) plugin
-   Role required: admin

## About this task

The Docusign eSignature spoke adds catalog items for use with the Docusign eSignature spoke sample flows. Before triggering a Docusign eSignature spoke sample flow, activate these catalog items.

|Catalog item|Description|
|------------|-----------|
|Send a Document for Digital Signature|Sends a document for digital signature in Docusign.|
|Demonstrate Template - Send Job Offer to Candidate|Sends a job offer using a Docusign template.|

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Maintain Items**.

2.  Search for and select **Send a Document for Digital Signature**.

3.  Click **Activate**.

4.  Open the record, **Send a Document for Digital Signature**.

5.  In the **Process Engine** tab, select **Send a Document for Digital Signature** for **Flow**.

6.  Search for and select **Send employment offer to candidate using DocuSign template**.

7.  Click **Activate**.

8.  Open the record, **Send employment offer to candidate using DocuSign template**.

9.  In the **Process Engine** tab, select **Send employment offer to candidate using DocuSign template** for **Flow**.


## Result

When one of these items is requested in the Service Catalog, the associated Docusign eSignature spoke sample flow triggers and performs actions in DocuSign.

