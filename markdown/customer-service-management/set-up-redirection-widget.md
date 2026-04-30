---
title: Set up a redirection widget
description: You can set up a widget to reroute the user to the csm\_ticket page once the record state changes from draft to new, indicating that the user has completed the intake process.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-04-15"
reading_time_minutes: 1
breadcrumb: [Set up custom Playbooks for Portals, Playbooks for Portals, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Set up a redirection widget

You can set up a widget to reroute the user to the `csm_ticket` page once the record state changes from draft to new, indicating that the user has completed the intake process.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Widgets**.

2.  Open the widget **CSM Intake Redirect**.

3.  Add the following code the in the client controller section.

    **Note:** As a best practice, clone the **CSM Intake Redirect** widget to modify and replace it on the `csm_intake` page, or on your custom page.

    ```
    spUtil.recordWatch($scope, 'sn_customerservice_case', c.data.filter, function(response) { //replace sn_customerservice_case with your table.
    
            if (response.data.operation == "update" && response.data.record.state && response.data.record.state.value != "0") { //checking if the state is not draft
    
                if (($window.location.href).indexOf('?id=csm_ticket&') == -1);
                $window.location = "?id=csm_ticket&table=" + c.data.table + "&sys_id=" + c.data.sys_id;
            }
        });
    ```

4.  Select **Update**.


