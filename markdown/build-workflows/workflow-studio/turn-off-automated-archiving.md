---
title: Turn off automated archiving
description: Turn off the automatic archiving of context records for your complete and cancelled playbooks.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Archive process contexts, Administering playbooks, Configuring playbooks, Configuring Workflow Studio, Workflow Studio, Build workflows]
---

# Turn off automated archiving

Turn off the automatic archiving of context records for your complete and cancelled playbooks.

## Before you begin

Role required: admin or playbook.admin

If you want to change the number of days to before a playbook is archived instead, see [Configure archive settings for process contexts](config-archive-settings-process-contexts.md).

## Procedure

1.  Navigate to **All** &gt; **System properies** &gt; **All Properties**.

2.  Search for and open the **sn\_pa\_designer.enableDataRetentionFeatures** property.

3.  Select the **here** link in the warning message to edit the record.

4.  Set the **Value** to **true**.

    **Warning:** Changing other fields in this record could potentially break automated archiving.

5.  Select **Update**.

    Automated archiving is turned off.


## Turn off archiving

![](../images/turn-off-archiving.gif)

**Parent Topic:**[Archive process contexts](archive-process-executions.md)

