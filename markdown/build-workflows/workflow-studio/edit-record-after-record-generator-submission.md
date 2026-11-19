---
title: Edit a record after record generator submission
description: Keep a record editable after a playbook record generator creates it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/workflow-studio/edit-record-after-record-generator-submission.html
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-09-15"
reading_time_minutes: 1
breadcrumb: [Playbook record generator, Designing playbooks, Use, Workflow Studio, Build workflows]
---

# Edit a record after record generator submission

Keep a record editable after a playbook record generator creates it.

## Before you begin

Role required: admin

After a record generator activity's form is submitted, the activity's type changes from Record Generator to Record, because it's now associated with the created record. Without an activity action to reopen it, the completed form is set to read-only.

## Procedure

1.  Navigate to **All** &gt; **Process Automation Designer** &gt; **Activity Actions**.

2.  Select **New**.

3.  Set Type to **Server Script**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Applies to|Select Record activities.|
    |State|Select Complete.|
    |Form Fields Required|Enable this option.|
    |Script|Enter `current.update();`|

5.  Select **Submit**.

6.  Add the activity action to the relevant Playbook Experience Action Assignment Map.


## Result

The record created by the record generator remains editable in Complete state.

**Parent Topic:**[Playbook record generator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/playbook-record-generator-overview.md)

