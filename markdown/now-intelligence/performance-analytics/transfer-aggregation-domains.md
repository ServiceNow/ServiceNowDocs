---
title: Transfer domain configuration with score aggregation
description: To transfer between instances a Performance Analytics domain configuration that is set to aggregate scores, transfer both the configuration and the aggregation domain.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Domain configurations, Domain separation, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Transfer domain configuration with score aggregation

To transfer between instances a Performance Analytics domain configuration that is set to aggregate scores, transfer both the configuration and the aggregation domain.

## Before you begin

Transfer the domain configuration with an update set. For more information about using update sets to transfer configurations between instances, see System update sets.

Role required: admin

## Procedure

1.  Log in as admin to the source instance from which you transferred the domain configuration.

2.  Navigate to **Data Collector** &gt; **Domain Configurations**.

3.  Open the domain configuration record that you transferred in the update set.

4.  Right-click on the header of the form and select **Show XML**.

5.  Copy the sys\_id, which is the value of the `aggregate_domain` element.

    ![The XML of the transferred domain configuration, with the sys_id highlighted.](../image/aggregate-domain-sysid.png)

6.  Navigate to **Domain Admin** &gt; **Domains**.

7.  Filter the list of domains by the sys\_id that you copied from the transferred domain configuration.

8.  Open the filtered domain and from the context menu, export the domain record to XML.

9.  Log in as admin to the target instance.

10. Navigate to **Domain Admin** &gt; **Domains**.

11. From the context menu, import the XML file of the domain record from the source instance.


## Result

You can execute data collection jobs for the transferred domain.

**Parent Topic:**[Grouping domains in Performance Analytics domain configurations](../concept/pa-domain-separation-msp.md)

