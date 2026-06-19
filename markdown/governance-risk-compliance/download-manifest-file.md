---
title: Download the manifest file
description: Install ServiceNow Document designer manifest file. This add-in should be enabled for customizing the reports and Microsoft Word templates, according to your business needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/download-manifest-file.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Generating Microsoft Word reports using Document designer, Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Download the manifest file

Install ServiceNow Document designer manifest file. This add-in should be enabled for customizing the reports and Microsoft Word templates, according to your business needs.

## About this task

An Office add-in manifest file is an XML \(or JSON for unified manifests\) file that describes an add-in to Microsoft Word, including its name, ID, version, and permissions. It specifies how the add-in integrates with Microsoft Word, such as defining custom UI elements like ribbon buttons and the HTML files for its UI.

Starting withDigital Resilience Incident Reporting, version 22.3.0, the manifest of the Document designer add-in is merged with the manifest of the Microsoft 365 reporting add-in. As a result, when you side-load the Document designer with Word add-in, the **Add Content** and **Manage Content** icons \(that previously shipped only with the Microsoft 365 reporting add-in\) are now available in the same task pane in a Microsoft Word document as shown in the example.

\[Omitted image "document-designer-add-manage-content-icons.png"\] Alt text: Microsoft Word toolbar with the Document Designer task pane open, showing Add Content and Manage Content icons.

You can use the icons to insert Microsoft 365 reporting items into a Microsoft Word template without installing a second add-in.

## Before you begin

Role required: sys\_admin

Verify that the following plugins are activated with the sys\_admin role.

-   sn\_grc\_doc\_design
-   sn\_outlook\_addin

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Add-Ins for Office** &gt; **Office Add-In Manifests**.

2.  From the Office Manifests list, select **ServiceNow Document Designer**.

3.  Select **Download Manifest**.

    The manifest file is downloaded in your local drive.

    \[Omitted image "download-manifest.png"\] Alt text: Office manifest file for Document Designer.

4.  To enable the add-in, contact your Microsoft 365 account manager who can use the manifest file you downloaded in step 3.

5.  Verify that the add-in is loaded in Microsoft Word.

    1.  Open Microsoft Word.

    2.  Select **Insert** &gt; **Add-ins** &gt; **My Add-ins**.

    3.  Verify that ServiceNow Document designer is listed.


## What to do next

To build the Microsoft Word template using the add-in, see [Build the Microsoft Word template using the add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/build-word-template-using-add-in.md).

For detailed instructions on how to deploy the manifest file, see the [Deploy add-ins in the Microsoft 365 admin center \[KB1307378\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1307378) article in the Now Support Knowledge Base.

To configure the HTTP response headers for add-in for Microsoft Word in the browser, see the [Response header resolution \[KB1434453\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1434453) article in the Now Support Knowledge Base.

