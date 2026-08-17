---
title: Add integration
description: Connect a use case to a workflow by adding an integration. Integrations automate document task creation or value extraction based on triggers in the target table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-integration.html
release: australia
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Set up a use case, Information Extraction skill, Configure, Content Understanding, Enable AI experiences]
---

# Add integration

Connect a use case to a workflow by adding an integration. Integrations automate document task creation or value extraction based on triggers in the target table.

## Before you begin

Role required: DocIntel Admin \[sn\_docintel.admin\] or DocIntel Manager \[sn\_docintel.manager\] role

## Procedure

1.  Select **Add integration**.

    This option is available when a target table is selected for the use case.

    If you have already defined one or more integrations and you want to add another, select **New integration**.

2.  Enter a name for the integration.

3.  Select the type of integration you want to use.

    The `Process task` type creates an integration point to automatically create and process document tasks based on specific triggers happening in the target table.

    The `Extract values` type creates an integration point to automatically propagate the extracted values to the target table when extraction has been completed.

4.  Use the conditions to select certain fields as specific triggers for the integration.

    Conditions are available if you selected `Process task` in the previous step. For more information on conditions, see [OR conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_UsingORConditions.md).

5.  Select the **Create Flow** option to create a flow for this integration in Workflow Studio.

    **Tip:** This option should be selected, unless you're planning to write your own custom script to set up the integration.Be sure the integration is activated on Workflow Studio. For more information, see [Building flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/flows.md).

6.  Select **Save**.

7.  Select **Save and continue**.


## What to do next

[Review and activate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/review-and-activate.md)

