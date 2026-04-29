---
title: Configure a group by data item
description: Configure a data item for a grouped list screen. You group items in a data item to get a count. For example, you can group a list according to priority and then on a grouped list screen see a count of how many high, medium, and low items exist.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data items, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a group by data item

Configure a data item for a grouped list screen. You group items in a data item to get a count. For example, you can group a list according to priority and then on a grouped list screen see a count of how many high, medium, and low items exist.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Data** category, and then select **New**.

4.  From the Create a data item dialog box, select the type of data item you want to create, and then select **Continue**.

    You can select either a standard **Data item** or a **Relationship data item**.

5.  Complete the following fields as needed.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the data item.|
    |Table|Table where the data item gets its data.|
    |Description|Description used to identify your data item.|
    |Condition Type|Whether the conditions for the data item are declarative, scripted, or use an encoded query. For a grouped list, select either **Declarative** or **Script**.|

6.  In the **Data** section, use the **Group By** field to select the field you want to use to group the records in your list.

7.  Select **Save**.


**Related topics**  


[Grouped list screen](../concept/grouped-list-screen.md)

[Configure a group list screen](sg-config-grouped-list.md)

