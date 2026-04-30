---
title: Create parent determination rules for service locations
description: Create parent determination rules that facilitate assignment of a parent to a service location.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mapping a service location to a parent location, Configuring Field Service with Service Locations, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Create parent determination rules for service locations

Create parent determination rules that facilitate assignment of a parent to a service location.

## Before you begin

The Field Service with Service Locations support plugin must be active to enable setting the parent determination rules.

Role required: wm\_admin

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Administration** &gt; **Service Location Parent Configuration**.

2.  On the Parent Determination Configuration page, click **New**.

3.  Choose the determining factor for the rule to use and provide the value.

    |Criterion|Rule action|
    |---------|-----------|
    |**Zip/Postal code**|Assigns the provided zip or postal code to a parent location.|
    |**Min Zip/Postal codeMax Zip/Postal Code.

**|Provides the minimum and maximum zip or postal code values used to assign a range to a parent location.|
    |**CityState.

**|Assigns the city and state to a parent location.|
    |**State**|Assigns the state to a parent location.|

    The **Country** and **Parent** fields are required.

    **Note:** Once you select the determining criterion, the other fields are grayed out and cannot be selected.

4.  Enter the **Country** name in the text field.

5.  In the **Parent** field, click the Lookup using list icon \( ![Lookup icon.](../image/magnifying-glass.png)\) and select the parent location from the region list.

6.  Click **Submit**.

    **Note:** If you add a rule that already exists in the wm\_location\_parent\_lookup\_rule table, an error message displays.


## Result

The parent location is configured and can be associated with a service location.

