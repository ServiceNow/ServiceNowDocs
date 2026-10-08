---
title: Configure content filtering rules
description: Create a rule that grants a role access to the content in a content definition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/configure-content-filtering-rules-playbook.html
release: brazil
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 1
breadcrumb: [Content access filtering, Managing playbook permissions, Configure, Playbooks, Workflow Studio, Build workflows]
---

# Configure content filtering rules

Create a rule that grants a role access to the content in a content definition.

## Before you begin

Role required: admin, playbook.admin

A content definition must exist. See [Configure content filtering definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/configure-content-definitions.md).

## About this task

A content filtering rule associates one or more roles with a single content definition. Users with the named role can reach the content covered by the definition, unless the content has required roles set. For more information, see [Content access filtering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/content-access-filtering-playbooks.md).

## Procedure

1.  Navigate to **Process Automation** &gt; **Flow Administration** &gt; **Content Filtering Rules**.

    The **Workflow Resource Filter Rules** table opens.

    If you don't have access to Flow Administration, **Content Filtering Rules** appears directly under **Process Automation**.

2.  Select an existing rule or select **New**.

3.  Fill in the form.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the rule.|
    |User Role|Role a user must have to reach the content.|
    |Delegated Development Permission|Optional. The resource path for which the user is a delegated developer.|
    |Active|Whether the rule is in force.|
    |Application|Application the rule belongs to. Defaults to the current scope.|
    |Resource Definition|Content definition the rule grants access to.|

4.  Select **Submit**.


## Result

Users with the named role can reach the content covered by the definition. Assign playbook.write rather than pd\_author to those users, because pd\_author grants access to all content and overrides the restriction because of a default, unmodifiable content filtering rule.

**Parent Topic:**[Content access filtering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/content-access-filtering-playbooks.md)

