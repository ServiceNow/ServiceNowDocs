---
title: Risk and issues page
description: This page provides detailed information about a risk signal including risk occurrences, threshold values, and risk solution.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Risk portfolio dashboard, Customer success, Use, Customer Success Management]
---

# Risk and issues page

This page provides detailed information about a risk signal including risk occurrences, threshold values, and risk solution.

To view this page, follow these steps:

1.  Login as a user with the `sn_acct_lc.customer_success_agent` role.
2.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workpace** and select the **List** icon.
3.  Navigate to **Customer Success** &gt; **All Risks and Issues** and select **Number** column to open the record. You can also navigate to this page from the [Risk portfolio dashboard](account-lifecycle-risk-portfolio.md).

\*\*\* to be updated \*\*\*

![Risks and issues page](../image/account-lifecycle-risk-issues.png)

You can see the following details:

-   Engagement details: This section shows the details of the engagement for which the risk signal has been generated. It includes the Contract value, Stage, Next Renewal date, Health, and so on.
-   Risk signal details: The risk signal details including probability, tracking method, category, and so on. See [Create a risk signal](../task/account-lifecycle-create-risk-signal.md) for details.
-   Risk occurrence: List of risk occurrences based on the scheduled job. This includes the start and end dates on which the scheduled job was executed, the current value, threshold value, and the gap. Select the link to drill down to the Risk Occurrence page.

The following options are available:

-   **Recommend solutions**: Recommends and executes success plays to address the risk signal. The Now Assist panel opens up and starts the workflow for the specific risk.

    **Note:** This option is available only for unaddressed risks and requires the Now Assist for TMT to be installed.

-   **Discuss**: Select this option to start a sidebar discussion about this risk signal. In the pop-up window, select the participants who must participate in the discussion, enter a brief message, and select **Start discussion**. A window appears with a link to the record. Select **Open record** and start the discussion. When the discussion has been completed, you can see the details in the Activity stream.
-   **Create success play**: See [Create a success play](../task/account-lifecycle-create-success-play.md)

    The success play created from a risk signal is automatically tagged as a risk solution record.

-   **Export**: Select **Export** to export the risk occurrences or solutions to an Excel file.

## Recommend solutions

This option identifies and executes success plays that address an unaddressed risk.

1.  Select **Recommend Solution**. The Now Assist panel opens and automatically starts the agentic workflow for that specific risk signal.
2.  The Now Assist panel displays up to three solution options, each containing one or more success plays. The solutions are arrived at using the following approaches:
3.  -   Machine learning similarity model: Identifies past risks similar to the current risk and recommends the success plays that resolved those risks. Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solution Definitions**. Select the **Risk similarity** solution definition that is available with the base system and do the following:
    -   Select the **Active** check box to enable this similarity solution.
    -   Select **Update &amp; Retrain**. The similarity definition uses the short description and description of all closed risk signals to build a similarity index. Once trained, it identifies risks similar to the current risk signal and recommends the success plays that were used to resolve past risks.
-   AI Search: If AI Search is enabled, similar solutions are identified based on the risk details.
-   Decision table: Identifies the Customer Success definition mapped to the risk category and recommends the associated success plays.
    If none of these approaches return results, a link is provided to manually browse the catalog and run a success play.

4.  The first solution option is the recommended one but you can select one of the three solution options. You're prompted to provide the required inputs for each success play within the selected option.

    **Note:** Multiple success plays within the selected solution are run sequentially.

5.  Provide the required inputs, such as the planned start date and planned end date, for each success play. Once all the inputs have been provided, the success plays are initiated and run in the background. Optionally, you can select additional plays from the success catalog.
6.  After the plays have been completed, the solutions are automatically added to the Risk solutions related list on the risk signal record.
7.  A scheduled job runs every day and automatically identifies risk signals that are eligible for closure and generates closure notes. See [Draft close notes for a risk signal using Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/draft-risk-close-notes.md) for details.
8.  When the risk is closed, closure notes are automatically generated and are visible in the Activity stream and Closure Notes in the risk record.

    **Note:** Closure notes are automatically generated only when the **Draft closure notes** skill is enabled, all associated risk solutions are closed, and no new risk occurrences exist for the risk signal.


**Parent Topic:**[Risk portfolio dashboard](account-lifecycle-risk-portfolio.md)

