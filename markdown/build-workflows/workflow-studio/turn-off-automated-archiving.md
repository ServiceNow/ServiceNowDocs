---
title: Turn off automated archiving
description: Turn off the automatic archiving of context records for your complete and cancelled playbooks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/build-workflows/workflow-studio/turn-off-automated-archiving.html
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Archive process contexts, Administering playbooks, Configuring playbooks, Configuring Workflow Studio, Workflow Studio, Build workflows]
---

# Turn off automated archiving

Turn off the automatic archiving of context records for your complete and cancelled playbooks.

## Before you begin

Role required: admin or playbook.admin

If you want to change the number of days to before a playbook is archived instead, see [Configure archive settings for process contexts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/config-archive-settings-process-contexts.md).

## Procedure

1.  Navigate to **All** &gt; **System properies** &gt; **All Properties**.

2.  Search for and open the **sn\_pa\_designer.enableDataRetentionFeatures** property.

3.  Select the **here** link in the warning message to edit the record.

4.  Set the **Value** to **false**.

    **Warning:** Changing other fields in this record could potentially break automated archiving.

5.  Select **Update**.

    Automated archiving is turned off.


## Turn off archiving

\[Omitted image "turn-off-archiving.gif"\] Alt text: Animation of navigating to system properties and editing the archiving property.

**Parent Topic:**[Archive process contexts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/archive-process-executions.md)

