---
title: Create a definition for your store application
description: Create a definition for your store app to define the licensing metrics you want collected.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Custom licensing for ISV applications, Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Create a definition for your store application

Create a definition for your store app to define the licensing metrics you want collected.

## Before you begin

Role required: admin or developer

## About this task

Create a definition for an application in development or for an application you have already published. However, if you assign a definition to a published application, you will have to re-publish it with the new definition. Additionally, you can only assign one definition to an application.

**Note:** You can only create a definition for capacity subscriptions. See [Types of subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=types-subscription-v2&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **My Company Applications**.

2.  Select the application.

3.  Under the **Subscription Management** section, set **Subscription Model** to **Capacity**.

4.  Select the search icon next to **License Definition**.

    The **Application License Definitions** pop-up loads.

5.  Select **New**.

6.  Fill in the **Application License Definition** record.

<table id="table_vlt_mhd_zlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the definition.

</td></tr><tr><td>

Description

</td><td>

Brief summary of the definition.

</td></tr><tr><td>

Metric Type

</td><td>

Type of collected metric.

</td></tr><tr><td>

Frequency

</td><td>

How often metrics are collected.

</td></tr><tr><td>

Performance Validated

</td><td>

Check the box if you have tested the performance of the definition.

</td></tr><tr><td>

Table

</td><td>

Table used to determine usage.**Note:** Only lists tables associated with the current application.

</td></tr><tr><td>

Query

</td><td>

Criteria to use on the table.

</td></tr><tr><td>

Aggregation

</td><td>

Type of aggregation. -   Set to Count to count all records.
-   Set to Count \(Distinct\) to count unique records only.


</td></tr><tr><td>

Aggregation Column

</td><td>

Table column used for aggregation.**Note:** Column must be indexed to be aggregated.

</td></tr><tr><td>

Group By

</td><td>

Columns in the table to group the data by. Max of 3. **Warning:** Case sensitive.

</td></tr></tbody>
</table>7.  Select **Submit**.

    Your new definition appears in the **Application License Definitions** pop-up.

8.  Select the definition to apply it to the application.


## What to do next

Create a new version of the application and publish it to the ServiceNow Store. While your application is in review, any changes to the definition may cause subsequent versions of your application to be rejected. Once the application is approved and published to the ServiceNow Store, the definition becomes read-only.

To change the definition of an application already on the ServiceNow Store, you must create a new definition, submit a new version of the application, and go through the review process.

**Parent Topic:**[Custom licensing for ISV applications](../concept/custom-licensing-isv-apps.md)

