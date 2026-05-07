---
title: Properties for n8n
description: Service Graph Connector for n8n  properties control the behavior of the connector.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [n8n, Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# Properties for n8n

Service Graph Connector for n8n  properties control the behavior of the connector.

## System properties

**Note:** To open the System Properties \[sys\_properties\] table, enter sys\_properties.list  in the navigation filter.

<table id="table_ujl_vck_m3c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_n8n\_integ.list\_execution\_page\_size

</td><td>

The maximum number of items to return in each page of sn\_n8n\_integ.sgn8n\_list\_execution datastream. This is passed as a query parameter to n8n REST API via the datastream.

 **Note:** The maximum permitted size is 250 by n8n.

</td></tr><tr><td>

sn\_n8n\_integ.list\_workflow\_page\_size

</td><td>

The maximum number of items to return in each page of sn\_n8n\_integ.sgn8n\_list\_workflow datastream. This is passed as query parameter to n8n REST API via the datastream.

 **Note:** The maximum permitted size is 250 by n8n.

</td></tr></tbody>
</table>