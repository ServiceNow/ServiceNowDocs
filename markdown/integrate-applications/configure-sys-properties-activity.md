---
title: Configure the system properties for an activity stream in RPA Hub
description: Configure the system properties for an activity stream of work queues, schedules, packages, process parameters, and shared parameters in RPA Hub. You can add or remove the fields that are captured in the work notes of an activity stream.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, RPA Hub, Workflow Data Fabric]
---

# Configure the system properties for an activity stream in RPA Hub

Configure the system properties for an activity stream of work queues, schedules, packages, process parameters, and shared parameters in RPA Hub. You can add or remove the fields that are captured in the work notes of an activity stream.

## Before you begin

You must do this task in the classic environment.

Role required: admin

## About this task

You can view work notes captured for few fields, that are configured by default.

## Procedure

1.  In the **All menu** filter, enter `sys_properties.LIST`.

2.  In the search bar, search for the system properties that are listed in the following table.

<table id="table_vzp_zbc_5vb"><thead><tr><th>

System Property

</th><th>

Description

</th><th>

Existing Values \(in .csv format\)

</th><th>

Fields \(as displayed on their respective forms\)

</th></tr></thead><tbody><tr><td>

sn\_rpa\_fdn.work\_queue\_work\_note\_fields

</td><td>

List of work queue fields that are captured in the work notes.

</td><td>

name,is\_queue\_item\_name\_unique,max\_attempts,purge\_status,purge\_days

</td><td>

-   Name
-   Is Queue Item Name Unique
-   Maximum Attempts
-   Purge Status
-   Purge After \(days\)


</td></tr><tr><td>

sn\_rpa\_fdn.process\_schedule\_work\_note\_fields

</td><td>

List of process schedule fields that are captured in the work notes.

</td><td>

name,start\_date,end\_date,active,start\_time,workstation\_timezone,timezone

</td><td>

-   Name
-   Start Date
-   End Date
-   Active
-   Start Time
-   Workstation Timezone
-   Timezone


</td></tr><tr><td>

sn\_rpa\_fdn.package\_work\_note\_fields

</td><td>

List of package fields that are captured in the work notes.

</td><td>

name

</td><td>

Name

</td></tr><tr><td>

sn\_rpa\_fdn.process\_parameter\_work\_note\_fields

</td><td>

List of process parameters fields that are captured in the work notes for the shared parameters and process parameters.

</td><td>

name,value,is\_sensitive

</td><td>

-   Name
-   Value
-   Sensitive


</td></tr></tbody>
</table>3.  Select the system property that you want to modify.

4.  On the System Property form, add or remove the values in the **Value** field.

    For example, to display the changes for the **Interval Type** field on the Schedule form, open the **sn\_rpa\_fdn.process\_schedule\_work\_note\_fields** system property, and then add the `interval_type` value in the **Value** field.

    Ensure that the values are added in the CSV \(Comma-Separated Values\) format in the **Value** field.

5.  Select **Update**.


**Related topics**  


[Robots in RPA Hub](../concept/robots-rpa-hub.md)

[Configuring a bot process record in RPA Hub](../concept/create-botprocess.md)

