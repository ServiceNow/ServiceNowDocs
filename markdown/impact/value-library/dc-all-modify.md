---
title: Modifying the Data Collection configuration
description: You can make changes to the Data Collection configuration to align with your organization's needs.
locale: en-US
release: yokohama
product: Value Library
classification: value-library
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data Collection Toolkit, Value Management, Impact Delivery Instance \(formerly Impact Digital Experience\), Impact]
---

# Modifying the Data Collection configuration

You can make changes to the Data Collection configuration to align with your organization's needs.

When the standard definitions for the Success Metrics from ServiceNow don’t align with how your organization functions or how you use the platform, you can change the configuration of the data collection app to reflect your processes and implementation.

Alterations of a success metric data point definition require changes to one or both of the following pieces of the metric architecture within Performance or Performance/Platform Analytics:

-   Change the Indicator Source when you need a different basic data set.
-   Change the automated indicator when you need to change the filters that are applied on the basic data set for the calculation.

## Example of common modifications

Some organizations do not use the recommended Outages table within the CMDB \(and the Employee Center notification functionality that comes with it\) to capture outages.

In this case, work with the Service Owner and your Squad to define the correct way to identify or approximate what an Outage is. For example, some customers consider Priority 1 incidents to be a representation of outages.

The alterations for this change in metric definition would imply the following configuration changes:

-   A basic data set indicator source for the incident table already exists as it is leveraged by some of the other success metrics. Therefore, you don’t have to create a new indicator source.
-   The Automated Indicators configurations for the following need to be adjusted: Impact VM - Mean Time to Restore - Unplanned Outages \(hrs\) and Impact VM - \# of Unplanned Outages This Month.
    -   Change the Indicator Source field to **Impact VM - Incidents Closed This Month** on both indicators.
    -   Change the Additional Conditions to add a filter for **Priority 1** on both indicators.
    -   For Time to Restore, as the duration field may not be in use, you can use a scripted calculation for the duration. You can re-use the script from the automate indicator **Impact VM - Average Time to Close an Incident \(hrs\)** for this.

