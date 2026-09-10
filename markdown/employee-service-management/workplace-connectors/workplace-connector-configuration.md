---
title: Configure connectors for badging data
description: Configure the connector configuration table \[sn\_wsd\_wc\_connector\_config\] to fetch the badging spoke data records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/workplace-connectors/workplace-connector-configuration.html
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

    \[Omitted image "wsd-app-scope-connectors.png"\] Alt text: Application Global Scope selected as Workplace Connectors.

3.  Select **New**.

4.  In the **Target table** field, select the target table for the badging spoke data.

    In this case, it’s the Employee Attendance Data table. For more information, see [Attendance Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/attendance-analytics.md).

5.  In the **Type** field, select the type of data the connector processes from the drop-down list.

    For example, badging data or occupancy data.

6.  In the **Extension Point Definition** field, select the lookup list icon \(\[Omitted image "search-icon.png"\] Alt text: Lookup list icon.\) and select the **BadgingDataHandler** as the extension point for integration.

    **Note:** The extension point is used to process badging data from the provider and convert it to the standard format to be implemented by each provider. It's just an interface. Each provider must have a separate implementation.

    For more information, see .

7.  Select **Submit** to save the connector configuration.


**Parent Topic:**[Setup Workplace Connectors for badging data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/setup-workplace-connectors.md)

**Previous topic:**[Create a badging data provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/wsd-connector-badging-providers.md)

**Next topic:**[Provider connector configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-connectors/provider-configuration-ovw.md)

