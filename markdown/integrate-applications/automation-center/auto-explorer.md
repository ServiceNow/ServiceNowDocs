---
title: Explore automations
description: Automation explorer enables you to scan your entire ServiceNow instance and discover relevant automations based on a targeted query. You can filter by automation type, execution time period, and application scope, then onboard high-value automations directly to Automation Center for ROI tracking.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/automation-center/auto-explorer.html
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 2
breadcrumb: [Use, ServiceNow Otto for Automation Center, Use, Automation Center, Workflow Data Fabric]
---

# Explore automations

Automation explorer enables you to scan your entire ServiceNow® instance and discover relevant automations based on a targeted query. You can filter by automation type, execution time period, and application scope, then onboard high-value automations directly to Automation Center for ROI tracking.

## Before you begin

Role required: sn\_ac.automation\_technical\_user

Run the fix script to be able to view the results of the Automation explorer. For information, see [Run fix script to view results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/automation-center/run-script.md).

**Note:** You can control how catalog items are onboarded as automations using the sn\_ac.auto\_onboarding\_catalog\_items system property. Users with sn\_ac.automation\_admin can edit the system property.

-   True \(default\): New catalog items are onboarded automatically and appear on the automation dashboard immediately. However, the time and cost savings aren't displayed.
-   False: New catalog items are onboarded manually using the Automation Explorer feature. Generating this data takes longer, but the dashboard shows an expanded summary with time and cost savings for each catalog item.

## Procedure

1.  Navigate to **Workspaces** &gt; **Automation Center Workspace**.

2.  Select the **Automation explorer** tab.

    \[Omitted image "auto-explorer-land.png"\] Alt text: Automation explorer tab

    You can select the automation type card at the outset or select **Discover automations** button. Both actions launch an agent-driven conversation via the ServiceNow Otto panel, which guides you through defining your search criteria step by step

3.  Select your search method.

<table id="choicetable_rrb_zjf_q3c"><tbody><tr><td id="d92118e123">

**If you know the automation type**

</td><td>

Select the relevant automation type card to begin a focused search.

</td></tr><tr><td id="d92118e132">

**If you don't know the automation type**

</td><td>

Select the open-ended search button to launch the ServiceNow Otto panel and start an agent-guided conversation.

</td></tr></tbody>
</table>4.  In the ServiceNow Otto panel, respond to the agent prompts to define your search criteria.

    The agent asks three questions to scope your search:

    1.  Select the automation type you want to search for \(for example, Flows\).

    2.  Select the time period in which the automations were executed \(for example, Last 30 days\).

        You can also enter a custom time value if the predefined options don't meet your requirements.

    3.  Select the application scope for the search \(for example, All\).

    The agent scans your instance within the defined scope and retrieves matching automations. This process may take a few minutes depending on the instance size and search scope.

5.  Select **Show** to view the search results.

    \[Omitted image "auto-show-result.png"\] Alt text: Show results

    The results display all relevant automations on the instance against the search query, including:

    -   AI-estimated cost saving per run.
    -   AI-estimated time saving per run.
    -   An explanation for the AI-generated estimates.
6.  Select one or more automations to estimate the value \(time and cost saved\) and then onboard.

    Use the check-boxes next to each automation, and select **Estimate value**, and **Onboard**. Review the cost and time saving estimates and the accompanying AI explanation to make your decision.

    \[Omitted image "auto-esti-onboard.png"\] Alt text: Estimate value of automations and onboard them


## Result

The selected automations are onboarded to Automation Center. Their cost savings and time savings are now tracked and visible in the Automation Center Value dashboard.

## What to do next

After onboarding, monitor the ROI of your automations in the Automation Center Value dashboard. You can return to Automation explorer at any time to discover additional automations or refine your search criteria.

**Parent Topic:**[Using ServiceNow Otto for Automation Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/automation-center/use-now-assist.md)

