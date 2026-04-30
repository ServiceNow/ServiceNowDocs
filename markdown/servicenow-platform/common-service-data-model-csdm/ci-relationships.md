---
title: CI relationships in the CSDM
description: For configuration management to be most effective, establish relationships between the objects and CIs in the conceptual CSDM.
locale: en-US
release: zurich
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CI relationships in the CSDM

For configuration management to be most effective, establish relationships between the objects and CIs in the conceptual CSDM.

## Required CSDM relationships

-   Most features and products, such as the Technology Portfolio Management risk assessment and Application Portfolio Management \(APM\), depend on the relationships.
-   The relationships commonly created as part of Service Mapping and Discovery are the standard for infrastructure CIs. If you map the elements manually, be sure to consider how Discovery would have treated them.
-   Not all objects in the CSDM conceptual model are CMDB tables, and not all the objects have relationships. You might need to create some of the following required relationships.
-   CSDM v5 implements the **Uses::Used By** relationship between Business Applications and Application Services. Earlier CSDM versions used **Consumes::Consumed By**. A Business Application, ultimately, relates to an Application Service table and not any other type of Service Instance.

    **Note:** Enterprise Architecture Workspace users should continue to use the **Consumes::Consumed by** relationship so that the TPM and TRM lifecycle timelines are displayed correctly.


![CSDM relationships.](../image/csdm-ci-relationships.png)

**Note:** Business services and technology management services connect to the spm\_service\_portfolio through the spm\_taxonomy\_node. See [Service Portfolio Management taxonomy](https://www.servicenow.com/docs/access?context=SPM2-taxonomy&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

## Resources in the ServiceNow Community

For an extended explanation of the business application reference attribute's role in managing platforms from a CSDM perspective, [see this article](https://www.servicenow.com/community/common-service-data-model-forum/mapping-business-application-to-business-application-in-csdm/m-p/337115) in the ServiceNow community.

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

**Parent Topic:**[CSDM reference](csdm-content-frame-reference.md)

**Related topics**  


[CSDM resources](../reference/csdm-resources.md)

