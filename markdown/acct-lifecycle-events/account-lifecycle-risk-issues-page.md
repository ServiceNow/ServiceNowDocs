---
title: Risk and issues page
description: This page provides detailed information about a risk signal including risk occurrences, threshold values, and risk solution.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Risk portfolio dashboard, Using customer success, Customer success, Customer Success Management]
---

# Risk and issues page

This page provides detailed information about a risk signal including risk occurrences, threshold values, and risk solution.

To view this page, follow these steps:

1.  Login as a user with the `sn_acct_lc.ale_success_agent` role.
2.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workpace** and select the **List** icon.
3.  Navigate to **Customer Success** &gt; **All Risks and Issues** and click **Number** column to open the record. You can also navigate to this page from the [Risk portfolio dashboard](account-lifecycle-risk-portfolio.md).

![Risks and issues page](../image/account-lifecycle-risk-issues.png)

You can see the following details:

-   Engagement details: This section shows the details of the engagement for which the risk signal has been generated. It includes the Contract value, Stage, Next Renewal date, Health, and so on.
-   Risk signal details: The risk signal details including probability, tracking method, category, and so on. See [Create a risk signal](../task/account-lifecycle-create-risk-signal.md) for details.
-   Risk occurrence: List of risk occurrences based on the scheduled job. This includes the start and end dates on which the scheduled job was executed, the current value, threshold value, and the gap. Click on the link to drill down to the Risk Occurrence page.

The following options are available:

-   Discuss: Click **Discuss** to start a sidebar discussion about this risk signal. In the popup window, select the participants who need to participate in the discussion, enter a brief message, and click **Start discussion**. A window appears with a link to the record. Click **Open record** and start the discussion. When the discussion has been completed, you can see the details in the Activity stream.
-   Create success play: See [Create a success play](../task/account-lifecycle-create-success-play.md)
-   Export: Click **Export** to export the risk occurrences or solutions to an Excel file.

