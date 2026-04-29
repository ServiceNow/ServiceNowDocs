---
title: Nested Playbooks
description: Embed or "nest" a child playbook within a parent playbook to organize your processes and then present the appropriate sequence of steps in the runtime experience. Creating child playbooks that can be used in other parent playbooks enables you to define sets of activities that can be re-used across multiple playbooks to avoid duplication.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Design Playbook Experience, Playbooks, Workflow Studio, Build workflows]
---

# Nested Playbooks

Embed or "nest" a child playbook within a parent playbook to organize your processes and then present the appropriate sequence of steps in the runtime experience. Creating child playbooks that can be used in other parent playbooks enables you to define sets of activities that can be re-used across multiple playbooks to avoid duplication.

Using nested playbooks can also enable you to break up very large playbooks so they are easier to maintain, and they can load faster in Playbook Designer.

## About nested playbooks

When building child playbooks they must be of the Standalone execution type. This means that they are launched manually and not with an automated trigger. When you create a new playbook and select the Standalone execution type, you can also select a check box that allows the playbook to be nested in a parent playbook. The "nestable" playbook must be activated to be visible in the picker for selection as a nestable playbook in a parent playbook.

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

1.  Build a child playbook that can be nested in a parent playbook. For information about this step, see [Create a nestable child playbook](../task/create-nestable-child-playbook.md).
2.  Build a parent playbook that can host the child playbook. For more information about this step, see [Create a parent playbook to host a nestable child playbook](../task/create-parent-playbook.md).

