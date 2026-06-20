---
title: Configure restart for Playbooks
description: Configure restart so that agents and fulfillers in Playbook Experience can restart a playbook from the beginning, or from a specific stage or activity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/workflow-studio/enable-define-restart.html
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [Enabling playbook restart, Playbooks in Workflow Studio, Building playbooks, Use, Workflow Studio, Build workflows]
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

    3.  In the upper right-hand corner, open the **More actions menu**\[Omitted image "icon-horizontal-menu.png"\] Alt text: More actions menu, and select **Properties**.

        The **Additional Properties** modal displays.

    4.  At the bottom of the **General** tab, select the **Allow this process to be restarted during runtime** box.

        \[Omitted image "restart-playbook-setting.png"\] Alt text:

        Agents can now restart the whole playbook.

        **Note:** Restart can be enabled for activities and stages even if the whole playbook cannot be restarted.

2.  Define restart rules for each stage and activity.

    **Note:** Restart settings for a stage do not apply to its activities. Each activity also has its own restart settings.

    1.  In the Playbooks builder, open the stage or activity you want to configure restart settings for.

    2.  Under **Restart rules**, select what you want the stage or activity to do when restarted.

        \[Omitted image "playbooks-restart-rules.png"\] Alt text: Activity and stage restart rules in the side panel

<table id="choicetable_kcx_5sn_tzb"><thead><tr><th align="left" id="d55658e202">

Rule

</th><th align="left" id="d55658e205">

Description

</th></tr></thead><tbody><tr><td id="d55658e211">

**Skip on restart**

</td><td>

The stage or activity only runs during a playbook's initial run. It never runs during a restarted run.**Note:** This setting is helpful if you don't want new tasks or records to be created during a restarted run, because the original execution and resulting record is still relevant.

</td></tr><tr><td id="d55658e225">

**Run always**

</td><td>

The stage or activity always runs, whether during an initial or restarted run.

</td></tr><tr><td id="d55658e234">

**Skip on first run**

</td><td>

The stage or activity runs only during restarted runs. It never runs during an initial run.

</td></tr></tbody>
</table>    Your restart rules are applied.

    -   Restart settings are reflected in both the Diagram view and Board view of the Workflow Studio Playbooks builder.

        \[Omitted image "run-always.png"\] Alt text: Run always icon on a stage in Diagram view

        \[Omitted image "skip-first-run-board.png"\] Alt text: Skip on first run icon on an activity in board view

    -   Restart buttons are added to context menus in your playbook.

        \[Omitted image "restart-stage-pe.png"\] Alt text: Restart stage button in context menu during runtime

3.  To test your playbook with the restart options, select **Test** in the upper right-hand corner and open the **Playbook preview**.

    \[Omitted image "restart-playbook-pe.png"\] Alt text: Restart playbook button in context menu in Playbook preview


**Parent Topic:**[Enabling playbook restart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/restart.md)

