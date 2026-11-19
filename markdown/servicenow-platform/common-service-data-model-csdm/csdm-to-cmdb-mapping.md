---
title: How CSDM concepts map to CMDB tables
description: The objects in the conceptual CSDM framework must map to the physical model objects \(CIs and CI class tables\) in the CMDB. You can navigate in the platform to see dictionary attributes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/common-service-data-model-csdm/csdm-to-cmdb-mapping.html
release: zurich
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-08-25"
reading_time_minutes: 1
breadcrumb: [Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# How CSDM concepts map to CMDB tables

The objects in the conceptual CSDM framework must map to the physical model objects \(CIs and CI class tables\) in the CMDB. You can navigate in the platform to see dictionary attributes.

\[Omitted image "csdm-data-to-table-mapping.png"\] Alt text: Conceptual-to-physical mapping CSDM to CMDB.

Business Application data belongs in the cmdb\_ci\_business\_app table, and not in the cmdb\_ci\_app table.

**Note:** Business services and technology management services connect to the spm\_service\_portfolio through the spm\_taxonomy\_node. See [Service Portfolio Management taxonomy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/SPM2-taxonomy.md).

## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

**Parent Topic:**[CSDM reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/common-service-data-model-csdm/csdm-content-frame-reference.md)

**Related topics**  


[CSDM resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/common-service-data-model-csdm/csdm-resources.md)

