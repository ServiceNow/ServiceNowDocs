---
title: Discovery Home page
description: The Discovery Home page provides a summary of discoveries that were triggered by cloud and non-cloud schedules. You can view any errors that occurred during a Discovery and find remediation suggestions. Use the Home page view to examine the cloud resources discovered for the service accounts you selected in a cloud schedule. From the ServiceNow Home page, you can view the Discovery errors that occurred during a Discovery and get suggestions for resolving these errors. You can view the errors for all schedules or for a single schedule.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Discovery monitoring and issue resolution, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Home page

The Discovery Home page provides a summary of discoveries that were triggered by cloud and non-cloud schedules. You can view any errors that occurred during a Discovery and find remediation suggestions. Use the Home page view to examine the cloud resources discovered for the service accounts you selected in a cloud schedule.

To open the Discovery Home page, navigate to **Discovery** &gt; **Home**. The Home page shows the Discovery totals for each of the following categories. Click a tile to see details for that category.

![Discovery Home page](../image/DiscoHomeSummary.png)

<table id="table_home-page-categories"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td id="entry-item1">

Schedules

</td><td>

The number of Discovery schedules that are configured to find cloud resources and virtual machines \(IP addresses\).

 Click **View Schedules** to open the CI schedule view, where you can see specific details about each CI schedule separately. View the results of your cloud or IP address schedules and create new schedules.

</td></tr><tr><td id="entry_item2">

Discovered Devices

</td><td>

The total number of device CIs discovered. Devices include all the CIs in tables that extend the Hardware \[cmdb\_ci\_hardware\] table, such as Computer \[cmdb\_ci\_computer\] and Cisco UCS Equipment \[cmdb\_ci\_ucs\_equipment\].

</td></tr><tr><td id="entry_item3">

Cloud Resources

</td><td>

