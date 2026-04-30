---
title: Configure a parent mapping for a request
description: You can configure a mapping that specifies the association between the parent record and the request record.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service Catalog request fulfillment, Configuring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure a parent mapping for a request

You can configure a mapping that specifies the association between the parent record and the request record.

## Before you begin

Role required: admin or catalog\_admin

## Procedure

1.  Navigate to **All** &gt; **Catalog Administration** &gt; **Request Parent Mapping**.

    **Note:** The Incident request configuration that creates a mapping between the incident table and the request table is available by default.

2.  Click **New** and specify the field information.

<table id="table_xmq_tn2_zdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the mapping configuration for a request.

</td></tr><tr><td>

Parent table

</td><td>

Table from which the request is created.

</td></tr><tr><td>

Request Parent

</td><td>

Request table field that specifies the association with the parent table.

</td></tr><tr><td>

Parent requestor

</td><td>

User reference field on the parent table that is specified as the requestor of the request.**Note:** For delegated request experience, the user from the parent table record is populated in the Requested For variable. For information on delegated request experience, see [Delegated request experience](../concept/delegated-request-exp.md).

</td></tr></tbody>
</table>3.  Click **Submit**.


**Parent Topic:**[Service Catalog request fulfillment](../concept/request-fulfillment.md)

