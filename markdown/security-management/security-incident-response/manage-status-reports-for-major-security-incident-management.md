---
title: Configure Major Security Incident status reports
description: Configure major security incident reports to set up and download the reports according to your business needs throughout the life cycle of the major security incident record remediation process.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Manage MSIM status reports, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Major Security Incident status reports

Configure major security incident reports to set up and download the reports according to your business needs throughout the life cycle of the major security incident record remediation process.

You can build the report templates with a specific format and layout, and customize these reports according to your specific requirements using the Status Reports feature of the Major Security Incident Management workspace.

A user with the sn\_msi.workspace\_manager role can create and configure the report templates that outline the type of report information that can be used to generate all the status reports, which can be shared with specific users such as executive stakeholders, legal departments and map those templates to the major security incident records.

To customize your MSI status reports, you must first set up the report templates using **Report Templates**. With the help of Report Templates, you can build the report template types, define the report components for those report templates, add additional information, create visualized data to track the scope and progress metrics, add related list data, and generate the status reports.

The following describes the default fields provided in all the report template types. You can configure and format the report template based on your requirements using sections, subsections, and its elements:

|Component Type|Description|
|--------------|-----------|
|Report Title|Title of the report type. For example, the default format of the report type is: \{MSI Number\} - \{Executive Stakeholder Report\} depicted as MSI0001001: Executive Stakeholder Report.|
|Name|Displays the name of the user who generated the report using the Status Reports section of the Major Security Incident Management workspace.|
|Summary|Displays a brief summary of the report.|
|Date|Displays the date on which the report is shared with the concerned recipient.|
|Progress|Displays the Scope and Progress Metrics such as the linked SIR Incidents, Response Tasks, Supplementary Tasks, External Collaboration, Timeline components, and Recent Timeline Events.|
|Challenges|This section displays a brief description on the challenges involved throughout the major security incident remediation process.|
|Next Steps|This section displays a brief description on the next steps involved in resolving the major security incident. For example, the active team subsection in the executive stakeholder report provides you with the information with the next step on the team assignment who is involved in further analysis of the major security incident record.|
|Other customizations|The report template also provides you with the capability to upload the logo and customize the headers and footers on the report.|

Following are the types of report categories that can be set up and viewed:

-   **Executive** Email
-   **Technical Status Report** PDF
-   **Executive Status Report** PDF

The above reports are configured and available for the user to select, view, and generate the report from the Major Security Incident Management workspace.

## Mobile-friendly Executive Status Reports - Email

The Executive Status Reports - Email are mobile-friendly status reports that are generated in email format. The report section includes a summary of the report, MSI duration column, incident scope/impact, active team metrics, progress metrics, and Timeline components such as the recent timeline events for that specific major security incident record.

Customize and configure the following report template features to add additional information to the report. A sample executive email status report is shown below for your reference.

![Executive Status Report Email](../image/msim-executive-report-email.png "Executive Status Report Email")

## Executive Status Reports - PDF

The Executive Status Reports - PDF are status reports that are generated in PDF format. The report section includes a summary of the report, MSI duration column, incident scope/impact, active team metrics, progress metrics, and Timeline components such as the recent timeline events for that specific major security incident record.

Customize and configure the following report template features to add additional information to the report. A sample executive report is shown below for your reference.

![Executive Status Report PDF](../image/executive-reports-01.png "Executive Status Report PDF")

## Technical Status Reports - PDF

The Technical Status Reports - PDF are status reports that are generated in PDF format. The report section includes a summary of the report, MSI duration column, incident scope/impact, active team metrics, progress metrics, and Timeline components such as the recent timeline events for that specific major security incident record, labeled Task updates and labeled activities, based on the assignment group and selected tag label since when the last status report is generated, and additional information such as incident impact and linked incidents.

Customize and configure the report template to add additional information to the report. A sample technical report that shows the additional information, such as the incident impact, is illustrated below for your reference, and the remaining part of the report information is similar to the executive reports.

![Technical Status Report PDF](../image/msim-technical-status-report.png "Technical Status Report - PDF")

The report template sections contain various subsections, which describe how you can construct the report subsections and its elements such as:

1.  Branding: [Add Branding to your Report Templates](../task/add-branding-to-your-report-templates.md)
2.  Template Scripts: [Use Template Scripts in your Report Templates](../task/using-template-scripts-in-your-report-templates.md)
3.  [Use Visualizations in Report Templates](../task/using-widgets-in-your-report-templates.md)
4.  [Use Reports Lists in Report Templates](../task/using-reports-lists-in-your-report-templates.md)

-   **[Create a Report Template](../task/create-report-template.md)**  
Create various report templates, which can be applied to the major security incidents and generate a status report. You can add standard and custom Major Security Incident Response form fields to the report template that are dot-walkable. In addition, you can format and configure the report based on your requirements using sections, subsections, and its elements.
-   **[Create a Report Section Template](../task/create-report-section-template.md)**  
A report can further be divided into various sections. Use the Report section to break down the report into multiple sections and reorganize them in order.
-   **[Create a Report Subsection Template](../task/create-report-subsection-template.md)**  
Use the report subsection to further organize the section into multiple subsections and configure their alignment and position using the available types such as Text side panel, Primary, and Secondary.
-   **[Create Report Subsection Element template](../task/create-report-subsection-element-template.md)**  
Use subsection elements to further organize a subsection into multiple elements. Subsection elements help define visualizations, lists, free-form text more declaratively with filter options such as assignment groups and labels.
-   **[Add system properties](adding-system-properties-to-your-status-reports.md)**  
Add system properties to control MSIM application behavior. Following are the default system properties that are introduced as part of the Major Security Incident Management status reports.

**Parent Topic:**[Managing MSIM status reports](reports-and-metrics.md)

