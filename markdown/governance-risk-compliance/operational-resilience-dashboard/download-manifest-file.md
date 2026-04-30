---
title: Download the manifest file
description: Install ServiceNow Document designer manifest file. This add-in should be enabled for customizing the reports and Microsoft Word templates, according to your business needs.
locale: en-US
release: yokohama
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-11-16"
reading_time_minutes: 1
breadcrumb: [Generating Word reports using Document designer, Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Download the manifest file

Install ServiceNow Document designer manifest file. This add-in should be enabled for customizing the reports and Microsoft Word templates, according to your business needs.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

An Office add-in manifest file is an XML \(or JSON for unified manifests\) file that describes an add-in to Microsoft Word, including its name, ID, version, and permissions. It specifies how the add-in integrates with Microsoft Word, such as defining custom UI elements like ribbon buttons and the HTML files for its UI.

## Before you begin

Verify that the following plugins are activated:

-   sn\_grc\_doc\_design
-   sn\_outlook\_addin

Role required: sys\_admin

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Add-Ins for Office** &gt; **Office Add-In Manifests**.

2.  From the Office Manifests list, select **ServiceNow Document Designer**.

3.  Select **Download Manifest**.

    The manifest file is downloaded in your local drive.

    ![Office manifest file for Document Designer.](../../grc-business-continuity-management/image/download-manifest.png)

4.  To enable the add-in, contact your Microsoft 365 account manager who can use the manifest file you downloaded in step 3.


## What to do next

For detailed instructions on how to deploy the manifest file, see the [Deploy add-ins in the Microsoft 365 admin center \[KB1307378\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1307378) article in the Now Support Knowledge Base.

To configure the HTTP response headers for add-in for Microsoft Word in the browser, see the [Response header resolution \[KB1434453\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1434453) article in the Now Support Knowledge Base.

