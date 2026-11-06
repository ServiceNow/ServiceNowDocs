---
title: Set up a triage board in SAFe
description: Set up your own triage board by defining filter criteria, and view records that are important to your team, such as problems, incident tasks, defects, or change requests. For example, you can create one triage board for defects and another for incidents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/scaled-agile-framework-safe/safe-setup-triage-board.html
release: australia
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [SAFe — Unified Backlog, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# Set up a triage board in SAFe

Set up your own triage board by defining filter criteria, and view records that are important to your team, such as problems, incident tasks, defects, or change requests. For example, you can create one triage board for defects and another for incidents.

## Before you begin

The Agile - Scaled Agile Framework - Unified Backlog plugin must be active. Otherwise, the **Triage Board** option doesn't appear on the SAFe Board.

**Important:**

Starting with the Xanadu release, the plugins Portfolio SAFe, Essential SAFe, Performance Analytics Content Pack for Essential SAFe, Work Progress Status for SAFe, Agile - Scaled Agile Framework - Unified Backlog, and Read only roles for SAFe are being prepared for future deprecation. These plugins will be hidden and can no longer be activated on new instances but will continue to be supported. [Enterprise Agile Planning in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/enterprise-agile-planning/eap-landing.md) provides the latest experience for this functionality.

For more information on the deprecation process and its impact, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

The team must have a current program increment. Otherwise, the **Backlog** tab shows the message **There are no active program increments**, and the **Triage Board** option doesn't appear.

You must be added to the SAFe team that would be responsible for handling work from this triage board.

Role required: safe\_scrum\_master

## Procedure

1.  Navigate to **All** &gt; **Scaled Agile Framework \(SAFe\)** &gt; **SAFe Board**.

2.  Select the **Backlog** tab.

3.  Select **Triage Board**.

4.  On the form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Name|Suitable name for the triage board.|
    |Table|Table from which you want to filter records.|
    |Filter|Filter criteria to be applied on the table for refinement of records.|

    **Note:** When setting up a triage board, do not to remove these default conditions:

    -   **Active is true**: This condition ensures that the tasks on your Triage Board are relevant.
    -   **Agile story is empty**: This condition ensures that the task is not present in some other backlog.
5.  Click **Submit**.

    A triage definition is created.


## What to do next

1.  Select the triage definition.
2.  To add a record to the triage definition, click **New**.
3.  To move a record from the triage board to the **Backlog** tab, click **Add to Backlog**.

**Parent Topic:**[SAFe — Unified Backlog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scaled-agile-framework-safe/safeunified-backlog.md)

