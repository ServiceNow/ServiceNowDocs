---
title: Create a Microsoft Word template record for an audit report
description: Generate your audit reports for an engagement in Microsoft Word template to collaborate with your auditors in an effortless and user-friendly manner.
locale: en-US
release: yokohama
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Generate an audit report for an engagement using Microsoft Word template, Audit Workspace, Audit Management, Governance, Risk, and Compliance]
---

# Create a Microsoft Word template record for an audit report

Generate your audit reports for an engagement in Microsoft Word template to collaborate with your auditors in an effortless and user-friendly manner.

## Before you begin

Role required: sn\_audit.admin, sn\_irm\_shared\_cmn.word\_template\_creator, sn\_irm\_shared\_cmn.word\_template\_reader

-   The Word template creator role \(sn\_irm\_shared\_cmn.word\_template\_creator\) has create, read, update, and delete access to all the records in the Word template \[sn\_irm\_shared\_cmn\_word\_template\] and Word template category \[sn\_irm\_shared\_cmn\_word\_template\_category\] tables.
-   The minimum role is the Word template reader role \(sn\_irm\_shared\_cmn.word\_template\_reader\) that has the read access to the records in the Word template and Word template category tables.
-   The minimum role is the Word template reader role \(sn\_irm\_shared\_cmn.word\_template\_reader\) that has the read access to the records in the Word template and Word template category tables.

    You can generate the audit report for an engagement record in a Word template in Audit Workspace only.

-   To apply the Word template in the engagement record and to generate the report in the Audit Workspace, you must have the Audit manager role \(sn\_audit.manager\). See, [Generate audit report for an engagement](../../grc-workspace-audit/task/generate-audit-report.md).

    You can generate the audit report for an engagement record in a Word template in Audit Workspace only. To apply the Word template in the engagement record and to generate the report in the Audit Workspace, you must have the Audit manager role \(sn\_audit.manager\). See, [Generate audit report for an engagement](../../grc-workspace-audit/task/generate-audit-report.md).


**Important:** You must set up the ServiceNow Document designer for Word plugin before you create a Microsoft Word template and generate the audit report for an engagement record.

For more information, see [Content configuration](../../grc-common/concept/configuring-audit-word-based-templates.md).

## About this task

As an audit admin, you can navigate to the Word template module and configure the record for a particular table or a document.

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit report** &gt; **Word Report Templates**.

2.  Select **New**.

3.  On the form, fill in the fields.

    See the [Word template form](../reference/audit-word-template-form.md) for values to enter in each field of the form.

4.  Select **Submit**.


## What to do next

You must select the Word report template as the template type for the engagement record. Then, generate the report in the Audit Workspace.

For more information, see

-   [Create an audit engagement in Audit Workspace](../../grc-workspace-audit/task/create-engagement-ws.md).
-   [Generate audit report for an engagement](../../grc-workspace-audit/task/generate-audit-report.md).

