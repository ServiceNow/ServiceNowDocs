---
title: Workflow of Microsoft 365 for ServiceNow Reporting
description: The Microsoft 365 for ServiceNow Reporting integration utilizes a workflow that requires participation from multiple user roles such as system administrators, ESG administrators, and disclosure managers. By defining a clear workflow, individuals and teams can better understand their roles and responsibilities and generate the necessary disclosures.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating Microsoft 365 with ServiceNow reporting, Integrating ESG Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Workflow of Microsoft 365 for ServiceNow Reporting

The Microsoft 365 for ServiceNow Reporting integration utilizes a workflow that requires participation from multiple user roles such as system administrators, ESG administrators, and disclosure managers. By defining a clear workflow, individuals and teams can better understand their roles and responsibilities and generate the necessary disclosures.

To generate Microsoft Word disclosures:

1.  Download the ServiceNow Reporting add-in: As a system administrator, download and install the ESG manifest file. A manifest file contains information about the files included in a software application or package. It is used by the software installer to ensure that all the necessary files are installed in the correct locations. At this stage, you must also work with your Microsoft 365 administrator to upload the manifest file to the Microsoft Word application. The Microsoft 365 administrator has the necessary access rights.
2.  As an ESG administrator, set up the Microsoft 365 reporting configuration records to specify which tables, reports, and charts from your ServiceNow® instance must be used to import data into your Microsoft Word. You can also specify the columns from a table from which you want to import data.
3.  As an ESG administrator, you can configure additional reporting filters. These filters specify at a granular level what data must be imported to the disclosure report from a table.
4.  As an ESG reporting and disclosure manager, go to your Microsoft Word document, authenticate yourself, and import the data from your instance to the document. You can alter the formatting of the data according to your preferences.

**Parent Topic:**[Integrating Microsoft 365 with ServiceNow reporting](integrating-o365-with-servicenow.md)

