---
title: Add a system property
description: Add or create a property to control system behavior.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-platform-administration/t\_AddAPropertyUsingSysPropsList.html
release: zurich
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Basic system configuration, Get started, Administer]
---

# Add a system property

Add or create a property to control system behavior.

Add a system property 

## Before you begin

Role required: admin

For more information on creating system properties for your own applications, take the training on the [ServiceNow® Developer Site](https://developer.servicenow.com/dev.do#!/learn/courses/tokyo/app_store_learnv2_automatingapps_tokyo_automating_application_logic/app_store_learnv2_automatingapps_tokyo_application_properties/app_store_learnv2_automatingapps_tokyo_what_are_application_properties).

## About this task

Some properties in the system aren’t visible in an instance by default and must be added to the System Property \[sys\_properties\] table. If a feature requires the addition of the property, you can add a system property.

**Important:** System properties store configuration information that rarely or never changes. Each time you change or add a system property, the system flushes the cache to keep all nodes in the cluster in sync. This cache flush has a very high performance cost for one to 10 minutes, which can potentially cause an outage if done excessively. To prevent such outages, don’t use a system property to store configuration information that changes more than once or twice a month. Instead, use a custom table to store regularly changing configuration information.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Verify that the property doesn’t exist by searching for the property name.

3.  Select **New**.

4.  Complete the System Property form using the database name of the property.

    Make sure to specify the correct data **Type** and add the new value that you want the property to use.

    Properties that you add already contain default values. You add properties to change this value.

<table id="table_tqn_cfv_s1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the property you’re creating.

</td></tr><tr><td>

Description

</td><td>

Type a brief, descriptive phrase describing the function of the property.

</td></tr><tr><td>

Choices

</td><td>

Comma-separated values for a choice list. If you need a different choice list label and value, use an equal sign \(=\) to separate the label from the value. For example, `Blue=0000FF`, `Red=FF0000`, `Green=00FF00` displays **Blue**, **Red**, and **Green** in the list, and saves the corresponding hex value in the property value field.

</td></tr><tr><td>

Type

</td><td>

Select the appropriate data type from the list \(for example, **integer**, **string**, or **true\|false\)**.

</td></tr><tr><td>

Value

</td><td>

Set the desired value for the property. All property values are stored as strings. When retrieving properties via the gs.getProperty\(\) method, treat the results as strings. For example, a true\|false property returns 'true' or 'false' \(strings\), not the Boolean equivalent.

</td></tr><tr><td>

Ignore cache

</td><td>

The system stores system property values in server-side caches to avoid querying the database for configuration settings. When you change a system property value, the system always flushes the cache for the sys\_properties table. Use this field to determine whether to flush this property's value from all other server-side caches.

 The default cleared check box means that the system will flush all server-side caches and retrieve the current property value from the database. Leave the check box cleared when you want to ensure all caches have the current property value.

 Select the check box to ignore flushing some server-side caches, thus flushing only the cache for the sys\_properties table and preserving the prior property value in all other caches. This option avoids the performance cost of flushing all caches and retrieving new property values.

 Typically, you should only select the check box and enable ignoring the cache when you have a system property that changes more frequently than once a month, and the property value is only stored in the sys\_properties table.

</td></tr><tr><td>

Private

</td><td>

Set this property to true to exclude this property from being imported via update sets. Keeping system properties private prevents settings in one instance from overwriting values in another instance. For example, you may not want a system property in a development instance to use the same value as a production instance.

</td></tr><tr><td>

Read roles

</td><td>

Define the roles that have read access to this property.

</td></tr><tr><td>

Write roles

</td><td>

Defines the roles that have write access to this property.

</td></tr></tbody>
</table>5.  Select **Submit**.

    Depending on the property name, an administrator might be able to change its value only through a new module. It may also appear in one of the Properties pages in System Properties.

    **Note:** If the **Ignore cache** check box is selected, the system flushes the server cache when the parameter is changed.


**Parent Topic:**[Basic system configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/p_CoreConfigurationOverview.md)

