---
title: Custom interactive filter examples
description: As an administrator, you can create custom interactive filter widgets to provide advanced filtering options on dashboards.Create custom interactive filter widgets to provide advanced filtering options on dashboards.After you create the interactive filter, add the filtering logic.When the standard selection of date/time filter options doesn't meet your needs, you can create a custom option.You can use a custom interactive filter to filter multiple reports using different tables. There are two different APIs to publish an interactive filter for a single table or multiple tables. This example filters a report on the incident and problem tables by assignment group using a custom interactive filter.
locale: en-US
release: zurich
product: Interactive Filters
classification: interactive-filters
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Custom interactive filters, Interactive Filters, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Custom interactive filter examples

As an administrator, you can create custom interactive filter widgets to provide advanced filtering options on dashboards.

## Use case

This example details how to create a custom filter to filter reports on the Task table, or its child tables. The filter only shows records where the current user is the caller. The filter exposes two buttons to the user, one button to add the filter and one to remove the filter.

**Parent Topic:**[Custom interactive filters](../concept/c_CustomPublishers.md)

**Related topics**  


[Configure a content block](https://www.servicenow.com/docs/access?context=t_CreateAContentBlock&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)

[UI scripts](https://www.servicenow.com/docs/access?context=c_UIScripts&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

[Jelly tags](https://www.servicenow.com/docs/access?context=r_JellyTags&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

[DashboardMessageHandler](../../../app-store/dev_portal/API_reference/DashboardMessageHandler/concept/c_DashboardMessageHandler.md#)

## Create a custom interactive filter widget

Create custom interactive filter widgets to provide advanced filtering options on dashboards.

### Before you begin

Role required: admin

### Procedure

1.  Open a dashboard that you want to add the custom interactive filter to.

2.  Click the add content icon \(![Add content icon](../image/icon-add-user-db.png)\).

3.  From the **Widget Category** list, select `Content Blocks`.

    ![Widget category menu with Content Blocks selected](../image/add-content-block-db-polaris.png)

4.  From the list of content blocks, select `New Dynamic Content`.

5.  In the New Dynamic Content panel, click **Add**.

    ![New Dynamic Content widget option](../image/add-new-dynamic-content.png)

    A new Dynamic Content block is added to the dashboard.

6.  On the dashboard, click the link that says **Click here to configure this reusable Dynamic Content block**.

    ![New Dynamic Content widget option](../image/add-new-dynamic-content-config.png)

7.  Define the filtering logic in the **Dynamic content** field.

    ![Dynamic content - New record](../image/db-custom-interactive-filter-ex.png)


### What to do next

Define the filtering logic.

## Define filtering logic - example

After you create the interactive filter, add the filtering logic.

### Before you begin

Role required: admin

Filters use the DashboardMessageHandler class to manage active filters. Instantiate DashboardMessageHandler with a unique value.

**Note:** The ID of the custom interactive filter must be unique. If it has the same ID as another interactive filter or custom interactive filter, the filtering logic does work properly.

### Procedure

1.  In the dynamic content record, add the filtering logic to the Dynamic content XML block.

2.  The **Only mine** button publishes a filter on Task table reports using the encoded query `caller_idDYNAMIC90d1921e5f510100a9ad2572f2b477fe`.

    The **All tasks** button removes the filter.

3.  You can then add buttons or other interface elements to the dynamic content. In this example, the code for the `clearFilter()` function and the buttons in the filter are added below the `publishFilter()` function.

    ```
    <?xml version="1.0" encoding="utf-8" ?>
    <j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
     <script>
         var my_dashboardMessageHandler = new DashboardMessageHandler("my_unique_id");
        
        function publishFilter () {
            var filter_message = {};
            filter_message.id = "my_unique_id";
            filter_message.table = "task";
        
        <!--     Add your own filter query logic here -->
            filter_message.filter = "assigned_toDYNAMIC90d1921e5f510100a9ad2572f2b477fe";
            SNC.canvas.interactiveFilters.setDefaultValue({
                    id: filter_message.id,
                    filters: [filter_message]
                }, false);
            my_dashboardMessageHandler.publishFilter(filter_message.table, filter_message.filter);
        }
        
        function clearFilter() {
            var filter_message = {};
            filter_message.id = "my_unique_id";
            filter_message.table = "task";
            filter_message.filter = "";
            SNC.canvas.interactiveFilters.setDefaultValue({
                    id: filter_message.id,
                    filters: [filter_message]
                }, false);
            my_dashboardMessageHandler.removeFilter();
        }
     </script>   
     
    Example of a filter that generates a static filter on 'task' table reports, or removes it <br/>
        <input id="allTasks" type="button" value="All tasks" onclick="clearFilter();" />
        <input id="onlyMine" type="button" value="Only mine" onclick="publishFilter();" />
        
    </j:jelly>
    ```

4.  Select **Submit**.


### Result

The custom interactive filter appears on the dashboard you added the dynamic content block to. It is also in the list of content blocks in the **Add Widgets** panel.

## Create a custom date/time filter option

When the standard selection of date/time filter options doesn't meet your needs, you can create a custom option.

### Before you begin

Follow these steps to create a custom Date/Time filter option that can then be included in any Date/Time-based interactive filter for use on a Dashboard. In this example, you create a filter option for the period of a two weeks, a fortnight.

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

2.  Open the business rule Get Date Filter Options for Date Filters.

    This rule populates the list of selectable options in forms for new or existing date type interactive filters.

3.  On the **Advanced** tab, modify the **Script** field to include the JavaScript needed to add the new option.

    Add the following line:

    ```
    answer.add('<Time_Period_Name>@javascript:<Beginning_Time_Period>@javascript:<Ending_Time_Period>', gs.getMessage('<Textual_Representation_Of_Time_Period>'));
    ```

4.  In the line you added, make the following substitutions.

<table id="choicetable_qnn_gnq_bvb"><tbody><tr><td id="d40214e450">

**&lt;Time\_Period\_Name&gt;**

</td><td>

A unique name for the time period selected. This string is used internally by the system to identify the option and is set to something that can be descriptive of the time period described.Enter the value `112_Last Fortnight`.

</td></tr><tr><td id="d40214e465">

**&lt;Beginning\_Time\_Period&gt;**

</td><td>

The specific date and time on which this filter starts. This value can use absolute or relative values. It’s much more common to use a relative value that uses the JavaScript URL syntax.Enter the value `gs.daysAgoStart(14)` to indicate that the time interval for this selection should be exactly two weeks ago.

</td></tr><tr><td id="d40214e480">

**&lt;Ending\_Time\_Period&gt;**

</td><td>

The specific date and time on which the time period for this filter option should end. This value can also use absolute or relative values. Similar to the **Beginning\_Time\_Period** this value is usually a relative time period to use the JavaScript URL syntax.Enter the value `gs.daysAgoStart(0)` to indicate that the time period ends at the current date and time.

</td></tr><tr><td id="d40214e498">

**&lt;Textual\_Representation\_Of\_Time\_Period&gt;**

</td><td>

A short text string that displays in the list of Date/Time filter options, which appear in ascending alphabetical order.Enter `Last fortnight`, to indicate that this selection specifies a time period from one fortnight before the current date and time.

</td></tr></tbody>
</table>    The complete statement now reads:

    ```
    answer.add('112_Last Fortnight@javascript:gs.daysAgoStart(14)@javascript:gs.daysAgoEnd(0)', gs.getMessage('Last fortnight'));
    ```

5.  Select **Update** to save your changes to the business rule.

6.  Check that the new option is available when you edit or create a Date/Time filter.

    1.  Navigate to **All** &gt; **Reports** &gt; **Administration** &gt; **Interactive Filters**.

    2.  Select a Date filter.

        The available filters include **Last fortnight**.

        ![Available date filter options including last fortnight](../image/available-date-time-filter-options-fortnight.png)

7.  Edit a date filter to include the new value and add the filter to a dashboard.

    ![A date filter with the last fortnight option available](../image/date-filter-new-option.png)


## Custom interactive filter example - Multiple reports

You can use a custom interactive filter to filter multiple reports using different tables. There are two different APIs to publish an interactive filter for a single table or multiple tables. This example filters a report on the incident and problem tables by assignment group using a custom interactive filter.

### About custom interactive filters on multiple tables

Keep the following in mind when you create a custom interactive filter:

-   Custom interactive filters that apply to only one table use the function DashboardMessageHandler.publishFilter\(\).
-   Custom interactive filters that apply to multiple tables use the function DashboardMessageHandler.publishMessage\(\).
-   Before you publish, an interactive filter call to the SNC.canvas.interactiveFilters.setDefaultValue\(\) function is required.
-   A call to either the SNC.canvas.interactiveFilters.removeDefaultValue\(\) or the DashboardMessageHandler.removeFilter\(\) function is required before you reset the filter.

A custom interactive filter that calls the publishFilter\(\) method multiple times refreshes the associated report the same number of times. Repeated calls to this method can cause performance issues.

### How to apply Custom Interactive Filter to multiple tables

The following example filters the report by assignment group on the Incident \[incident\] and Problem \[problem\] tables.

DashboardMessageHandler.publishMessage\(\) accepts multiple filters as an array. Construct the filter array and then create a single instance of DashboardMessageHandler which calls DashboardMessageHandler.publishMessage\(\[filters\]\). This method refreshes the widget only once.

```
<?xml version="1.0" encoding="UTF-8"?>
<j:jelly xmlns:j="jelly:core" xmlns:g="glide" xmlns:g2="null" xmlns:j2="null" trim="false">
   <script>
      var my_dashboardMessageHandler = new DashboardMessageHandler("my_unique_id");

function publishMultipleFilter() {
      <!-- Mutliple filters can be passed as an array -->
      var finalFilter = [{"table":"incident","filter":"assignment_group=6fcd3b573b331300ad3cc9bb34efc447"}, {"table":"problem","filter":"assignment_group=6fcd3b573b331300ad3cc9bb34efc447"}];
      <!-- call setDefaultValue first -->
      SNC.canvas.interactiveFilters.setDefaultValue({
id: my_dashboardMessageHandler._unique_id,
filters: finalFilter,
}, false);
      <!-- then call Publishmessage to publish filters-->
      my_dashboardMessageHandler.publishMessage(finalFilter);
}

function clearFilter() {
SNC.canvas.interactiveFilters.removeDefaultValue(my_dashboardMessageHandler._unique_id, false);
my_dashboardMessageHandler.removeFilter();
}
   </script>
   
Example of a filter that filters incident and problem table where the assignment group is Problem solving
   <input id="allTasks" type="button" value="All" onclick="clearFilter();" />
   <input id="onlyMine" type="button" value="Assignment group is [Problem solving]" onclick="publishMultipleFilter();" />
</j:jelly>
```

