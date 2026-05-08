---
title: Install the ServiceNow Document Designer add-in
description: Install ServiceNow Document Designer add-in to your Microsoft Word document. This add-in is required to create audit and CAM report templates.
locale: en-US
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring ATO artifacts report templates, CAM reference, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Install the ServiceNow Document Designer add-in

Install ServiceNow Document Designer add-in to your Microsoft Word document. This add-in is required to create audit and CAM report templates.

## Before you begin

Ensure that the following plugins are activated:

-   sn\_grc\_doc\_design
-   sn\_outlook\_addin

Role required: sys\_admin

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Add-Ins for Office** &gt; **Office Add-In Manifests**.

2.  From the Office Manifests list, select **ServiceNow Document Designer**.

3.  Select **Download Manifest**.

4.  To enable the add-in, contact your Microsoft 365 account manager who can use the manifest file you downloaded in step 3.


## What to do next

For detailed instructions on how to deploy the manifest file, see the [Deploy add-ins in the Microsoft 365 admin center \[KB1307378\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1307378) article in the Now Support Knowledge Base.

To configure the HTTP response headers for add-in for Microsoft Word in the browser, see the [Response header resolution \[KB1434453\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1434453) article in the Now Support Knowledge Base.

-   **[Reference information for Document designer](../reference/properties-for-document-designer.md)**  
There are several properties that get installed with the Document designer plugin. These properties help to control the various aspects of how the plugin works.

**Parent Topic:**[Configuring ATO artifacts report templates](../../grc-cam/reference/cam-configure-word-based-template.md)

**Parent Topic:**[../concept/document-designer-template.md](../concept/document-designer-template.md)

