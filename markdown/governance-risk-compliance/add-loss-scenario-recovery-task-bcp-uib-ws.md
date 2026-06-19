---
title: Add loss scenarios
description: Add a loss scenario and define the related asset dependencies in your business continuity plan. You can then view the details of the assets in BCM UIB Workspace and then plan a recovery strategy for an identified loss scenario.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/add-loss-scenario-recovery-task-bcp-uib-ws.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Add loss scenarios

Add a loss scenario and define the related asset dependencies in your business continuity plan. You can then view the details of the assets in BCM UIB Workspace and then plan a recovery strategy for an identified loss scenario.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager, or sn\_bcm.planner

## About this task

If the plan was created from a plan template, loss scenarios may already be pre-configured. When the plan template's "Synchronize loss scenario assets with recovery strategy assets" option is enabled, asset lists are kept in sync with the recovery strategy automatically.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  In the List view, navigate to **Planning** and select the link to the plan record in the **Name** column.

3.  Select the **Loss scenarios** tab and select **Add**.

    You can add a loss scenario to the business continuity plan. In the example, you can select the Loss of Datacenters loss scenario and add it to the business continuity plan.

    \[Omitted image "loss-scenarios-list.png"\] Alt text: Add a loss scenario.

    The loss of scenario record is displayed as shown in the example.

    \[Omitted image "loss-scenarios-details-tab.png"\] Alt text: Loss of scenario record with the tabs.

4.  Navigate to **Related asset dependencies** tab and select **Add**.

    You can add the related asset dependencies to the loss of scenario as shown in the example.

    \[Omitted image "loss-scenarios-add-rel-asset-dep.png"\] Alt text: Add the related asset dependencies to the loss of scenario.

5.  Select the dependencies from the list and select **Add**.

    You can add the dependencies to the loss of scenario as shown in the example.

    \[Omitted image "loss-scenarios-add-dep.png"\] Alt text: Add the dependencies that are related to the assets.

6.  Select **Save**.

    The related asset dependencies are listed on the **Related asset dependencies** tab.

    Starting with the Australia release of the application, the Loss scenario record has the following related lists:

    -   Task template groups
    -   Task templates
    -   Recovery strategies
    -   Plan templates

## What to do next

After the loss scenario is created, you can populate its **Recovery tasks** tab in bulk by selecting **Add groups** or **Add tasks**. The **Select task template groups** dialog automatically filters by the loss scenario's element definition \(for example, only groups applicable to Datacenters are shown for a Loss of Datacenters scenario\). For field-level details, see [Add recovery tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-a-recovery-task.md).

\[Omitted image "plan-loss-scenario-form.png"\] Alt text: Loss of Datacenters plan-loss-scenario record showing the Details tab.

**Parent Topic:**[Structured workflows for BCPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcp-tasks-performed-by-bcp-owner.md)

