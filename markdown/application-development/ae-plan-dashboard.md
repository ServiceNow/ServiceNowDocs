---
title: Using the dashboard
description: The Autonomous Engineer dashboard displays the status of every work item in your plan and provides navigation to individual work items, milestones, and pre-flight verification items.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ae-plan-dashboard.html
release: brazil
topic_type: concept
last_updated: "2026-09-09"
reading_time_minutes: 3
keywords: [Autonomous Engineer, Build Agent, plan dashboard, work items, milestones, pre-flight verification, Overview tab, Work items tab]
audience: programmer
breadcrumb: [Overview, Autonomous Engineer, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Using the dashboard

The Autonomous Engineer dashboard displays the status of every work item in your plan and provides navigation to individual work items, milestones, and pre-flight verification items.

After you approve a plan, the dashboard opens in Autonomous Engineer. The dashboard updates as background agents complete work items, so you can track progress without leaving the editor. The dashboard has two tabs: **Overview** and **Work items**. To return to a previous plan or find plans created by other users, use the **Plans** view in the Build Agent navigator panel. For more information, see .

## Overview tab

The **Overview** tab shows the plan header and two sections: **Pre-flight verification** and **Milestones**.

The plan header displays the plan title, a status badge, and a last-updated timestamp. The status badge reflects the overall state of the plan as work items progress.

-   **Pre-flight verification**

    The pre-flight verification section appears when one or more work items have blockers that require action before or during execution. The section has two subsections:

    -   **Install required plugins**

        Lists any plugins that work items depend on, with the installation state of each. Use the inline link to navigate to the plugin installation page for each plugin listed.

    -   **Complete manual work items**

        Lists implementation steps that Autonomous Engineer can't perform autonomously. Each item includes instructions for completing the step manually. Complete all manual steps before execution begins to help reduce the risk that dependent work items fail.

    When all pre-flight blockers are resolved, the section collapses.

    **Note:** The section does not appear for plans that have no pre-flight requirements.

-   **Milestones**

    The **Milestones** section lists the subplans that make up the current plan. Each row shows the milestone name and the number of work items it contains. Select the drill-down arrow on a milestone row to open that subplan's own **Overview** tab. Use the breadcrumb navigation at the top of the dashboard to return to a parent plan at any depth.

    The dashboard updates the work item counts and statuses in the **Milestones** section as execution progresses.

-   **Update sets**

    When the plan completes, a batch update set is available and includes all the update sets for the work items for the plan.


## Work items tab

The **Work items** tab lists every work item in the current plan scope. Each row shows the work item name, its current state, and any relevant status indicators. The list updates incrementally as background agents progress through execution, so you don't have to refresh the dashboard.

Select a work item row to open the work item record. From there you can:

-   Read the generated artifacts and Test Agent \(ATF\) test results. For more information, see [Test Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/test-agent-landing-page.md).
-   Edit the work item content and ask Autonomous Engineer to retry.
-   Roll back the changes for that work item if the output doesn't meet your requirements. For more information, see [Checkpoints and conversation change log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ba-conversational-change-log.md).
-   When the work item completes, an update set is available and includes all the changes for the work item.
-   Mark the work item complete when you're satisfied with the results.

\[Omitted image "ae-work-items-dash.png"\] Alt text: Dashboard showing work item execution progress and status counts. For details, refer to the surrounding description.

Work items that require your attention, for example because they failed automated retries or surfaced a question during execution, are highlighted in the list and chat panel.

## Chat panel context

While the Autonomous Engineer dashboard is open, the chat panel displays the context of the active plan. Use the chat panel to ask questions about plan progress, check the status of specific work items, and respond to questions that background agents surfaced during execution.

**Parent Topic:**[Exploring Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/exploring-autonomous-engineer.md)

