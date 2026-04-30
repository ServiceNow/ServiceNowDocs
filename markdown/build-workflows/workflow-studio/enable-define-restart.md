---
title: Enable and Configure Restart for Playbooks
description: Configure your playbook so that agents and fulfillers in Playbook Experience can restart a playbook from the beginning, or from a specific stage or activity.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Restart, Playbooks in Workflow Studio, Building playbooks, Use, Workflow Studio, Build workflows]
---

# Enable and Configure Restart for Playbooks

Configure your playbook so that agents and fulfillers in Playbook Experience can restart a playbook from the beginning, or from a specific stage or activity.

## Before you begin

Role required: pd\_author

When you open an existing playbook in Workflow Studio for the first time after upgrading to the Process Automation Designer 25.1.2 ServiceNow Store app, a banner message notifies you to enable restart for your playbook. You must enable the restart feature before you can perform the task below.

![Restart notification in Workflow Studio](../images/restart-enable-message.png)

This message only displays for existing playbooks. Restart is automatically enabled for new playbooks and does not change any other features and functions.

**Note:** Once enabled, restart cannot be disabled. If you don't want agents to be able to restart a playbook or the activities and stages in a playbook, do not perform the following task.

## Procedure

1.  Enable restart for an entire playbook.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio** and select **Playbooks**.

        The Playbooks list displays.

    2.  Open the playbook you want to enable restart for.

        The Playbooks builder displays.

    3.  In the upper right-hand corner, open the **More actions menu**![More actions menu](../images/icon-horizontal-menu.png), and select **Properties**.

        The **Additional Properties** modal displays.

    4.  At the bottom of the **General** tab, check the **Allow this process to be restarted during runtime** box.

        ![](../images/restart-playbook-setting.png)

        Agents can now restart the whole playbook.

        **Note:** Restart can be enabled for activities and stages even if the whole playbook cannot be restarted.

2.  Define restart rules for each stage and activity.

    **Note:** Restart settings for a stage do not apply to its activities. Each activity also has its own restart settings.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio** &gt; **Playbooks**.

        The Playbooks list displays.

    2.  Open the playbook you want to configure stage or activity restart settings for.

        The Playbooks builder displays.

    3.  Open the stage or activity you want to configure restart settings for.

        ![Activity and stage restart rules in the side panel](../images/playbooks-restart-rules.png)

    4.  Select what you want the stage or activity to do when restarted.

<table id="choicetable_kcx_5sn_tzb"><thead><tr><th align="left" id="d111585e284">

Rule

</th><th align="left" id="d111585e287">

Description

</th></tr></thead><tbody><tr><td id="d111585e293">

**Skip on restart**

</td><td>

The stage or activity only runs during a playbook's initial run. It never runs during a restarted run.**Note:** This setting is helpful if you don't want new tasks or records to be created during a restarted run, because the original execution and resulting record is still relevant.

</td></tr><tr><td id="d111585e307">

**Run always**

</td><td>

The stage or activity always runs, whether during an initial or restarted run.

</td></tr><tr><td id="d111585e316">

**Skip on first run**

</td><td>

The stage or activity runs only during restarted runs. It never runs during an initial run.

</td></tr></tbody>
</table>    Your restart rules are applied.

    -   Restart settings are reflected in both the Diagram view and Board view of the Workflow Studio Playbooks builder.

        ![Run always icon on a stage in Diagram view](../images/run-always.png)

        ![Skip on first run icon on an activity in board view](../images/skip-first-run-board.png)

    -   Restart buttons are added to context menus in your playbook.

        ![Restart stage button in context menu during runtime](../images/restart-stage-pe.png)

3.  To test your playbook with the restart options, select **Test** in the upper right-hand corner and open the **Playbook preview**.

    ![Restart playbook button in context menu in Playbook preview](../images/restart-playbook-pe.png)


**Parent Topic:**[Restart](../concept/restart.md)

