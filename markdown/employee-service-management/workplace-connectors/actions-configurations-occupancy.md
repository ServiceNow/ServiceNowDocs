---
title: Retrieving Action Configurations data
description: Retrieve Actions from occupancy data provider using Flow Designer Integration Hub. Specify the transform definitions and invoke the Sub flow to retrieve Occupancy data. For example, Metrikus Spoke integration. The occupancy sensor data from the Occupancy data provider is transformed to derive space occupancy data in Workplace Connectors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-connectors/actions-configurations-occupancy.html
release: australia
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setup Workplace Connectors for occupancy data, Configure, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Retrieving Action Configurations data

Retrieve Actions from occupancy data provider using Flow Designer Integration Hub. Specify the transform definitions and invoke the Sub flow to retrieve Occupancy data. For example, Metrikus Spoke integration. The occupancy sensor data from the Occupancy data provider is transformed to derive space occupancy data in Workplace Connectors.

## Before you begin

**Note:** If you’re using demo data or product data \(seed data\), some fields are pre-filled. In case, if you aren’t using the base system product data, you can configure the Actions configuration data table. The seed data is available as part of the Metrikus Spoke integration.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Connectors** &gt; **Administration** &gt; **Action Configurations**.

    \[Omitted image "wsd-action-configurations.png"\] Alt text: Actions configuration table showing the Metrikus occupancy action, transform definition, and sub flow.

2.  Select **New**.

    Fill in the form fields:

<table id="table_nsh_24s_s1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider

</td><td>

Name of the provider. Select **Metrikus**. For more information, see [Configure sensor data providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-connectors/providers-occupancy.md).

</td></tr><tr><td>

Action Name

</td><td>

Actions are reusable operations to automate processes. Actions are defined in the Flow designer Metrikus spoke integration. For more information, seeSelect **Query Space Occupancy**: The script for action configurations checks the workplace space for occupancy status. For example, **Occupied**, **Unoccupied**, **Invalid**, and so on.

</td></tr><tr><td>

Transform Definition

</td><td>

Transforms the occupancy data output from the providers \(For example, Metrikus\) in Workplace ConnectorsSelect **Occupancy DataHandler**.

</td></tr><tr><td>

Connector Configuration

</td><td>

Option to select a sensor data from the connector configuration table. For example, Occupancy or Badging.Select **Occupancy**.

For more information, see [Connector Configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-connectors/connector-configuration-occupancy.md).

</td></tr><tr><td>

Invoke

</td><td>

Invokes sub flows from the Flow designer for Metrikus spoke integration. For more information, see Select **Subflow**.

</td></tr><tr><td>

Sub flow

</td><td>

Sub flows consist of properties, inputs or outputs, sequence of actions, and data collected or created. Sub flows are repeatable actions.Select **Get All occupancy by Ids**.

</td></tr></tbody>
</table>3.  Select **Submit**.

    The occupancy data from the Actions Configurations table is loaded into the final or target table [Retrieving Space Occupancy Data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-connectors/space-occupancy-data.md) table.


**Parent Topic:**[Setup Workplace Connectors for occupancy data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-connectors/setup-occupancy-connectors.md)

**Previous topic:**[Configure Provider Space Mapping for occupancy data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-connectors/provider-space-mappings-occupancy.md)

**Next topic:**[Retrieving Space Occupancy Data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-connectors/space-occupancy-data.md)

