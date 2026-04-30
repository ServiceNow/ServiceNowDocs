---
title: Lifecycle Events workflows
description: The HR Activity Set Launcher workflow drives the entire lifecycle event process. Associated workflows drive each of the activity sets within a lifecycle event.
locale: en-US
release: zurich
product: Lifecycle Events
classification: lifecycle-events
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Lifecycle Event Workflow]
breadcrumb: [Activate Lifecycle Events, Configure, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Lifecycle Events workflows

The **HR Activity Set Launcher** workflow drives the entire lifecycle event process. Associated workflows drive each of the activity sets within a lifecycle event.

When a lifecycle event case is created:

-   The **Invoke Activity Set Launcher Workflow** business rule runs.
-   The **HR Activity Set Launcher** workflow starts.
-   The workflow runs during the lifecycle event case and manages the activity sets.

    **Note:** You can access the workflows from **Execution Contexts**.


![Activity set workflow diagram.](../image/LEWorkflow1-Brand2.png)

Each activity set in a lifecycle event has an associated workflow. Each workflow:

-   Monitors trigger conditions and dependencies on other activity sets to generate activities.
-   Checks the status of activities in the workflow every four hours \(default\) for activity sets triggered by date or a custom script.
-   Checks the status of activities when an activity case or request is updated.
-   Closes the activity set when activities are marked complete.

    The base system limits the total number of activity sets that can run at the same time to 25. This value can be increased, but system performance can be affected.

    **Note:** The **Evaluation interval** field is not revealed by default. This field works with the **Max activity count** field on the **Activities** tab under Workflow Properties. See [Workflow properties](https://www.servicenow.com/docs/access?context=r_WorkflowProperties&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) . If you reveal the **Evaluation interval** field with the intention of changing the default value \(four hours\), use caution. Frequent updates mean that more events fire and could cause your lifecycle event activity sets to cancel before the Lifecycle Event completes. For workflows associated with Lifecycle Events, the value of the **Max activity count** field has been increased to accommodate long running business processes that contain multiple workflow activities. For an alternative method, see [Lifecycle Events evaluation interval](le-evaluation-interval1.md).

    1.  Open Workflow Editor.
    2.  From Workflows, select **HR Activity Set Launcher**.
    3.  Under Parallel Flow Launcher, click the **Activity Properties**.
    4.  Update the **Max Simultaneous** value.

        See [Parallel Flow Launcher workflow activity](https://www.servicenow.com/docs/access?context=r_ParallelFlowLauncher&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) .


**Parent Topic:**[Activate Lifecycle Events](../task/activate-enterprise-onboarding-and-transitions-scoped.md)

