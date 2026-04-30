---
title: Configure connectors for badging data
description: Configure the connector configuration table \[sn\_wsd\_wc\_connector\_config\] to fetch the badging spoke data records.
locale: en-US
release: zurich
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setup Workplace Connectors for badging data, Configure, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Configure connectors for badging data

Configure the connector configuration table \[sn\_wsd\_wc\_connector\_config\] to fetch the badging spoke data records.

## Before you begin

As a Workplace Connectors administrator, add the new connector configuration table to connect with the badging integration framework. This configuration fetches the badging data from the integration framework.

Role required: sn\_wsd\_wc.admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Connectors** &gt; **Connector Configuration**.

2.  On the pane, select the Application scope as **Workplace Connectors**.

    ![Application Global Scope selected as Workplace Connectors.](../images/wsd-app-scope-connectors.png)

3.  Select **New**.

4.  In the **Target table** field, select the target table for the badging spoke data.

    In this case, it’s the Employee Attendance Data table. For more information, see [Attendance Analytics](attendance-analytics.md).

5.  In the **Type** field, select the type of data the connector processes from the drop-down list.

    For example, badging data or occupancy data.

6.  In the **Extension Point Definition** field, select the lookup list icon \(![Lookup list icon.](../../workplace-case-mgmt/image/search-icon.png)\) and select the **BadgingDataHandler** as the extension point for integration.

    **Note:** The extension point is used to process badging data from the provider and convert it to the standard format to be implemented by each provider. It's just an interface. Each provider must have a separate implementation.

    For more information, see [Creating and adding a scripted extension point](https://www.servicenow.com/docs/access?context=impl-scripted-ext-pts-base-code&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

7.  Select **Submit** to save the connector configuration.


**Parent Topic:**[Setup Workplace Connectors for badging data](../concept/setup-workplace-connectors.md)

**Previous topic:**[Create a badging data provider](wsd-connector-badging-providers.md)

**Next topic:**[Provider connector configuration](../concept/provider-configuration-ovw.md)

