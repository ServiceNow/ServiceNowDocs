---
title: Add impacted areas manually to a regulatory alert
description: Add impacted areas such as citations, control objectives, policies, and more to your regulatory alerts. Adding impacted areas to a regulatory alert captures additional impacts that you identified and impacts that weren’t initially recommended.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Generate recommendations for regulatory alert impacted areas, Use generative AI skills, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Add impacted areas manually to a regulatory alert

Add impacted areas such as citations, control objectives, policies, and more to your regulatory alerts. Adding impacted areas to a regulatory alert captures additional impacts that you identified and impacts that weren’t initially recommended.

## Before you begin

Role required: sn\_grc\_reg\_change.user

For more information on related roles and regulatory alerts, see [Types of alerts, user roles, and states of regulatory alerts](../../grc-rcm/reference/user_roles_and_actions.md).

## About this task

Impacted areas can be added as part of accepted recommendations or can be manually added. For more information on adding impacted areas as part of a recommendation, see [Accept or dismiss recommendations for regulatory alert impacted citations](manage-recommendation-reg-alert.md).

**Note:** Impacted areas can be added only to regulatory alerts of type Regulatory event. You can’t add impacted areas to alerts of type Source document.

## Procedure

1.  Navigate to one of the following locations:

    -   **Workspaces** &gt; **Compliance Workspace**, select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png) and then navigate to **Regulatory alerts**.
    -   **Workspaces** &gt; **Compliance Workspace** select the Regulatory Change Management dashboard icon ![](../../grc-rcm/image/reg-change-icon.png) and then in the Activity overview, Tracking, or Trends section, select any segment or value in an Alerts related widget to open the list of regulatory alerts with that state.
2.  Select the regulatory alert that you want to review recommendations for and navigate to the Impacted areas tab.

3.  Select **Add**.

4.  Select the type of impacted area, the record you want and then select **Add**.

    The record you selected as an impacted area now appears in the Impacted areas list.

    **Note:** To confirm if impacted areas were added as part of a recommendation or manually, review the AI-assisted column in the Impacted areas list. "Yes" indicates a recommendation, while "No" indicates a manual addition.


## What to do next

You can initiate the implementation activity for impacted business areas of operations by setting the applicability of the regulatory alert to **Yes** or **No**. If the regulatory alert is applicable, a new regulatory change task is automatically created. If a regulatory alert is not applicable, the alert's state is updated to **Completed**. For more information, see [Manage regulatory change tasks](../../grc-rcm-workspace/task/manage-reg-change-tasks-using-ws.md).

**Related topics**  


[Activate Regulatory alert recommendation skills](configure-recommendation-skill-for-a-regulatory-alert.md)

[Generate recommendations for regulatory alert impacted citations, control objectives, controls, and policies](create-recommendation-reg-alert.md)

