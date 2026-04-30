---
title: Tutorial part 2: Create the application MVP in ServiceNow Studio
description: This section shows you how to create new applications and application files in ServiceNow Studio. ServiceNow Studio brings tools and builders to developers offering an effortless development experience. Create the foundations of your application in ServiceNow Studio. For this tutorial, you're going to create an app to track and manage volunteer events called We Volunteer.Create your first table in ServiceNow Studio.
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [ServiceNow Studio tutorial, Exploring ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Tutorial part 2: Create the application MVP in ServiceNow Studio

This section shows you how to create new applications and application files in ServiceNow Studio. ServiceNow Studio brings tools and builders to developers offering an effortless development experience.

**Parent Topic:**[ServiceNow Studio tutorial](lab-sns-lab-guide.md)

## Create your application in ServiceNow Studio

Create the foundations of your application in ServiceNow Studio. For this tutorial, you're going to create an app to track and manage volunteer events called **We Volunteer**.

### Before you begin

Role required: admin or Guided Application Creator \(GAC\) roles

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select **Create**

3.  Select **App**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the app. Enter `We Volunteer`.|
    |Description|Description for the app. Enter `The central hub where employees can search, register, and manage their volunteering-related events.`|

5.  Select **Continue**.

6.  Accept the default roles created in the app by selecting **Continue**.

    **Note:** The app creation may take a minute or two.

7.  Select **Go to app dashboard**.

8.  In the bottom left corner, select the Update set dialog, and select **New**.

9.  Name the update set `volunteer_mvp`.

10. Select **Save**.

11. Select **Apply**.


## Create a table using Table Builder

Create your first table in ServiceNow Studio.

### Before you begin

Role required: admin or delegated\_developer

### Procedure

1.  In the top right corner of the app dashboard, select **Create**.

2.  In the Data category, select **Table \(sys\_db\_object\)**.

3.  Select **Continue**.

4.  Select **Create a blank table**.

5.  Select **Continue**.

6.  Select **Create new table**.

7.  Select **Continue**.

8.  Specify the following settings for the table.

    -   Table label: Event
    -   Select the **Auto number** checkbox.
    -   Prefix: **EVENT**.
    -   Starting number: **1000**.
9.  Select **Continue**.

10. On the Roles page, select **All** for the admin role and **Read** for the user role.

11. Select **Continue**.

    It may take a few moments for the table to be created.

12. Select **Edit table**.

13. Use the tutorial to learn more about Table Builder.

    Other informational popups may show up. You can close these as needed.

14. Select **Add new field**.

15. On the form, fill in the fields.

    |Field|Entry|
    |-----|-----|
    |Column label|Name|
    |Type|String|
    |Max length|1000|

16. Create five more fields with the following specifications.

<table id="table_ws5_k4n_b2c"><thead><tr><th>

Column label

</th><th>

Type

</th><th>

Max length

</th></tr></thead><tbody><tr><td>

Starts

</td><td>

Date/Time

</td><td>

Not applicable

</td></tr><tr><td>

Ends

</td><td>

Date/Time

</td><td>

Not applicable

</td></tr><tr><td>

Event location

</td><td>

ReferenceTable: Location

</td><td>

Not applicable

</td></tr><tr><td>

Capacity

</td><td>

Integer

</td><td>

 

</td></tr><tr><td>

Purpose

</td><td>

String

</td><td>

1000

</td></tr></tbody>
</table>17. Select **Save**.


