---
title: Apply Reflow to playbook components
description: Apply reflow to out-of-the-box standalone and custom layout Playbook Experience components so that the UI adjusts when you resize your window o r zoom.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reflow for playbook components, Design Playbook Experience, Playbooks, Workflow Studio, Build workflows]
---

# Apply Reflow to playbook components

Apply reflow to out-of-the-box standalone and custom layout Playbook Experience components so that the UI adjusts when you resize your window o r zoom.

## Before you begin

Role required: admin

## Procedure

1.  Create the sys\_ux\_auto\_reflow\_rule record.

    1.  Open the **All** menu.

    2.  In the filter bar, type and enter **sys\_ux\_auto\_reflow\_rule.list**.

    The **UX Auto Reflow Rules** list is created and displays.

    There is a rule for each of the playbook standalone and custom layout components. When under a certain UI Builder page size, these rules use the default Reflow engine to override macroponent properties in the **UX Macroponent Definitions** list \(**sys\_ux\_macroponent.list**\) and certain CSS values. The rules provided in the Playbook Experience store apps use a 640px page width to toggle the components' **compactMode** property, as well as a 100vh height to ensure the components resize to fit the space.

    If you're using the standalone component, you are done. If you are working with custom layout components, proceed to the next step.

2.  Navigate to **All** &gt; **UI Builder**.

3.  Open the layout you want to apply Reflow to in Playbook Experience Builder.

4.  In the bottom left corner, select the **Data** icon and open the **Playbook Custom Layout** UI controller.

5.  In the **Activity View Mode** field, update the value for the **stagePickerVisible** output property to **true**.

6.  Select the component that you want the Reflow rule to apply to.

7.  Under the **Events** tab, add the **Compact Mode Changed** event handler.

    This automatically turns Compact Mode on and off according to the Reflow rule, by changing the value of the **compactMode** output property to true or false. This is then applied to the other components of your playbook so that everything automatically resizes as well.

8.  Select **Resizable panes**.

    1.  Update the **Panes position** to show in the **left and right** orientation, or as **top and bottom** panes.

    2.  Under the **Config** tab, open the scripted property value the **Default displayed pane** field.

    3.  Update the value for **if\(!api.data.playbook\_custom\_layout.compactMode\) return** to show only the **"left"**/**"top"** pane, only the **"right"**/**"bottom"** pane, or **"both"** panes when not in Compact Mode.

    4.  For Compact Mode, update the first value for **return \(api.data.playbook\_custom\_layout. selectedItem \|\| \(\)\).stageContextId ?** to show the **"left"**/**"top"** or **"right"**/**"bottom"** activity pane when a stage is selected.

        The second value indicates which pane to show when a stage is not selected.


