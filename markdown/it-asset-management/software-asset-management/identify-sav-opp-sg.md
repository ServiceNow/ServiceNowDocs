---
title: Identify savings opportunities
description: Identify savings opportunities and save money with the ServiceNow Software Asset Management application.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Microsoft 365 SaaS License Management success guide, Success Guides, Success portal view in Software Asset Workspace, Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Identify savings opportunities

Identify savings opportunities and save money with the ServiceNow Software Asset Management application.

## Before you begin

Role required: sam\_admin

## About this task

For enterprise subscriptions such as E1, E3, and E5, Microsoft may specify a commit level, which serves as a minimum or a floor to your license count, which means you can't reduce the enterprise subscription quantities below the commit level during the contract term. If your existing Microsoft contract has a commit level, you can realize potential savings opportunities at the end of the contract term.

## Procedure

1.  Realize your saving opportunities from over-licensed amounts.

    1.  Navigate to the Microsoft 365 data.

        |Interface|Action|
        |---------|------|
        |Core UI|Navigate to **All** &gt; **Software Asset** &gt; **Reconciliation** &gt; **License Workbench**.|
        |Software Asset Workspace|Navigate to **Software Asset Workspace** &gt; **License usage**.|

    2.  Locate and select Microsoft 365.

        The license compliance data is populated for the Microsoft 365 subscription.

        1.  Locate the Rights available value, which is calculated by `Rights used - Rights owned`.
        2.  Locate the Over-licensed amount, which is calculated by `Rights available * Software entitlement unit cost`. This amount presents the following potential savings opportunities:
            -   If new Microsoft 365 subscriptions aren't needed, you can remove the over-licensed amount during the next in-contract true-up without breaching the commit level.
            -   If the commit level prevents in-contract true-up, you can use the over-licensed amount to inform new contract negotiations, which would be a proactive cost saving approach.
2.  Realize your saving opportunities from software subscriptions last activity dates.

    1.  Navigate to the Software Subscriptions or User subscription page.

<table id="table_tgs_z5s_cxb"><thead><tr><th>

Interface

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Core UI

</td><td>

Navigate to **All** &gt; **Software Asset** &gt; **Discovery** &gt; **Software Subscriptions**.

</td></tr><tr><td>

Software Asset Workspace

</td><td>

1.  Navigate to **License operations** &gt; **User subscription** &gt; **User subscription**.
2.  Select a user display name.


</td></tr></tbody>
</table>    2.  Add the **Last activity** field and filter the list to view desired subscriptions.

        **Note:** The Last activity date is pulled from the published Microsoft 365 integration profile and inventory tools. If a subscription is a suite product, the Last activity date is the latest activity information from any of its suite components. Validate Last activity dates with Microsoft cloud administrators as needed.

    3.  Right-click the **Display name** column header and select **Bar Chart**.

    4.  On the Create a report form, set **Group by** to **Last activity** and select **Run**.

        For more information, see [Create a report](https://www.servicenow.com/docs/access?context=t_CreateYourOwnReport&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

        The report visualization automatically updates to display filtered software subscriptions grouped by last activity in bar chart form.

    5.  Point to any bar in the chart to view additional details and select a bar to view the individual records that comprise it.

        For more information about using reports, see [Using reporting](https://www.servicenow.com/docs/access?context=c_GenerateReports&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

3.  Find Software Asset Management optimization recommendations for Microsoft 365 based on subscription details, usage, and potential savings based on recommendation type.

    For more information, see [Publisher optimizations for Microsoft](../reference/pub-opt-microsoft.md).


## Result

Microsoft 365 subscriptions that haven’t registered user activity in over a few months are the potential reclamation candidates.

## What to do next

Here are a few follow-up actions:

-   Review the **User principal name** for any former employees. If found, reclaim subscriptions.
-   For subscriptions tied to active employees, navigate to the Software Installations \(cmdb\_sam\_sw\_install\) table.
-   Filter the Software Installations list for Microsoft 365 and add the **Last used** column. Create a report if wanted.
-   Compare the Software installations report with the Software subscriptions report.

