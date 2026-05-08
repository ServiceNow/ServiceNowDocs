---
title: Create new indicator form
description: Create an application or capability indicator to assess applications or capabilities within the indicator framework.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Create new indicator form

Create an application or capability indicator to assess applications or capabilities within the indicator framework.

<table id="table_i2t_dx5_zbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the application or capability indicator.

</td></tr><tr><td>

Short description

</td><td>

Short summary of the application or profile indicator.

</td></tr><tr><td>

Result limit

</td><td>

The maximum number of records an indicator displays when running an associated script. This enables better performance of Enterprise Architecture by not processing too many records.

</td></tr><tr><td>

Category

</td><td>

Category that the indicator is associated with.

</td></tr><tr><td>

Direction

</td><td>

Business applications or capabilities with maximum or minimum values. -   Select **Minimize** if lower values are better.
-   Select **Maximize** if higher values are better.

</td></tr><tr><td>

Unit

</td><td>

The type of unit in which indicator scores are displayed. Units can be numbers, percentages, currencies, quantities of time, or any other entity you define.

</td></tr><tr><td>

Automatic refresh interval

</td><td>

The refresh interval to update the indicator scores within the defined time range.

</td></tr><tr><td>

Order

</td><td>

The position of the indicator in the sequential order of all other indicators while accessing an application or capability.

</td></tr></tbody>
</table><table id="table_ngx_vgy_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

Defines the location from which the indicator receives data.

 -   **Performance Analytics**: Collects scores from indicators created in Performance Analytics. See Performance Analytics indicators.
-   **Custom Script**: Allows you to write a script that collects data from another application. Beneath the **Data Source** field, a sample script appears. Customize the script as needed. An example custom script is:

    ```
var results = {};
 var applications = [];
 var incidentCount = 0;
 
 var applicationsGr = new GlideRecord("cmdb_ci_business_app");
 applicationsGr.addQuery('active', true);
 applicationsGr.query();
 //for each application get incident count at business service level
 while(applicationsGr.next()) {
    incidentCount = 0;
    
    var gr = new GlideRecord("incident");
    gr.addEncodedQuery("opened_atBETWEEN"  + startDate  + "@" +   endDate);
    gr.addQuery('cmdb_ci_business_app', applicationsGr.getUniqueValue());   
    gr.query();
    
    incidentCount = gr.getRowCount();
    var appInfo = {};
    appInfo.appId = applicationsGr.getUniqueValue();
    appInfo.weight = incidentCount;
    applications.push(appInfo);
    }
 results.applications = applications;
 results;

    ```

-   **Query Condition**: Allows you to select a table to run filters on to obtain data.
-   **Assessments**: Allows you to evaluate, score, and rank records by assessing records in a table.
-   **Indicators**: Allows you to add dependent child indicators. Through the child indicators, data is gathered to the parent indicator.

For example, if the parent indicator is number of issues, the dependent indicators can be number of incident counts, number of problems, and changes. These dependent indicators are child indicators and the number of incidents, problems, and changes recorded are consolidated up to the parent indicator as the number of issues.


</td></tr><tr><td>

Indicator

</td><td>

The **Indicator** field appears when **Performance Analytics** is selected from the **Data source** list.Indicators are statistics that are used to measure current conditions and forecast trends.

 **Note:** If the collection frequency of the application indicator isn’t greater than the frequency at which the data of the Performance Analytic indicator are generated, then the system displays an error message: `Frequency of the indicator must always be greater than or equal to the frequency of the datasource configuration indicator`.

</td></tr><tr><td>

Default breakdown

</td><td>

Name of the Performance Analytics breakdown.

</td></tr><tr><td>

Normalized script

</td><td>

A script to evaluate and score business applications and capabilities using standardized metrics. It involves using indicators that provide a normalized score for the condition they are evaluating. These indicators can be based on assessments, query conditions, custom scripts, or performance analytics.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Click through URL navigation type|Select whether to view the application or capability indicator details in a new window, in the same window, or in a dialog box.|
|Click through URL script|The script associated with an indicator that allows users to select a URL and view the indicator data in a related application or dashboard. This enables quick access to relevant information, or actions related to the indicator data.|

**Parent Topic:**[Enterprise Architecture Workspace reference](eaw-reference.md)

**Related topics**  


[Manage indicators](../../concept/eaw-concept/eaw-configure-indicators.md)

[Add or edit an application indicator](../../task/eaw-task/eaw-create-indicator.md)

[Add or edit a capability indicator](../../task/eaw-task/eaw-add-or-edit-a-capability-indicator.md)

