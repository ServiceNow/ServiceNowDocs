---
title: Preview an activity's runtime UI
description: See how an activity will appear to end users when the playbook runs. Use the preview to confirm the activity's appearance as you work, and adjust its configuration before you activate the playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/preview-playbook-runtime-ui.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-06-24"
reading_time_minutes: 2
breadcrumb: [Creating and managing Playbooks, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Preview an activity's runtime UI

See how an activity will appear to end users when the playbook runs. Use the preview to confirm the activity's appearance as you work, and adjust its configuration before you activate the playbook.

## Before you begin

Role required: playbook.admin

## About this task

The preview appears in the activity property panel, beside the **Details**, **Automation**, and **UI Layout** tabs. It renders the activity as configured at design time. Automations don't run at design time, so a component that depends on an automation output has no data to draw on. That component isn't shown, the area collapses, and no placeholder appears in its place. A component can therefore be missing from the preview and still appear when the playbook runs. Components that draw on experience properties render as you configure them.

## Procedure

1.  Navigate to **All** &gt; **Workflow Studio** &gt; **Playbooks**.

2.  Select the playbook containing the activity you want to preview.

3.  On the diagram canvas, hover over an activity card to display its toolbar, and then select the Edit UI Layout icon \[Omitted image "playbook-edit-button.png"\].

    The activity property panel opens on the **UI Layout** tab with the preview open. Selecting the Edit icon opens the panel without the preview.

4.  If the preview is hidden, select **Show UI preview** to open it.

    \[Omitted image "pe-show-preview.png"\] Alt text: Screenshot showing the location of the Show UI preview button.

    The **Activity runtime UI preview** panel appears alongside the configuration panel.

5.  Configure the activity's experience properties on the **UI Layout** tab.

    \[Omitted image "pe-UI-live.png"\] Alt text: Screenshot showing the Your UI switch and the Tagline being updated live.

    The preview switches from **Example UI** to **Your UI** at your first change. Single-line fields such as **Title** and **Tagline** update as you type. **Description** updates when you move focus away from the field. An activity with no values in its experience property fields shows an empty card container, which is expected.

6.  Add sample data that displays in the UI Layout preview for a field in an activity that uses record inputs, for example a Record Form activity.

    When a data pill can't be resolved, a sample data field appears beneath the experience property. For a record data pill, the value you supply applies to every reference to that pill in the same playbook. Sample data populates the preview only and has no effect on runtime.

    1.  In the activity property panel, select the **UI Layout** tab.

    2.  Under **Associated Record**, enter a table to reference in the **Associated table** field.

    3.  Select the Data pill picker icon \[Omitted image "data-pill-picker-icon.png"\] Alt text: Data pill picker icon next to the **Associated record** field.

        If the data pill can't be resolved the option to add sample data is enabled.

    4.  Select **Add sample data for this pill**.

        \[Omitted image "playbook-add-sample-data.png"\] Alt text: Screenshot of the Add sample data for this pill option.

    5.  Select a record to use as sample data.

        If you can't select a record, the record list is still loading.

    6.  If you couldn't select a record, select **Save and close**, reopen the activity, and then select the record.

        Selecting **Save and close** also saves any other unsaved changes on the activity.

7.  Select **Hide UI preview** to dismiss the runtime view.

8.  Select **Save and close** to close the preview.


**Parent Topic:**[Creating and managing Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/creating-managing-playbooks.md)

