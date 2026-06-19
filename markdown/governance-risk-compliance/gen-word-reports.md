---
title: Generating Microsoft Word reports using Document designer
description: Digital resilience incident reporting administrators \(sn\_dri\_inc\_rptg.digital\_resilience\_incident\_administrator\) can now set up Microsoft Word templates and Digital resilience incident reporting managers \(sn\_dri\_inc\_rptg.digital\_resilience\_incident\_manager\) can download action task reports in Microsoft Word format​.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/gen-word-reports.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Generating Microsoft Word reports using Document designer

Digital resilience incident reporting administrators \(sn\_dri\_inc\_rptg.digital\_resilience\_incident\_administrator\) can now set up Microsoft Word templates and Digital resilience incident reporting managers \(sn\_dri\_inc\_rptg.digital\_resilience\_incident\_manager\) can download action task reports in Microsoft Word format​.

## Using the ServiceNow Document designer with Microsoft Word

The ServiceNow Document designer with Word application offers a low-code solution, enabling you to configure different aspects of Microsoft Word documents without requiring extensive technical expertise. The templates offered by ServiceNow are designed to align with the company's brand guidelines, verifying consistent and professional documentation.

Use the ServiceNow Document designer with Word application to generate intuitive and audit-ready Microsoft Word reports for action tasks directly from your ServiceNow instance. Configure the Microsoft Word templates in the application to include specific data from the records, such as tables and columns, into the reports. Options include using predefined templates, customizing them with low-code implementation, or creating your own templates to meet your company's specific guidelines.

You can save these reports either within your ServiceNow instance or as cloud documents in Microsoft SharePoint.

## Benefits of using Document designer

The ServiceNow Document designer with Word application enables you to pull metadata, such as fields and related lists, from ServiceNow tables. It also enables you to add content blocks that repeat for each record in a table, for example, 10 blocks for 10 issues. Apply the templates to specific records and create reports in Microsoft Word format.

## Workflow for configuring and managing the report templates

To configure and manage the report templates, complete the following steps in the given sequence.

1.  Install Document designer to automate Microsoft Word document generation from ServiceNow table data, including dynamic repeating content blocks based on record count. For more information, see [Install the Document designer with Word application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/generate-word-report-of-action-task.md)
2.  Create Template configuration to enable structured configuration of data relationships and dynamic variables and confirm an accurate, report-ready document output. For more information, see [Create Template configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-template-configuration.md).
3.  Create Data relationships to navigate and fetch data from any table, enabling accurate and targeted data retrieval in report templates. For more information, see [Create Data relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-data-relationships-action-tasks.md).
4.  Create Content configurations to define and display targeted report data—whether record lists or aggregated insights—fetching multiple records from any table. For more information, see [Create Content configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-content-configurations-action-tasks.md).
5.  Create Reporting configurations to manage how Digital Resilience Incident reports are generated and delivered with Microsoft 365 reporting configurations. For more information, see [Create reporting configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-reporting-configurations.md).

    Starting with Digital Resilience Incident Reporting, version 22.3.0, the Reporting Configurations module \(sn\_esg\_msoff\_intg\_o365\_reporting\_configuration\) is available in the Digital resilience incident reporting application. This module provides Microsoft 365 reporting configurations scoped to the Digital resilience incident \(DRI\) business domain.

    The Reporting Configurations and Template Configurations modules are both filtered to the Digital resilience incident \(DRI\) business domain. This domain is installed automatically with the Digital resilience incident reporting application. Administrators don't have to create it manually.

    **Note:** Create Reporting configurations after creating the Template configurations and before creating Data relationships.

6.  Download the manifest file and side-load it in the Document designer with Word application to customize reports and Microsoft Word templates according to your business needs. For more information, see [Download the manifest file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/download-manifest-file.md).
7.  Build Microsoft Word templates to generate standardized Microsoft Word reports using the Document designer add-in. For more information, see [Build the Microsoft Word template using the add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/build-word-template-using-add-in.md).
8.  Generate Microsoft Word reports across different records using predefined templates to streamline reporting in a standardized format. For more information, see [Generate a Microsoft Word report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/generate-word-report.md).

