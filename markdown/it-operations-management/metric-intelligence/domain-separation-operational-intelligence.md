---
title: Domain separation and Metric Intelligence
description: Domain separation is supported in Metric Intelligence. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Metric Intelligence
classification: metric-intelligence
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Domain separation and Metric Intelligence

Domain separation is supported in Metric Intelligence. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## How domain separation works in Metric Intelligence

When domains are separated in Metric Intelligence, users can view and manage alerts and events only in their own \(tenant\) domain. After the binding process has finished, the domain of the configuration item \(CI\) is used so that users within that domain can explore metric data. A domain column is present for Metric Intelligence tables that are provided in the base system. The domain column shows the name of the domain to which the CI belongs.

**Note:** If the domain column does not appear in the list, click ![Personalize List to add a column](../image/PersonalizeIcon.png)\(Personalize List\) and add the required column. In addition, you can add a column that displays the domain path.

The following Metric Intelligence features have limited domain separation support.

<table id="table_b3x_svh_l2b"><thead><tr><th>

Feature

</th><th>

Support

</th></tr></thead><tbody><tr><td>

Metric types

</td><td>

Supported at global level.

 The instance owner can control the metric types for all domains.

</td></tr><tr><td>

Metric type registration

</td><td>

Supported at global level.

 The instance owner can control the metric type registration for all domains.

</td></tr><tr><td>

Metric class

</td><td>

Supported at global level.

 The instance owner can control the metric classes that are used for all domains.

</td></tr><tr><td>

Configuration settings rules

</td><td>

Supported at global level.

 The instance owner can control the configuration settings rules for all domains

</td></tr></tbody>
</table>**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

