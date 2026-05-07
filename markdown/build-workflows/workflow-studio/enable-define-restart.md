---
title: Configure restart for Playbooks
description: Configure restart so that agents and fulfillers in Playbook Experience can restart a playbook from the beginning, or from a specific stage or activity.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Enabling playbook restart, Creating and managing Playbooks, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Configure restart for Playbooks

Configure restart so that agents and fulfillers in Playbook Experience can restart a playbook from the beginning, or from a specific stage or activity.

## Before you begin

Role required: pd\_author

**Note:** Once restart is enabled for a playbook, it cannot be disabled. If you don't want agents to be able to restart a playbook or its activities and stages, do not perform the following task.

## Procedure

1.  Enable restart for an entire playbook.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio** and select **Playbooks**.

        The Playbooks list displays.

    2.  Open the playbook you want to enable restart for.

        The Playbooks builder displays.

    3.  In the upper right-hand corner, open the **More actions menu**![More actions menu](../images/icon-horizontal-menu.png), and select **Properties**.

        The **Additional Properties** modal displays.

    4.  At the bottom of the **General** tab, select the **Allow this process to be restarted during runtime** box.

        ![](../images/restart-playbook-setting.png)

        Agents can now restart the whole playbook.

        **Note:** Restart can be enabled for activities and stages even if the whole playbook cannot be restarted.

2.  Define restart rules for each stage and activity.

    **Note:** Restart settings for a stage do not apply to its activities. Each activity also has its own restart settings.

    1.  In the Playbooks builder, open the stage or activity you want to configure restart settings for.

    2.  Under **Restart rules**, select what you want the stage or activity to do when restarted.

        ![Activity and stage restart rules in the side panel](../images/playbooks-restart-rules.png)

<table id="choicetable_kcx_5sn_tzb"><thead><tr><th align="left" id="d113657e202">

Rule

</th><th align="left" id="d113657e205">

Description

</th></tr></thead><tbody><tr><td id="d113657e211">

**Skip on restart**

</td><td>

The stage or activity only runs during a playbook's initial run. It never runs during a restarted run.**Note:** This setting is helpful if you don't want new tasks or records to be created during a restarted run, because the original execution and resulting record is still relevant.

</td></tr><tr><td id="d113657e225">

**Run always**

</td><td>

The stage or activity always runs, whether during an initial or restarted run.

</td></tr><tr><td id="d113657e234">

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


**Parent Topic:**[Enabling playbook restart](../concept/restart.md)

