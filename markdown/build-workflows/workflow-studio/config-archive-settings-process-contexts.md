---
title: Configure archive settings for process contexts
description: Change the default settings for the automated archiving feature for process contexts.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Archive process contexts, Administering playbooks, Configuring playbooks, Configuring Workflow Studio, Workflow Studio, Build workflows]
---

# Configure archive settings for process contexts

Change the default settings for the automated archiving feature for process contexts.

## Before you begin

Role required: admin or playbook.admin

If you want to turn off automated archiving instead, see [Turn off automated archiving](turn-off-automated-archiving.md).

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Search for and open the **sn\_pa\_designer.data\_retention\_policy** property.

3.  Select the **here** link in the warning message to edit the record.

4.  Change the **Value** to the number of days a complete or cancelled playbook must be unedited before the context records for it can be archived.

    The default value is 14. If you want context records for executions to be archived as soon as a playbook is complete or cancelled, you can set the value to O. If you want to wait longer before context records can be archived, enter a greater number.

    **Warning:** Changing other fields in this record could potentially break automated archiving.

5.  Select **Update**.

    Your change is saved.


## Change the wait period to 30 days

![Changing the Value from 14 to 30](../images/change-archive-wait-period.gif)

**Parent Topic:**[Archive process contexts](archive-process-executions.md)

