---
title: Configure content filtering definitions
description: Create a content definition that describes a set of content a filtering rule grants access to.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/configure-content-definitions.html
release: brazil
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Content access filtering, Managing playbook permissions, Configure, Playbooks, Workflow Studio, Build workflows]
---

# Configure content filtering definitions

Create a content definition that describes a set of content a filtering rule grants access to.

## Before you begin

Role required: admin, playbook.admin

## About this task

A content definition specifies a type of resource and, optionally, a condition that narrows it. Pair it with a content filtering rule to grant access. For more information, see [Content access filtering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/content-access-filtering-playbooks.md).

## Procedure

1.  Navigate to **Process Automation** &gt; **Flow Administration** &gt; **Content Definitions**.

    The **Workflow Resources** table opens.

    If you don't have access to Flow Administration, **Content Definitions** appears directly under **Process Automation**.

2.  Select an existing definition or select **New**.

3.  Fill in the form.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the content definition.|
    |Application|Application the definition belongs to. Defaults to the current scope. Select **Global** to apply the definition across all applications.|
    |Table|Table holding the content. Select the Process Definition \[sys\_pd\_process\_definition\] table to filter by playbook type, or the Activity Definition \[sys\_pd\_activity\_definition\] table to filter by activity.|
    |Conditions|Conditions that narrow the definition. Leave empty to cover every record on the table.|
    |Resource Tags|Tags that refine the definition further.|

4.  Select **Submit**.


## What to do next

Create a content filtering rule that names the roles granted access to this definition. See [Configure content filtering rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/configure-content-filtering-rules-playbook.md).

**Parent Topic:**[Content access filtering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/content-access-filtering-playbooks.md)

