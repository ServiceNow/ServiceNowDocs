---
title: Restart a playbook
description: Restart a playbook from the beginning, an activity, or a stage.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Running playbooks, Use, Workflow Studio, Build workflows]
---

# Restart a playbook

Restart a playbook from the beginning, an activity, or a stage.

## Before you begin

Role required: agent or pd\_restarter

If your playbook admin has enabled restart in your playbook, you can find the restart action in the action menus of the playbook, stages, or activities. If you are an admin and would like to enable and configure restart for a playbook in Workflow Studio, see [Enable and Configure Restart for Playbooks](enable-define-restart.md).

If a stage or activity is not configured to be restartable, you will not see all of the buttons in this procedure.

**Note:** Certain activities within a playbook cannot be restarted once they have started. Playbooks in a Cancelled, Complete, or Error state also cannot be restarted. However, the opposite is true for activities and stages. Activities and stages must be complete or in an error state before they can be restarted.

## Procedure

1.  Restart playbook
2.  **Note:** Playbooks in a **Complete**, **Error**, or **Cancelled** state cannot be restarted.

    Open your playbook.

3.  To restart the whole playbook:

    1.  Hover over the playbook name in the contextual side panel to open the context menu![context menu](../../../common/image/icon-menu.png).

    2.  Select **Restart playbook**.

        ![Restart playbook button in the context menu](../images/restart-playbook-pe.png)

4.  Restart stage
5.  Open your playbook.

6.  **Note:** Stages and activities must be completed or in an error state before they can be restarted. When a stage or activity is restarted, you may need to:

-   Complete all restartable stages and activities after it again.
-   Re-enter information to complete restartable stages and activities again.
    To restart a stage:

    1.  Hover over the name of the stage in the contextual side panel to open the context menu![More actions menu](../../../common/image/icon-menu.png).

    2.  Select **Restart stage**

        ![Restart stage button in the context menu](../images/restart-stage-pe.png)

        .

7.  Restart activity
8.  Open your playbook.

9.  **Note:** Stages and activities must be completed or in an error state before they can be restarted. When a stage or activity is restarted, you may need to:

-   Complete all restartable stages and activities after it again.
-   Re-enter information to complete restartable stages and activities again.
    To restart an activity:

    1.  In the activity card, open the context menu.

    2.  Select **Restart**.

        ![Restart button in activity card context menu](../images/restart-activity-pe.png)


**Parent Topic:**[Running playbooks](../../workspace/concept/playbook-agents-and-fulfillers.md)

