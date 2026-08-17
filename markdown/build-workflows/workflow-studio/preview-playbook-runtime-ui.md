---
title: Preview an activity's runtime UI
description: See how an activity will appear to end users when the playbook runs. Use the preview to confirm the activity's appearance in real-time, and adjust its configuration before publishing the playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/preview-playbook-runtime-ui.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-06-24"
reading_time_minutes: 1
breadcrumb: [Creating and managing Playbooks, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Preview an activity's runtime UI

See how an activity will appear to end users when the playbook runs. Use the preview to confirm the activity's appearance in real-time, and adjust its configuration before publishing the playbook.

## Before you begin

Role required: playbook\_experience.admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Studio** &gt; **Playbooks**.

2.  Select the playbook you want to preview.

3.  On the diagram canvas, hover over an activity card to display its toolbar, and then select the Edit UI Layout icon \[Omitted image "playbook-edit-button.png"\].

    The activity configuration panel opens with the UI preview open. Selecting the Edit icon opens the configuration panel without the UI preview open.

4.  Select **Show UI preview** to view the runtime appearance of the activity.

    \[Omitted image "pe-show-preview.png"\] Alt text: Screenshot showing the location of the Show UI preview button.

    The **Activity runtime UI preview** panel appears alongside the configuration tabs.

5.  Switch from **Example UI** to **Your UI** to view your configurations with sample data.

    \[Omitted image "pe-UI-live.png"\] Alt text: Screenshot showing the Your UI switch and the Tagline being updated live.

6.  Make changes to the activity configuration to build the runtime experience you want.

    The live preview updates in real-time to reflect your changes.

7.  Add sample data that displays in the UI Layout preview for a field in an activity that uses record inputs, for example a Record Form activity.

    When pills are unresolvable, an option to provide sample data is provided. The sample data entered for the field appears across all other instances of the same input field in other activities in the designer.

    1.  In the activity configuration panel, select the **UI Layout** tab.

    2.  Under **Associated Record**, enter a table to reference in the **Associated table** field.

    3.  Select the Data pill picker icon \[Omitted image "data-pill-picker-icon.png"\] Alt text: Data pill picker icon next to the **Associated record** field.

        If the data pill can't be resolved the option to add sample data is enabled.

    4.  Select **Add sample data for this pill**.

        \[Omitted image "playbook-add-sample-data.png"\] Alt text: Screenshot of the Add sample data for this pill option.

    5.  Select a record to use as sample data.

    6.  Select **Save and close** before leaving.

8.  Select **Hide UI preview** to dismiss the runtime view.

9.  Select **Save and close**.


**Parent Topic:**[Creating and managing Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/creating-managing-playbooks.md)