The total number of resources \(virtual machines\) discovered for the service accounts selected. See [Enable discovery of virtual machines](discovery-manager.md#) for details about setting up Discovery for your cloud resources.

 Click **View Cloud Resources** to open a list of discovered cloud resources, by type.

</td></tr><tr><td id="entry_item4">

Errors

</td><td>

The total number of unresolved errors that occurred during discovery.

 Click **View Errors** to drill down to specific types of errors.

</td></tr></tbody>
</table>## Viewing all schedules

The schedule view displays details for each schedule that ran for the selected filter. By default, the list shows all the Discovery schedules in alphabetical order, regardless of their current running status.

![Default view of aggregated Discovery schedules](../image/DiscoScheduleMgrDefault.png)

Use these controls to filter Discovery results by schedules:

-   **Schedule filters**

    You have the choice of these filters:

    -   **All**: Results of all Discovery schedules that ran. This is the default filter.
    -   **Cloud Schedules**: Results of all Cloud Discovery schedules that ran. When you select this filter, a second filter appears, allowing you to display cloud schedules by **Service Account**.

        ![Cloud schedule filters](../image/DiscoScheduleMgrCloud.png)

    -   **IP Based Schedules**: Results of all Discovery schedules that ran for Configuration Items \(CI\), using IP ranges. When you select this filter, a second filter appears, allowing you to display the CI schedules by a specific location or all locations.

        ![IP-based schedule filters](../image/CloudIPBasedFilter.png)

-   **Schedule sorter**

    From the schedule selector in the left pane, select a sorting criteria, from left to right:

    ![Cloud schedule sorting selections](../image/CloudScheduleSorter.png)

    -   Errors for each schedule listed.
    -   Unidentified IP addresses.
    -   Recent activity, which lists the schedules that are currently running first.
    -   Alphabetical listing of schedules.
-   **Schedule list**

    List of available Discovery schedules. Select a schedule to display its details. Click the pencil icon at the top of the page to edit the schedule.

-   **Date/time indicator**

    Date and time the selected schedule ran.

-   **Schedule topics**

    Tiles that show the Discovery result categories for the selected schedule. Click a tile to see more detail.

    -   **Cloud resources**: Displays the total number of CIs updated or created for this filter.
    -   **Virtual Machines**: Displays the total number of virtual machines discovered with the selected schedule.
    -   **Errors**: Displays the total number of errors that occurred from running the selected schedule.
    -   **Datacenters**: Displays the number of datacenters selected during the creation of the Discovery schedule.
-   **Cloud resources trend chart**

    Trend graph for the selected schedule. Each circle in the graph represents a specific Discovery run.

    Place the cursor over any circle to see a summary of that Discovery.

    ![Resource trend chart detail](../image/discovery-trend-circle.png)

    Click the circle to filter the values you see in the Discovery topics. The results populate the appropriate tiles above the graph.

-   **Errors by category**

    Category tiles for the errors encountered during the Discovery for the selected schedule. Click a tile to view the errors in that category and to see recommended actions for remediation. See [Discovery error messages](c_DiscoveryErrorMessages.md) for additional details.

-   **Discovered cloud resources**

    Breakdown of the cloud resources discovered for the selected schedule, presented in a horizontal bar chart.

-   **Add schedules**

    Types of schedules to add.

    ![Add cloud schedule selections](../image/CloudScheduleOptions.png)

-   **Advanced View**

    Displays the Discovery status record for the selected schedule. Use this link to examine the results of the schedule in the ECC Queue and the Discovery log.


## Viewing IP-based schedules

To display results from IP range discoveries, select **IP Based Schedules** in the primary filter. Use the secondary field that appears to filter the search results by **Location**. The tiles show the result categories for the selected IP-based schedule. Click a tile to see more detail.

-   **Discovered devices**: Total count of virtual machines discovered by the IP-based schedule, including both targeted and unidentified IP addresses.
-   **Errors**: Displays the total number of errors encountered running the selected IP-based schedule.
-   **Unidentified IPs**: Count of unidentified CIs discovered by the IP-based scheduled.
-   **Targeted IPs**: Count of CIs found that were configured in the IP-based schedule.

![Virtual machine view in the Discovery Home page](../image/DiscoScheduleMgrVM.png)

## Resolve CI Discovery Schedule errors

From the ServiceNow Home page, you can view the Discovery errors that occurred during a Discovery and get suggestions for resolving these errors. You can view the errors for all schedules or for a single schedule.

### Before you begin

Role required: discovery\_admin

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Home**.

    The summary page for all schedules appears.

    ![CI schedule summary](../image/DiscoHomeSummary.png)

2.  View the errors, using one of these methods:

    -   Click the **Errors** tile to see the errors by category for all CI discovery schedules.
    -   Click the **Schedules** tile to display the errors for a single schedule.
        1.  In the summary screen, select the schedule that you want to investigate for errors.

            If you have numerous schedules, you can filter by location, using the location dropdown list, or filter by the schedule name in the **Search by name** field.

            ![CI schedule results](../image/CIScheduleMgrFilter.png)

        2.  After you select the schedule, click the **Errors** tile.
        3.  Scroll down to view the errors by category.

            ![Errors by category for a schedule](../image/CIScheduleMgrErrorbyCat.png)

3.  Click a category tile to display the specific error codes that occurred in that category.

4.  Click the tile for the error code you want to investigate.

    ![Errors by category](../image/CIScheduleMgrCategories.png)

    The list displays all occurrences of that error code, either for a single CI schedule or for all schedules, depending on the path you took to view the errors. The list shows the IP address of each instance that experienced the error and the error status **Active error**. The **Recommended Actions** pane on the right contains the recommended action for the selected error. The **ACTION ON ALL** pane contains operations you can execute on all the errors in the list.

    ![Automation Error Messages filter](../image/CIScheduleMgrErrorControls.png)

5.  Click **View instructions** to see details and remediation suggestions for the error code.

    ![Error details and remediation instructions](../image/CIScheduleMgrErrorInst.png)

6.  To begin work, either select the check box next to an error to resolve that specific error or select an action for **ALL** to resolve that error code for all instances of that error.

    In this example, the system recommends creating new Windows credentials to resolve this error code.

    ![Error detail and recommended actions](../image/CIScheduleMgrErrorDetail.png)

7.  Complete the suggested remediation tasks before attempting to retry Discovery.

    In this example, the **Create new Windows Credentials** link opens a form for creating and testing new Windows credentials.

    ![Create new Windows credentials](../image/CIScheduleMgrWinCred.png)

8.  After all the recommended tasks are complete, click **Retry Discovery**.

    A possible course of action might be to retry Discovery for **ALL** instances after creating the credentials. The new credentials might solve the issue for all the instances experiencing this error code.

9.  Check the **Error Status** column to see the results of your remediation efforts.

    Single retries complete quickly. Retries for large numbers of IP addresses can take several minutes.

    An error can have one of these statuses:

    -   **Active error**: Unresolved error. This is the default status of all new errors.
    -   **Resolved**: Resolved error. The recommended actions show Error successfully resolved.
    -   **Assigned**: Task assigned to resolve this error. Click **Create a task** to assign a user to a task for all active errors. Assigned errors are considered **Active errors**, and actions can still be performed on them.
    -   **Pending Discovery**: Waiting for Discovery to start after you execute the **Retry Discovery** action on all errors.
    -   **In Discovery**: Discovery is currently active.

**Related topics**  


[Discovery status](c_DiscoveryStatus.md)

[Review the logs for horizontal discovery](../reference/r_DiscoveryLog.md#)

[The ECC queue for Discovery](../reference/r_DiscoveryStatusECCQueue.md)

[Create discovery schedules for cloud resources](discovery-manager.md#)

