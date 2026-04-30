---
title: Workflow of Management Reporting of Risk
description: The Management Reporting of Risk integration utilizes a workflow that requires participation from multiple user roles such as system administrators, Risk administrators, and Risk managers. By defining a clear workflow, individuals and teams can better understand their roles and responsibilities and generate the necessary reports.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrating Microsoft 365 with Management Reporting of Risk, Integrate, Risk Management, Governance, Risk, and Compliance]
---

# Workflow of Management Reporting of Risk

The Management Reporting of Risk integration utilizes a workflow that requires participation from multiple user roles such as system administrators, Risk administrators, and Risk managers. By defining a clear workflow, individuals and teams can better understand their roles and responsibilities and generate the necessary reports.

The following figure displays the complete workflow of using the Management Reporting of Risk integration to generate reports in a Microsoft Word document.

![Detailed workflow of how you can add the Management Reporting of Risk plugin in your MS word document.](../image/workflow-management-reporting-of-risk.jpg "Process flow for Management Reporting of Risk integration")

To generate Microsoft Word reports:

1.  Download the ServiceNow Reporting add-in: As a system administrator, download and install the Risk manifest file. A manifest file contains information about the files included in a software application or package. It’s used by the software installer to ensure that all the necessary files are installed in the correct locations. At this stage, you must also work with your Microsoft 365 administrator to upload the manifest file to the Microsoft Word application. The Microsoft 365 administrator has the necessary access rights.
2.  As a Risk administrator, set up the Microsoft 365 reporting configuration records to specify which tables, reports, and charts from your ServiceNow® instance must be used to import data into your Microsoft Word. You can also specify the columns from a table from which you want to import data.
3.  As a Risk administrator, you can configure additional reporting filters. These filters specify at a granular level what data must be imported to the disclosure report from a table.
4.  As a Risk manager, go to your Microsoft Word document, authenticate yourself with the ServiceNow® credentials, and import the data from your instance to the document. You can alter the formatting of the data according to your preferences.

