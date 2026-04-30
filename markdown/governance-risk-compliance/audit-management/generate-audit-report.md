---
title: Generate an audit report for an engagement using Microsoft Word template
description: Generate an audit report for an engagement record using Microsoft Word template that is in the Validate state or any subsequent states. You can manage the generated report either on cloud \(Microsoft SharePoint\) in the Cloud files tab or as a sys\_attachment to the engagement.
locale: en-US
release: zurich
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
keywords: [Generate audit report in audit Word template, Audit report template, Word report template for audit, Generate audit report, Audit report in Word template for an engagement record]
breadcrumb: [Audit Workspace, Audit Management, Governance, Risk, and Compliance]
---

# Generate an audit report for an engagement using Microsoft Word template

Generate an audit report for an engagement record using Microsoft Word template that is in the Validate state or any subsequent states. You can manage the generated report either on cloud \(Microsoft SharePoint\) in the Cloud files tab or as a sys\_attachment to the engagement.

## Before you begin

Role required: sn\_audit.manager, sn\_audit\_ws.supervisor, sn\_irm\_shared\_cmn.word\_template\_reader

1.  To apply the Word template in the engagement record and to generate the report in the Audit Workspace, you must have the Audit manager role \(sn\_audit.manager\) and also the Word template reader role \(sn\_irm\_shared\_cmn.word\_template\_reader\). More importantly, you must have access to the Audit Workspace.
2.  To generate the report for the engagement, the record must be in the Validate, Fieldwork, or Follow Up state.
3.  To view the **Generate report** button in the engagement record, you should have selected the **Word report template** option in the **Template type** field while creating the record.

**Important:** You must set up the ServiceNow Document designer for Word plugin before you create a Microsoft Word template and generate the audit report for an engagement record.

For more information, see [Content configuration](../../grc-common/concept/configuring-audit-word-based-templates.md) and [Create Word template record for an audit engagement](../../grc-audit/task/configure-audit-word-template.md).

## About this task

To generate an audit Word report, you must navigate to **All** &gt; **Audit** &gt; **Audit Report** and set up the following administrative steps for a Word template:

-   [Create content configurations](../../grc-common/task/create-content-configurations.md)
-   [Create Word Report Templates](../../grc-audit/reference/audit-word-template-form.md)
-   [Create Word Template Categories](../../grc-audit/reference/audit-word-template-category.md)

-   If you had selected the **Classic report template** option in the **Template type** field while creating the engagement record, then the reports are generated as a Knowledge Base, while the input template is in HTML, script, or XML. For more information, see [Create an audit report template](../../grc-common/task/create-audit-report-temp.md).
-   If you had selected the **Word report template** option in the **Template type** field as an input template while creating the engagement, then the Word template report that is generated is a Word file.

You can apply the Microsoft Word template to one or more audit engagement records and generate the audit report in Word format. You can use the Word document to collaborate with other stakeholders for report editing.

There are two steps to this process:

1.  As an audit admin, you can navigate to the Word template module and configure the record for a particular table or a document.
2.  As an audit manager, audit supervisor, or auditor you can then associate the Word report template to the engagement record and generate the audit report, provided you also have the template reader \(sn\_irm\_shared\_cmn.word\_template\_reader\) role.

You also have the option to manage the generated report either as an sys\_attachment or on cloud in the Audit Workspace.

The generated report can be saved at the Microsoft SharePoint or Google Drive site for report collaboration.

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit Workspace**.

2.  Select the lists icon \(![List icon.](../image/ListsIcon.jpg)\).

3.  Select **All engagements** in the Execution list.

4.  Select an engagement record for which you want to generate a report.

    **Note:** The record must have been scoped. It must be in the Validate, Fieldwork, or Follow Up state.

5.  Select the **Generate report** button.

    The ServiceNow Document designer for Word plugin must be activated. Only then the **Generate report** button is available.

6.  Select the audit report name in the **Report template** field of the Generate report pop-up.

    -   All the Word templates that are relevant to the engagement and are active and in Published state appear for you to select.

        ![Generate report pop-up.](../image/audit-ws-generate-report.png)

        If there are no Word templates created for this record, then a message appears stating so.

    -   If the Word template is cloud enabled, then a message pops up with the destination where the generated report would be saved after it's generated.
    -   If you had not set up the cloud file configuration for the engagement record, then an error message appears. To enable cloud file configuration, see [Manage your documents and work papers with Audit Management as cloud files](../../grc-audit/concept/manage-cloud-docs-using-onedrive-int.md).
7.  Enter a unique name for the report in the **Name of report** field.

8.  Select **Generate**.

    A message appears stating that the report generation has been initiated.

9.  If you hadn’t selected the **Cloud enabled** option in the [Word template form](../../grc-audit/reference/audit-word-template-form.md), then select the attachment \(![Attachment icon.](../../assessment-engine/image/attachment-icon.png)\) icon to download the report.

    A message appears confirming that the report is being generated as an attachment.

    1.  Select the actions \(![Actions icon.](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png)\) icon and click the **Download** option.

    2.  Select the downloaded Word file to view the audit report.

10. If you had selected the **Cloud enabled** option in the Word template, then select the Cloud files tab for the cloud-based report.

    1.  Select the URL link for the cloud folder path to open the Word document in the Microsoft SharePoint site.

    2.  View the contents of the audit engagement report in the cloud and share the report with your collaborators.

        You can also check your most recent report as a URL or as an attachment in the **Report** field of the Report section in the engagement form.

        For details on cloud document management, see [Manage your documents and work papers with Audit Management as cloud files](../../grc-audit/concept/manage-cloud-docs-using-onedrive-int.md).

    A Word report attachment is created each time you generate the report. By default, only the latest Word report is attached to the record. However, there's a system property that you can set to retain the previous attachments even when a new report is generated with the latest attachment.

    By default, the property is set as false, which means that the previous Word report as a sys attachment is deleted from the engagement record when the report is generated again. The engagement, therefore, has the latest report, which is attached to the record.

    As an audit admin, you can set the property as true to retain the previous attachments with the engagement record. All the previous attachments are available to view in the Attachments section. Retaining the previous attachments helps you to track an audit trail on the engagement.

    To reset the property, navigate to **All** &gt; **Audit** &gt; **Administration** &gt; **Properties**. See, [Properties installed with Audit Management and Advanced Audit](../../grc-audit/reference/r_InstallWAudit.md#).


