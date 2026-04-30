---
title: SCCM server Discovery for client software distribution
description: Discovery flow populates ServiceNow tables with collection, application, and deployment data retrieved from SCCM servers.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Retrieve SCCM data for client software distribution, Configuring SCCM, CSD from SCCM, Client Software Distribution, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# SCCM server Discovery for client software distribution

Discovery flow populates ServiceNow tables with collection, application, and deployment data retrieved from SCCM servers.

Users run the **Discover SCCM** flow from an [SCCM Server Instance](../tasks/retrieve-sccm-data-ihub.md) record to populate the following ServiceNow tables:

<table id="table_lxp_vcp_ks"><thead><tr><th>

Table

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

SCCM Application \[sn\_client\_sf\_dist\_sccm\_application\]

</td><td>

-   name
-   publisher
-   version
-   model
-   sccm\_server

</td></tr><tr><td>

SCCM Collection \[sn\_client\_sf\_dist\_sccm\_collection\]

</td><td>

-   name
-   type
-   sccm\_server

</td></tr><tr><td>

SCCM Deployment \[sn\_client\_sf\_dist\_sccm\_deployment\]

</td><td>

-   application
-   collection
-   type

</td></tr></tbody>
</table>**Note:** For details about the actions used in this flow to extract data from an SCCM server, see [Microsoft SCCM spoke](../concept/microsoft-sccm-spoke.md) .

**Parent Topic:**[Retrieve SCCM data for client software distribution](../tasks/retrieve-sccm-data-ihub.md)

