---
title: Explore automations
description: Automation explorer enables you to scan your entire ServiceNow instance and discover relevant automations based on a targeted query. You can filter by automation type, execution time period, and application scope, then onboard high-value automations directly to Automation Center for ROI tracking.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 2
breadcrumb: [Use, Now Assist for Automation Center, Use, Automation Center, Workflow Data Fabric]
---

# Explore automations

Automation explorer enables you to scan your entire ServiceNow® instance and discover relevant automations based on a targeted query. You can filter by automation type, execution time period, and application scope, then onboard high-value automations directly to Automation Center for ROI tracking.

## Before you begin

Role required: sn\_ac.automation\_technical\_user

Run the fix script to be able to view the results of the Automation explorer. For information, see [Run fix script to view results](run-script.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Automation Center Workspace**.

2.  Select the **Automation explorer** tab.

    ![Automation explorer tab](../images/auto-explorer-land.png)

    You can select the automation type card at the outset or select **Discover automations** button. Both actions launch an agent-driven conversation via the Now Assist Panel, which guides you through defining your search criteria step by step

3.  Select your search method.

<table id="choicetable_rrb_zjf_q3c"><tbody><tr><td id="d99851e107">

**If you know the automation type**

</td><td>

Click the relevant automation type card to begin a focused search.

</td></tr><tr><td id="d99851e116">

**If you do not know the automation type**

</td><td>

Click the open-ended search button to launch the Now Assist Panel and start an agent-guided conversation.

</td></tr></tbody>
</table>4.  In the Now Assist Panel, respond to the agent prompts to define your search criteria.

    The agent asks three questions to scope your search:

    1.  Select the **automation type** you want to search for \(for example, Flows\).

    2.  Select the **time period** in which the automations were executed \(for example, Last 30 days\).

        You can also enter a custom time value if the predefined options do not meet your requirements.

    3.  Select the **application scope** for the search \(for example, All\).

    The agent scans your instance within the defined scope and retrieves matching automations. This process may take a few minutes depending on the instance size and search scope.

5.  Select **Show** to view the search results.

    ![Show results](../images/auto-show-result.png)

    The results display all relevant automations on the instance against the search query, including:

    -   AI-estimated **cost saving per run**.
    -   AI-estimated **time saving per run**.
    -   An explanation for the AI-generated estimates.
6.  Select one or more automations to estimate the value \(time and cost saved\) and then onboard.

    Use the check-boxes next to each automation, and select **Estimate value**, and **Onboard**. Review the cost and time saving estimates and the accompanying AI explanation to make your decision.

    ![Estimate value of automations and onboard them](../images/auto-esti-onboard.png)


## Result

The selected automations are onboarded to Automation Center. Their cost savings and time savings are now tracked and visible in the Automation Center Value dashboard.

## What to do next

After onboarding, monitor the ROI of your automations in the Automation Center Value dashboard. You can return to Automation explorer at any time to discover additional automations or refine your search criteria.

**Parent Topic:**[Using Now Assist for Automation Center](../concept/use-now-assist.md)

