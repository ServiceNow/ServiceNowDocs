---
title: Install the ServiceNow Reporting add-in for risk reporting
description: Install the ServiceNow Reporting add-in to your Microsoft Word document. This add-in is required to import reports and data from your ServiceNow instance to Microsoft Word documents to create risk reports.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrating Microsoft 365 with Management Reporting of Risk, Integrate, Risk Management, Governance, Risk, and Compliance]
---

# Install the ServiceNow Reporting add-in for risk reporting

Install the ServiceNow Reporting add-in to your Microsoft Word document. This add-in is required to import reports and data from your ServiceNow® instance to Microsoft Word documents to create risk reports.

## Before you begin

Ensure that the following plugins are activated:

-   sn\_esg\_msoff\_intg
-   sn\_outlook\_addin
-   sn\_grc\_mgmt\_report

Role required: sys\_admin

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Add-Ins for Office** &gt; **Office Add-In Manifests**.

2.  From the Office Manifests list, select **ServiceNow Reporting**.

3.  Select **Download Manifest**.

4.  To enable the add-in, contact your Microsoft 365 account manager who can use the manifest file you downloaded in step 3.


## What to do next

For detailed instructions on how to deploy the manifest file, see the [Deploy add-ins in the Microsoft 365 admin center \[KB1307378\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1307378) article in the Now Support knowledge base.

To configure the HTTP response headers for the add-in for Microsoft Word in the browser, see the [Response header resolution \[KB1434453\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1434453) article in the Now Support knowledge base.

