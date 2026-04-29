---
title: Export a process to Playbook
description: Export a process to Playbooks to use the advanced features available from Workflow Studio to improve your processes. This feature works with Now Assist.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Analyzing and getting process insights, Use, Process Mining, Platform Analytics]
---

# Export a process to Playbook

Export a process to Playbooks to use the advanced features available from Workflow Studio to improve your processes. This feature works with Now Assist.

## Before you begin

Role required: sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin. You must have the playbook.write roles.

## About this task

This task enables you to export any variant from within your process to playbook. This gives you more flexibility to work on your process. You can add more triggers, subflows, or attach a parallel process. This feature is enabled by Now Assist.

**Note:** You can export a maximum of 10 variants for a process graph.

The property for the playbook generation is set in the Process Mining system properties. For more information, see [Playbook generation properties](../concept/data-cleanup.md#).

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining workspace**.

2.  Select a project for which you want to analyze the graph.

3.  Select the Analyst workbench.

4.  Select a variant that you want to analyze from the **Variants** tab.

5.  Select **Apply**.

6.  Select **Playbooks** icon \(![Playbooks icon](../image/playbook-icon.png)\).

    ![Selecting variants to generate playbook](../image/playbook-1.png)

    The Playbooks panel is displayed.

7.  Select **Create playbook**.

    The Playbooks form is displayed.

    ![Playbooks panel](../image/playbook-2.png)

8.  Fill the Playbooks form.

    1.  Provide a name for the playbook that you want to generate.

        Provide an intuitive name.

    2.  Select **Attach snapshot**.

        This option takes a snapshot of the process graph that you want to export to Playbooks. This snapshot is attached to the playbook record on Analyst workbench. You can refer to the snapshot later to understand what is exported to Playbooks.

    3.  Select **Generate**.

        Workflow Studio opens where the playbook is generated for the selected process graph.

9.  Save and edit the playbook that is generated in Workflow Studio.

    In Workflow Studio, the name, and Now Assist prompt is displayed. You can choose to edit them and regenerate the preview.

    For information on Playbooks on Workflow Studio, see [Exploring Playbook](https://www.servicenow.com/docs/access?context=process-automation-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US).


**Parent Topic:**[Analyzing and getting process insights](../concept/analyze-get-process-insights.md)

