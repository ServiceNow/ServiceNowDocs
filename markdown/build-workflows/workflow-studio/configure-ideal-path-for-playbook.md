---
title: Configure the ideal path for a playbook
description: Mark one or more decision branches as the ideal path in Workflow Studio for a playbook. The playbook can highlight the expected execution route and show users a preview of upcoming activities at runtime.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/configure-ideal-path-for-playbook.html
release: brazil
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-08-21"
reading_time_minutes: 2
breadcrumb: [Ideal path for a playbook, Creating and managing Playbooks, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Configure the ideal path for a playbook

Mark one or more decision branches as the ideal path in Workflow Studio for a playbook. The playbook can highlight the expected execution route and show users a preview of upcoming activities at runtime.

## Before you begin

The playbook must contain at least one decision activity before you can configure an ideal path.

For more information about ideal path, see [Ideal path for a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/ideal-path-for-playbook.md).

Role required: admin, playbook.admin, pd\_author, or playbook.write.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Open the playbook for which you want to configure the ideal path.

3.  Enable **Ideal branch** for all decision activities in the playbook.

    \[Omitted image "playbook-ideal-path.png"\] Alt text: Enable the ideal branch for the branches you want to set up as the ideal.

    If you have more than two branches in a decision, depending on the selected **Branch processing approach**, you may be able to select one or more branches as the ideal branch.

    |Option|Description|
    |------|-----------|
    |**Process only the first matching branch**|Only one branch can be marked as ideal. Use this when the decision should resolve into a single outcome.|
    |**Process all matching branches**|Multiple branches can be marked as ideal. Use this when more than one branch can represent an expected outcome.|

    1.  Select a decision activity.

    2.  In the **Branches** tab, under Branches, enable **Ideal branch** for the branch or branches that represent the expected execution path.

    3.  Select **Save and close**.

4.  To view the ideal path of execution for the playbook, from the toolbar, select **View options** &gt; **Golden path**.

    \[Omitted image "playbook-golden-path-toggle.png"\] Alt text: Enable golden path from the view options toggle to view the ideal execution path of the playbook.

    The ideal path of execution is highlighted on the canvas.


## What to do next

Configure Playbook Experience to display the ideal path activities and stages before they are executed at runtime. For more information, see [Configure Playbook Experience to display ideal path](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/configure-playbook-experience-ideal-path.md).

**Parent Topic:**[Ideal path for a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/ideal-path-for-playbook.md)

