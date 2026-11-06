---
title: Nested Playbooks
description: Embed or "nest" a child playbook within a parent playbook to organize your processes and then present the appropriate sequence of steps in the runtime experience. Creating child playbooks that can be used in other parent playbooks enables you to define sets of activities that can be re-used across multiple playbooks to avoid duplication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/build-workflows/workflow-studio/nested-playbooks.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-10-16"
reading_time_minutes: 4
breadcrumb: [Playbooks patterns, Playbooks, Workflow Studio, Build workflows]
---

# Nested Playbooks

Embed or "nest" a child playbook within a parent playbook to organize your processes and then present the appropriate sequence of steps in the runtime experience. Creating child playbooks that can be used in other parent playbooks enables you to define sets of activities that can be re-used across multiple playbooks to avoid duplication.

Using nested playbooks can also enable you to break up very large playbooks so they are easier to maintain, and they can load faster in Playbook Designer.

## About nested playbooks

When building child playbooks, they must be of the Standalone execution type. This means that they are launched manually and not with an automated trigger. When you create a new playbook and select the Standalone execution type, select a check box that allows the playbook to be nested in a parent playbook. The "nestable" playbook must be activated to be visible in the picker for selection as a nestable playbook in a parent playbook.

-   **Permissions**

    Nested \(child\) playbook must have the same runtime permissions as the parent.

-   **Inserting optional activities**

    In this release, nested playbooks don't support inserting optional activities at runtime. Parent playbooks can still include optional activities, but insertion points are restricted to the parent playbook. Optional activities from the parent can't be inserted within a child playbook.

-   **Restarting playbooks**

    Restart is not supported on individual activities or stages that belong to a nested playbook. A restart of the whole nested playbook can be performed when the nested playbook is restarted from the parent playbook. The restart behavior of the nested playbook from the parent playbook is based on the following restart rules that are defined for the **Launch Nested Playbook** activity:

    -   **Skip on restart**: The nested playbook is not cancelled and continues to run.
    -   **Run always**: The nested playbook is cancelled, and a new nested playbook is triggered when the launch nested playbook activity starts again.
    -   **Skip on first run**: The nested playbook is only triggered when the parent playbook is restarted. It then follows the **Run always** rule behavior after subsequent restarts.
-   **How nested playbooks are affected by cancellation**

    Cancellation of the parent playbook automatically terminates the child playbook. Child playbooks can be cancelled by using the UI or an API.


## Process to build nested playbooks

Building nested playbooks is a two-part process:

1.  Build a child playbook that can be nested in a parent playbook. For information about this step, see [Create a nestable child playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/create-nestable-child-playbook.md).
2.  Build a parent playbook that can host the child playbook. For more information about this step, see [Create a parent playbook to host a nestable child playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/create-parent-playbook.md).

## Passing data between parent and child playbooks

A nested playbook runs as a separate process from its parent, so data doesn't pass between them automatically the way it does between activities in a single playbook. Two activities move data across the boundary. The **Launch Nested Playbook** activity in the parent carries values into the child, and the **Set Playbook Outputs** activity in the child returns values to the parent.

-   **Inputs into the child playbook**

    Define the inputs on the child playbook, and then map a value to each input on the **Launch Nested Playbook** activity in the parent. A value can be fixed, or it can come from a data pill for the trigger record, the parent table, or an earlier activity. The supported input types are String, Multi Line, and Reference.

    Define the inputs on the **Inputs &amp; Outputs** tab of the child playbook's properties, and then map a value to each input on the nested playbook activity in the parent. A value can be fixed, or it can come from a data pill for the trigger record, the parent table, or an earlier activity.

-   **Values from the person running the playbook**

    Add a **Questionnaire** activity to the parent before the **Launch Nested Playbook** activity, and then map the answers to the child inputs by using data pills. For more information, see [Questionnaire activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/questionnaire-activity.md).

-   **Outputs from the child playbook**

    To return values to the parent, the child playbook declares its outputs on the **Inputs &amp; Outputs** tab, and a **Set Playbook Outputs** activity sets their values. In the parent, the outputs are then available as data pills, so later activities, experience properties, and conditions can use them. Only activities that start before the target activity appear in the data pill picker.


The child playbook must define its inputs and outputs before you can map data to or from it in the parent.

## Example: Budget validation

A budget approval playbook launches a child playbook that validates a budget proposal. At the end of its run, the child uses a **Set Playbook Outputs** activity to return two true or false outputs. One shows whether the budget is over the limit, and the other shows whether documents are missing.

In the parent, a decision evaluates every branch whose condition is true. When the budget is over the limit, one branch routes the proposal for director review. When documents are missing, another branch requests them. Because the two outputs are independent, a single child result can start both branches.

