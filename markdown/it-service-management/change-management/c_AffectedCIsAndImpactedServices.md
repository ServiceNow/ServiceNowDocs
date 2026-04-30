---
title: Associated CIs on a change request
description: You can associate additional CIs or services to change requests through related lists on the Change Request form. You can also associate CIs with a change request from the dependency views map.You can use dependency views to identify dependent CIs affected by a change request, and then add them to the Affected CIs related list.You can associate multiple impacted or affected CIs with a single change request.From the change request form, you can add an affected CI that is associated with a calculated application service.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Process a change request, Using Change Management, Change Management, IT Service Management]
---

# Associated CIs on a change request

You can associate additional CIs or services to change requests through related lists on the Change Request form. You can also associate CIs with a change request from the dependency views map.

The **Affected CIs** and **Impacted Services/CIs** related lists enable you to manage CI changes.

When you first access a change request and work with these related lists, you can identify CIs across CI classes using configuration class. You can change the configuration class manually to filter the list and narrow the selection of CIs. For example, to filter for Linux servers only, select **Linux Servers** as the **Configuration Class**.

You can also create and save filters to provide quick access to common CI searches. The next time you access the change request, the **Configuration Class** field displays the last associated CI class. This automatic filter ensures that relevant CIs are displayed.

After identifying the CIs affected by a change request, you can add them to the **Affected CIs** related list on the change request. After saving affected CIs, you can open the form context menu and select the **Refresh Impacted Services** option. This option populates the **Impacted Services/CIs** related lists based on the primary CI i.e. the CI that is mentioned on the form.

The **Impacted Services/CIs** and **Service Offering** related lists represents a many-to-many relationship between the Task \[task\] and CMDB \[cmdb\_ci\] tables. The related list displays CIs, such as business services or other CI classes, and the offerings that are impacted. You can add this related list to any task form such as an incident or problem form. You can also enter the details of the impacted services and the service offerings manually, as required.

**Note:**

-   The manually added CIs are not deleted each time the impacted services are refreshed. However, business services related to the CIs are displayed on the **Impacted Services/CIs** related list.
-   Refresh Impacted Services was only available for Change Request table. From this release, it is available for tables that extend the Task table. The list of these tables is driven by the **com.snc.task.refresh\_impacted\_services** property. This UI action populates the Impacted Services/CIs related list based on the primary CI i.e. the CI that is mentioned on the form.
-   The Impacted Services list includes application services discovered by Service Mapping.

**Parent Topic:**[Process a change request](../task/t_ProcessAChangeRequest.md)

## Add affected CIs to change requests using dependency views

You can use dependency views to identify dependent CIs affected by a change request, and then add them to the **Affected CIs** related list.

### Before you begin

Role required: itil, sn\_change\_write, or admin

### About this task

When a change request is associated with a configuration item, the change record becomes accessible from dependency views. Services affected by the change request are easy to assess in dependency views.

If not visible, the administrator can configure the change request form to display the **Affected CIs** related list.

### Procedure

1.  In the change request, click the dependency views icon next to the **Configuration item** field.

    **Note:** If there are critical change requests attached to a CI for a database, the map includes the business services that rely on that database. The database icon has a blinking glyph on the lower left edge that indicates any issues with the node.

    The configuration item is displayed in the map with all dependent CIs.

2.  Click the down arrow next to the CI to display a list of tasks and issues with the CI.

    The list may contain one or more change requests, and follow-on audit tasks. You can open each record from this list.

3.  Click the task number to display the complete list of tasks attached to this CI.

    You can view the user assigned to the change and also open the record for more information.

4.  To change the map configuration, select a format from the **Layout** field or use the filter panel to filter the map.

    The dependency views map highlights the affected CIs that depend on the database or other CI.

5.  To add an affected CI to the change, click the arrow next to the highlighted node and select **Add Affected CIs**.

6.  Reload the change request form.

    You can view the CI you added in the **Affected CIs** related list.


## Associate multiple CIs with a change request

You can associate multiple impacted or affected CIs with a single change request.

### Before you begin

Role required: itil, change\_manager, sn\_change\_write, or admin

### About this task

Use the **Configuration Item** &gt; **Configuration** &gt; **CI Class Manager**.

In the Affected CIs related list, a new filter is added for the Principal Class. You can control this functionality by the system property **com.snc.task.principal\_class\_filter**. The property contains all the task types where the Principal Class filter is applied to.

When you create a change request, you can add multiple CIs to that change request using the **Affected CIs** or **Impacted Services/CIs** related lists in the change record. Affected CIs can be added only when the change request is in the **New** state.

### Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Open** and select a change request record.

2.  In either the **Affected CIs** or **Impacted Services/CIs** related list, click **Add**.

    ![Add CIs](../image/Create-Change-select-CIs-0.png)

3.  Select the appropriate CIs from the list of CIs displayed in the pop-up window.

    The pop-up window for the **Affected CIs** list is filtered for the configuration class of the last added CI. This automatic filter ensures that relevant CIs are displayed. You can change the class to list other CIs, if appropriate.

    ![Affected items pop-up window displays the same CI class](../image/Create-Change-select-CIs-1.png)

    The **Impacted Services/CIs** pop-up window lists all CIs and provides standard filtering options. You can also save any filters you create to provide faster access to common CI searches.

4.  Perform one of the following actions.

    -   Select the CIs to add and click **Add Selected** to add the selected CIs to the change request.
    -   Click **Add All** to add all the CIs in the list to the change request.

**Related topics**  


[Mass Update CI](bulk-ci-change.md)

## Add an affected CI with a calculated application service

From the change request form, you can add an affected CI that is associated with a calculated application service.

### Before you begin

Role required: itil, sn\_change\_write, or admin

### Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Open**.

2.  Select a change request to add affected CIs to.

3.  On the Change Request form, scroll to the Related Links section.

4.  Click the **Affected CIs** tab and then click **Add** to add an affected CI to the change request.

    **Note:** You can export the Affected CIs in an excel. Right click on the change request and open in a new window. Right click on **Configuration Item**, and select **Export Excel**.

5.  Open the form context menu and click **Refresh Impacted Services**.

6.  Click the **Impacted Services/CIs** tab to see any dynamic services that are associated with the affected CI and that are impacted by the change request.


