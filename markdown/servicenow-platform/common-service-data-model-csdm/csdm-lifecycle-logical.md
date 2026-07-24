---
title: Life cycle of intangible/logical entities
description: The intangible/logical life-cycle value pairs represent the overall life cycle of logical assets and CIs as related to their products. A logical or software asset includes items like applications, services, and licenses. The life cycle stage and life cycle stage status values of logical items are visible only in tables related to intangible/logical items in Asset Management and the CMDB.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-logical.html
release: australia
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Life cycle of intangible/logical entities

The intangible/logical life-cycle value pairs represent the overall life cycle of logical assets and CIs as related to their products. A logical or software asset includes items like applications, services, and licenses. The life cycle stage and life cycle stage status values of logical items are visible only in tables related to intangible/logical items in Asset Management and the CMDB.

## Life-cycle values for intangible/logical CIs, assets, and IBIs

For definitions of the values in the diagram, see [Definitions of life-cycle values for intangible/logical entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-df-intangible-logical.md).

\[Omitted image "csdm-lifecycle-vp-intangible-logical.png"\] Alt text: Relationships between CSDM stages and life cycle values.

**Note:** The \[life\_cycle\_control\] table uses the type of CI \(tangible/physical, document and contract, location and so on\) to determine which *life cycle stage status* values are available for each *life cycle stage*.

## Service instances use intangible/logical life cycles

Because service instances are logical in nature, they should use the Logical life-cycle value pairs. Service instances follow the same life-cycle guidance as any other logical CI.

See [Use Service instance \(Application Services\) dashboard to monitor health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/app-service-dashboard.md).

## Life cycle inheritance for Business Applications

Parent life cycle stages \(for example, Deploy or Inventory\) appear in Business Application records even though they aren’t defined directly for the class. This is expected due to aggregation-based inheritance.

Business Application records define a restricted set of life cycle stages intended to reflect application planning and usage, such as **Ideation**, **Design**, **Operational**, and **End of Life**. These life cycle definitions are configured using the life\_cycle\_control table specifically for the cmdb\_ci\_business\_application class.

However, when viewing or editing a Business Application record, additional life cycle stages such as **Deploy** and **Inventory** may also appear. These stages are not defined directly for Business Application, but are inherited from parent CI classes \(for example, cmdb\_ci\) through the aggregation-based inheritance model used by life\_cycle\_control.

In this model, life cycle definitions from the current CI class are combined with life cycle definitions from all parent classes in the CMDB class hierarchy. Child classes therefore extend parent life cycle definitions rather than overriding them.

As a result, Business Application records can display life cycle stages that are applicable to infrastructure or hardware CIs but may not be semantically meaningful for applications. This behavior is expected and working as designed.

**Note:**

The life cycle inheritance model used by life\_cycle\_control differs from the inheritance behavior of sys\_choice. While sys\_choice uses a “most specific table wins” model \(child table choices override parent table choices\), life cycle controls are aggregated across the class hierarchy. There is currently no mechanism to suppress parent life cycle stages for a child CI class.

-   **[Definitions of life-cycle values for intangible/logical entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-df-intangible-logical.md)**  
The intangible/logical life-cycle value pairs represent the overall life cycle of logical assets and CIs as related to their products. A logical or software asset includes items like applications, services, and licenses. The life cycle stage and life cycle stage status values of logical items are visible only in tables related to intangible/logical items in Asset Management and the CMDB.
-   **[Intangible/logical tables in the CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/common-service-data-model-csdm/csdm-lifecy-tables-intang-logical.md)**  
List of intangible/logical tables.

**Parent Topic:**[CSDM reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/common-service-data-model-csdm/csdm-content-frame-reference.md)

**Related topics**  


[Intangible/logical tables in the CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/common-service-data-model-csdm/csdm-lifecy-tables-intang-logical.md)

