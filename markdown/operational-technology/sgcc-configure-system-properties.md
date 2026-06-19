---
title: Configure system properties on SGC Central
description: In this step, review and modify the configurable system properties included with the integration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/sgcc-configure-system-properties.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-05-19"
reading_time_minutes: 1
breadcrumb: [SGC Central, Service Graph Connector for ServiceNow Operational Technology \(OT\) Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Configure system properties on SGC Central

In this step, review and modify the configurable system properties included with the integration.

## Before you begin

Role required: admin

## Procedure

1.  Next, review and modify **Configure system properties** included in the integration.

    1.  Next to the Configure system properties task, select **Configure**.

        \[Omitted image "config-system-props-all-2.png"\] Alt text: Configure system properties

    2.  The Configure System properties window opens.
    3.  Review the System properties and adjust as needed for your instance configuration.

<table id="table_fc2_xcs_m2c"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\(Optional\) Comma-separated list of OT Discovery categories to filter the Asset imports.

</td><td>

Filters the Asset import to only import assets of particular categories. For example, if you wanted to only import ICS Host and PLC category devices from the OT Discovery Console, you could set this to `PLC,IcsHost`.Default: empty

**Note:** These are categories defined on the Console side.

</td></tr><tr><td>

API Page Size

</td><td>

Maximum number of rows to be returned from a single REST call. Default: 500

</td></tr><tr><td>

API Max Timeout

</td><td>

Maximum amount of time to wait for a response when making REST calls to OT Discovery.Default: 30000

</td></tr><tr><td>

Load Raw API Data into Staging Table

</td><td>

When set to true, the raw API data for each row is included in the staging tables along with the parsed data. This is useful when trying to compare data imported data into ServiceNow vs. What is available in the OT Discovery API.

</td></tr><tr><td>

Log Levels

</td><td>

Logging level verbosity to use for the application.Default: Info

</td></tr></tbody>
</table>    4.  Select **Save** and move to the next step.

