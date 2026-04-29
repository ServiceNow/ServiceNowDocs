---
title: Create and activate a configured insight for Security Posture Control
description: You can create your own insights. Configured insights are insights that you can create either using existing policies or your own custom policies.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use the workspace, Security Posture Control, Security Operations]
---

# Create and activate a configured insight for Security Posture Control

You can create your own insights. Configured insights are insights that you can create either using existing policies or your own custom policies.

## Before you begin

You must create an insight record and activate it before you can view your data on the Configured insights dashboard. You can have up to six insights and 21 charts on the Configured insights dashboard module in the workspace.

Any policies you use for a custom insight must be activated.

For policies you create with ‘Software’ as the Asset type, you can save the policy and create custom insights, but you cannot configure findings from the policy record.

Roles required: SPC Admin Group or SPC Analyst Group

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Posture Control** &gt; **Insight builder**.

    On this landing page, there are three tabs:

    -   **Active**

        Your activated custom insights. Activated custom insights are displayed on the Configured insights landing page \(second icon from the top in the workspace\).

    -   **Inactive**

        Your inactive custom insights. Deactivated insights are not displayed on the Configured insights landing page until the insights and their supporting policies supporting them are activated.

    -   **All**

        All your active and inactive configured insights.

2.  Select **New Insight** on the right of the page to create a new record.

3.  In the Type field select an insight from the choice list.

    |Option|Description|
    |------|-----------|
    |Comparison chart|Compare counts for matching assets for up to five policies.|
    |Policy match count widget|The total number of your assets that match a policy or policies.|
    |Policy match percentage chart|The percentage of your total assets that match or do not match a policy.|
    |Policy match trend chart|Historical trend of assets that match a policy or policies.|

4.  Select one.

    -   Hardware asset or Cloud virtual machine
    -   Software
5.  Select groups for your insight.

    An insight must belong to at least one group. You must create or assign groups to your configured insights when you create new records in the Custom insight builder module. Groups allow you to organize your reports on the Configured insights dashboard.

6.  Select the policies and the corresponding labels you want for your insight data.

7.  Select **Save**.

    Your insight is saved on the Inactive insight tab.

8.  To activate your new insight, open the record on the Inactive list and select **Activate**.

    Data is gathered from the next scheduled import for the Service Graph Connectors that are associated with the insight's policies, and data is displayed on the Custom insights dashboard module in the workspace.


