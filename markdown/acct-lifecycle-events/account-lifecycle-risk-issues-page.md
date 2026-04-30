---
title: Risk signal and issues page
description: This page provides detailed information about a risk signal including risk occurrences, threshold values, and risk solution.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Risk portfolio dashboard, Customer success, Use, Customer Success Management]
---

# Risk signal and issues page

This page provides detailed information about a risk signal including risk occurrences, threshold values, and risk solution.

To view this page, follow these steps:

1.  Login as a user with the `sn_acct_lc.customer_success_agent` or `sn_acct_lc.agent` role.
2.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workpace** and select the **List** icon.
3.  Navigate to **Customer Success** &gt; **All Risk Signal and Issues** and select **Number** column to open the record. You can also navigate to this page from the [Risk portfolio dashboard](account-lifecycle-risk-portfolio.md).

![Risks signal and issues page.](../image/account-lifecycle-risk-issues.png)

You can see the following details:

-   Engagement details: This section shows the details of the engagement for which the risk signal has been generated. It includes the Contract value, Stage, Next Renewal date, Health, and so on.
-   Risk signal details: The risk signal details including probability, tracking method, category, and so on. See [Create a risk signal](../task/account-lifecycle-create-risk-signal.md) for the details.
-   Risk occurrence timeline: List of risk occurrences based on the scheduled job. This includes the dates on which the scheduled job was created, executed, the current value, engagement health, and the threshold value.
-   Summarize: Generates a summary from a risk signal and issues summarization record and all associated tasks. See [Summarize a risk signal and issues using Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-risk-signals-issues&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US) to generate the summary.

The following options are available:

-   Discuss: Select **Discuss** to start a sidebar discussion about this risk signal. In the pop-up window, select the participants who must participate in the discussion, enter a brief message, and select **Start discussion**. A window appears with a link to the record. Select **Open record** and start the discussion. When the discussion has been completed, you can see the details in the Activity stream.
-   Create success play: See [Create a success play](../task/account-lifecycle-create-success-play.md)
-   Export: Select **Export** to export the risk occurrences or solutions to an Excel file.

## Contextual side panel component

The contextual side panel component includes different tools that agents can use to research and resolve customer issues. The contextual side panel in the Risk Signal and Issues record page includes the following tabs.

<table id="table_dts_xpn_ghc"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Recommended Actions**

</td><td>

The Recommended Actions tab includes [AI search](https://www.servicenow.com/docs/access?context=ra-csm-ai-search&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) functionality. Agents can use AI search to find relevant resources or resolutions for customer issues.The search feature displays an initial set of search results based on the text in the risk record short description. This initial set of results includes knowledge articles. Agents can also enter different search keywords and repeat the search.

From the list of search results, agents can do the following:

-   Select a source to see search results of that type.
-   Filter the list of search results.
-   Sort the list of search results.
-   Open the search results in full view in a record subtab.
-   Take the following actions:
    -   View and attach article
    -   Perform other actions such as reading articles in full view, flagging articles, or marking articles as helpful or unhelpful.
-   View successful actions by selecting the Actions history icon.

For more information, see [Use AI search in Recommended Actions to resolve cases](https://www.servicenow.com/docs/access?context=nba-use-ai-search&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

**Note:** Using Recommended Actions in the contextual side panel requires the [Recommended Actions](https://www.servicenow.com/docs/access?context=nba&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) application \(sn\_cs\_nb\_action\) which is included with the CSM Configurable Workspace application.

</td></tr><tr><td>

**Activity Stream**

</td><td>

The activity stream component displays a list of the activities occurring on a risk record.

</td></tr><tr><td>

**Related Items**

</td><td>

The Related Items tab provides access the risk record-related lists. New risk can be created from the related items.The risk signal and issues record page incorporate related list functionality into the contextual side panel. These lists appear in an accordion format that agents can expand and collapse as needed.

An indicator displays the number of risk records available in a related list. When expanded, the records in a related list are displayed in card format.

The Related Items tab shows the list of items:

-   **Emails**: View the consolidated emails that are related to the risk record.
-   **Risk Impacted Records**: View the records that are related to the risk record.
-   **Risk Occurrences**: Navigate to the risk record.
-   **Documents**: View the documents that are related to the risk record.

</td></tr><tr><td>

**Template**

</td><td>

The Templates tab provides access to available form templates that enable agents to automatically populate fields on new records. Agents can manually apply a template when creating a record such as an incident or change.

</td></tr><tr><td>

**Attachment**

</td><td>

The Attachments tab provides access to risk record-related attachments. From this tab, agents can view and download attachments.

</td></tr></tbody>
</table>**Parent Topic:**[Risk portfolio dashboard](account-lifecycle-risk-portfolio.md)

