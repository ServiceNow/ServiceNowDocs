---
title: Activate the Knowledge transfer record created trigger
description: Enable the knowledge transfer record created trigger to ensure that the employee review workflow runs after a knowledge transfer record is generated. This trigger allows departing employees to review and approve auto-generated knowledge transfer content before sharing with their manager.
locale: en-US
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-02-24"
reading_time_minutes: 1
breadcrumb: [Offboarding knowledge transfer plan generation agentic workflow, Use agentic workflows, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Activate the Knowledge transfer record created trigger

Enable the knowledge transfer record created trigger to ensure that the employee review workflow runs after a knowledge transfer record is generated. This trigger allows departing employees to review and approve auto-generated knowledge transfer content before sharing with their manager.

## Before you begin

Role required: admin \[virtual\_agent\_admin\]

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

    A list of agentic workflows appear.

2.  Locate the Knowledge transfer summary agentic workflow and select the corresponding **Duplicate** icon.

    The You are duplicating an agentic workflow dialog box appears.

3.  Select **Duplicate**.

    The duplicated agentic workflow appears with "\(Copy\)" appended to the original name.

4.  In the **Workflow Name** field, revise the default workflow name to reflect your organization's naming conventions.

5.  In the Define key requirements section, select **Save and continue** to accept the default values.

6.  In the Define user access section, select **Save and continue** to accept the default values.

7.  In the Define data access section, set the following fields:

    1.  Set the **User identity type** field to **AI user**.

    2.  Set the **AI user** field to **sn\_hr\_ai\_agents.offboarding\_agent**.

    3.  Select **Save and continue**.

8.  In the Add triggers section, select the trigger name that appears in the Triggers widget.

    The Edit a trigger form appears.

9.  In the **Name** field, revise the default trigger name to reflect your organization's naming conventions.

10. Select the **Trigger is OFF** toggle to activate the trigger.

    The toggle changes to **Trigger is ON**.

11. Set the **Portal** field to **Employee Center**.

12. Select **Save**.

13. Select **Save and continue**.

14. In the Select channels and status section, select the **Display** toggle in the Virtual Agent widget.

15. Set the **Assistants where AI agents are discoverable** field to **Now Assist in Virtual Agent \(default\)**.

16. Select **Save and test**.


## Result

The following trigger is now active: Knowledge transfer record created. When a knowledge transfer record is generated, the system automatically engages the departing employee through Now Assist in Virtual Agent to review and approve the knowledge transfer content.

