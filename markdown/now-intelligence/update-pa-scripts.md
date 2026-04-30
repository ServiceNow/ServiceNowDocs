---
title: Update Performance Analytics scripts
description: Platform Analytics Solutions include Performance Analytics scripts to perform calculations on records. These scripts use the time stamp fields from the indicator sources. If you change the time field stamps in an indicator source, also modify the related scripts.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Platform Analytics Solutions, Analytics solutions, Platform Analytics]
---

# Update Performance Analytics scripts

Platform Analytics Solutions include Performance Analytics scripts to perform calculations on records. These scripts use the time stamp fields from the indicator sources. If you change the time field stamps in an indicator source, also modify the related scripts.

## Before you begin

**Important:** If you did not update any indicator sources in your Platform Analytics Solutions, skip this task.

Role required: pa\_admin, admin

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Automation** &gt; **Scripts**.

2.  Click a script to open its details.

    For example, the Change.CloseTime.Hours script record contains the following script:

    ```
    var diff=function(x,y){return y.dateNumericValue() - x.dateNumericValue();};
    var hours=function(x,y){return diff(x,y)/(60*60*1000);};
    hours(current.opened_at, current.closed_at);
    ```

3.  In the Source section, click the lock icon next to the list of Fields.

    ![The Fields list in a script record, showing the lock icon](../image/update-scripts-fields-lock.png)

    The Fields selector opens.

4.  Move the desired fields into the fields that are **Selected** for the script, and remove fields that are not appropriate.

    For example, if your organization uses the **Created** time stamp field to define a new change, replace **Opened** with **Created**.

    ![Fields selector after Opened has been removed and Created has been added](../image/update-scripts-select-fields.png)

5.  In the **Script** field, replace the references to disused fields with references to the fields you just selected.

    In this example, references to the **Opened** field are replaced by references to **Created**.

    ```
    var diff=function(x,y){return y.dateNumericValue() - x.dateNumericValue();};
    var hours=function(x,y){return diff(x,y)/(60*60*1000);};
    hours(current.opened\_atcurrent.sys_created_on, current.closed_at);
    ```

6.  Click **Update** to save your changes.


**Parent Topic:**[Configure Platform Analytics Solutions](../concept/configure-nowintel-solutions.md)

**Previous topic:**[Review the indicator sources](review-indicator-sources.md)

**Next topic:**[Review the breakdown sources](review-breakdown-sources.md)

