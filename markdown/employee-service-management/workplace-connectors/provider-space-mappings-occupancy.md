---
title: Configure Provider Space Mapping for occupancy data
description: The Provider Space Mapping data table stores the workplace locations and external Ids provided by the occupancy data provider.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-connectors/provider-space-mappings-occupancy.html
release: australia
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setup Workplace Connectors for occupancy data, Configure, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Configure Provider Space Mapping for occupancy data

The Provider Space Mapping data table stores the workplace locations and external Ids provided by the occupancy data provider.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Connectors** &gt; **Administration** &gt; **Provider Space Mapping**.

    The location data is mapped with the external Ids of the provider. For example, Metrikus occupancy data using the External Ids. The location hierarchy is shown for the spaces or locations that you selected in the [Provider Connector Configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-connectors/provider-connector-config-occupancy.md) table.

    \[Omitted image "wsd-provider-space-mappings.png"\] Alt text: Provider space Mappings table showing mapped Workplace Service Delivery spaces with external IDs provided by Metrikus occupancy sensor.

2.  To create a provider space mapping records, select **New**.

    Fill in the form fields:

<table id="table_qsm_r3s_s1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Location

</td><td>

Workplace locations mapped with Occupancy data provider. The location data shows the complete location hierarchy \(Region, site, campus, buildings, floors, and spaces\)

</td></tr><tr><td>

External id

</td><td>

Option to enter manually the external id provided by the Metrikus spoke or any other occupancy spoke data provider. Select and select a row in the External id column, enter the Metrikus Id or spoke provider Id and select the tick mark icon \(\[Omitted image "green-check-mark-icon.png"\] Alt text: check-mark-icon to save an entry\) to save it. External Ids are corresponding space Ids or location ids on the provider side. External ids from the Provider \(for example, Metrikus\) are mapped with the space records in Workplace Connectors

.The external Id data is transformed to a corresponding Workplace Connectors space Id in the Metrikus Spoke data converter extension point. The data is then mapped to a space id in Workplace Connectors.

</td></tr><tr><td>

Provider

</td><td>

Name of the Provider providing the occupancy data in Workplace Connectors. For example, Metrikus. For more information, see [Configure sensor data providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-connectors/providers-occupancy.md).

</td></tr><tr><td>

Connectors list

</td><td>

Option to show the list of all connectors or sensor data that the provider supports. Select the unlock connector list icon \(\[Omitted image "wsd-unlock-connectors-list-icon.png"\] Alt text: Select the unlock connector list icon to select a sensor or connector.\) and select **Occupancy**.

</td></tr></tbody>
</table>3.  Select **Submit**.


**Parent Topic:**[Setup Workplace Connectors for occupancy data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-connectors/setup-occupancy-connectors.md)

**Previous topic:**[Provider Space Type Mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-connectors/provider-space-type-mapping.md)

**Next topic:**[Retrieving Action Configurations data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-connectors/actions-configurations-occupancy.md)

