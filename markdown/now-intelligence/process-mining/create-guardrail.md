---
title: Create a table-level guardrail
description: Define a mandatory filter condition for a table to prevent projects from being configured in ways that consume more mining capacity than necessary.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/create-guardrail.html
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 1
keywords: [process mining, guardrails, admin panel]
breadcrumb: [Meter-based guardrails and controls, Use, Process Mining, Platform Analytics]
---

# Create a table-level guardrail

Define a mandatory filter condition for a table to prevent projects from being configured in ways that consume more mining capacity than necessary.

## Before you begin

Role required: sn\_process\_mining\_power\_user or sn\_process\_mining\_admin

Other users can view existing guardrails but can't create, edit, or delete them.

## About this task

You can define one mandatory filter condition per table \(for example, "only cases resolved in the last 12 months"\). Once active, this condition is automatically applied to every project built on that table. The person creating the project can add their own filters on top, but can't remove or edit the administrator's condition.

## Procedure

1.  Navigate to **All** &gt; **Process Mining** &gt; **Table Guardrails** &gt; **Create New**.

2.  Fill in the following fields:

    |Field|Description|
    |-----|-----------|
    |Name|A descriptive label for the condition.|
    |Primary Table|The table this guardrail applies to.|
    |Filter Condition|The mandatory condition, built using the standard condition builder. Dot-walking is supported; conditions on related lists aren't supported.|
    |Active|Whether this guardrail is currently enforced. Defaults to selected. Clear this to save the guardrail without enforcing it yet.|

    **Note:** Filter conditions automatically apply to all new projects created on the primary table. Existing and scheduled projects on this table will also be updated.

3.  Select **Submit**.


## Result

Every new project built on this table automatically includes this condition. The condition appears in a locked Guardrails section during project setup. Users can add their own filters on top, but can't edit or remove the guardrail.

**Parent Topic:**[Meter-based guardrails and controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/meter-based-guardrails.md)

