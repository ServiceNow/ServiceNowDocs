---
title: Enable a reflow for your UI Builder pages
description: Enable a reflow for your UI Builder pages. This way, when you’re resizing a window, you don't have to scroll horizontally.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Playbooks for Portals, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Enable a reflow for your UI Builder pages

Enable a reflow for your UI Builder pages. This way, when you’re resizing a window, you don't have to scroll horizontally.

## Before you begin

Role required: admin

## About this task

The reflow feature adjusts the properties of the components when you’re resizing a window. It accommodates smaller screen sizes and changes the component’s properties for the different screen sizes.

## Procedure

1.  Navigate to **All** &gt; **UI Builder**.

2.  Under **Experiences**, select **Playbook Experience Portal**.

3.  Open a specific page or variant: Either **CSM Create Case Process** or **CSM Case Process**, for which you want to adjust the reflow.

4.  Edit the **Playbook Activity Viewer** component settings.

5.  On the **Styles** tab in the UI Builder, set the height of the activity viewer to 100vh.

6.  Navigate to the component **Resizeable Panes** &gt; **Panes configuration** and copy the code in the default displayed pane by editing the scripted property value.

    ```
    // Resizable Panes default displayed pane scripted value
    ​
    // when in left/right pane position
    function evaluateProperty({api, helpers}) {
        if(!api.data.playbook_custom_layout.compactMode) return "both";
    ​
      return (api.data.playbook_custom_layout.selectedItem || {}).stageContextId ? "right" : "left";
    }
    ​
    // when in top/bottom pane position
    function evaluateProperty({api, helpers}) {
        if (!api.data.playbook_custom_layout.compactMode) return "both";
    
      return (api.data.playbook_custom_layout.selectedItem || {}).stageContextId ? "bottom" : "top";
    }
    ```

7.  Select **Done**.

    For more details, see [Reflow for playbook components](https://www.servicenow.com/docs/access?context=reflow-for-playbook-components&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).


