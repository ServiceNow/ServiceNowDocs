---
title: Duplicate an ETL transform map
description: Use an existing ETL transform map if you need to create a map that is mostly similar to that existing map. Select an existing map, specify a new data source for the new duplicate map, and then change or retain other settings such as data transforms.
locale: en-US
release: zurich
product: Integration Hub ETL
classification: integration-hub-etl
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [IntegrationHub ETL, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Duplicate an ETL transform map

Use an existing ETL transform map if you need to create a map that is mostly similar to that existing map. Select an existing map, specify a new data source for the new duplicate map, and then change or retain other settings such as data transforms.

## Before you begin

The data source for the new duplicated ETL transform map must satisfy these requirements:

-   The schema of the data source must be identical to the schema of the original ETL transform map. For example, both data sources must have an identical number of columns and identical column labels.
-   The data source must preexist.
-   The data source must not be used in any other ETL transform map.

Role required: cmdb\_inst\_admin

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **IntegrationHub ETL**.

    The landing page of the IntegrationHub ETL lists all integrations that exist in the system, including integrations that were downloaded from the ServiceNow Store.

2.  Click **Duplicate** and then fill out the Duplicate ETL Transform Map form.

<table id="table_grv_tq3_slb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Duplicate from

</td><td>

The ETL transform map to duplicate from.

</td></tr><tr><td>

CMDB application

</td><td>

The CMDB application associated with the ETL transform map.

 You can select **Add new**, which adds the **CMDB Application** and the **Discovery Source** fields for the new CMDB application.

</td></tr><tr><td>

Discovery Source

</td><td>

Discovery source associated with a new CMDB Application. Appears if you set **CMDB Application** to **Add new**.

</td></tr><tr><td>

CMDB Application Name

</td><td>

Name of a new CMDB Application. Appears if you set **CMDB Application** to **Add new**.

</td></tr><tr><td>

Name

</td><td>

Name of the ETL transform map.

</td></tr><tr><td>

Data Source

</td><td>

The source feed, unique for this ETL transform map, where the raw source data is imported from.

</td></tr></tbody>
</table>3.  Click **Create Duplicate**.


## Result

Data for the new duplicated ETL transform map is imported, and the **Import Source Data and Provide Basic Details** task, is set as complete.

## What to do next

Continue with the next steps on the guided setup steps to review the imported data and complete the integration using the duplicated ETL transform map.

