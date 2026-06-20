---
title: CSDM reference
description: Reference topics provide detailed descriptions of tables, properties, forms, and roles that are used in the CSDM framework.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-content-frame-reference.html
release: xanadu
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CSDM reference

Reference topics provide detailed descriptions of tables, properties, forms, and roles that are used in the CSDM framework.

## Basics

[CSDM terms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-term-definitions.md)

[CI relationships in the CSDM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/ci-relationships.md)

[How CSDM concepts map to CMDB tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-to-cmdb-mapping.md)

## Life cycles

[Document life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-document.md)

[Hardware life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-hardware.md)

[Location life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-location.md)

[Logical life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-logical.md)

[Product life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-product.md)

-   **[CSDM terms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-term-definitions.md)**  
Most ServiceNow products and ServiceNow AI Platform applications align closely with the Common Service Data Model. This table defines terms as they are used across the ServiceNow AI Platform.
-   **[CSDM life-cycle terms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-life-cyle-terms.md)**  
Most ServiceNow products and ServiceNow AI Platform applications align closely with the Common Service Data Model. This table defines terms as they are used across the ServiceNow AI Platform.
-   **[Life cycle mapping form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-life-cycle-mapping-form.md)**  
Use the Life Cycle Mapping module to specify how existing legacy status values should be converted to CSDM life-cycle value pairs \(**life cycle stage** and **life cycle stage status**\). You map both asset and CI legacy status values to life-cycle value pairs.
-   **[How CSDM concepts map to CMDB tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-to-cmdb-mapping.md)**  
The objects in the conceptual CSDM framework must map to the physical model objects \(CIs and CI class tables\) in the CMDB.
-   **[CI relationships in the CSDM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/ci-relationships.md)**  
For configuration management to be most effective, establish relationships between the objects and configuration items \(CIs\) in the conceptual CSDM.
-   **[How life-cycle values for Asset, CI, and IBI are synced](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/cmdb-asset-CI-IBI-sync-options.md)**  
Your organization gains significant value from your ServiceNow AI Platform applications when you take advantage of the option to directly map legacy status values to CSDM **life cycle stage** and **life cycle stage status** values and auto-sync the values going forward.
-   **['Foundation' stage reports on the CSDM Data Foundations dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-datafdn-dash-foundation-tab.md)**  
Foundation domain reports on the CSDM Data Foundations dashboard
-   **['Crawl' stage reports on the CSDM Data Foundations dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-datafdn-dash-crawl-tab.md)**  
Crawl stage reports on the CSDM Data Foundations dashboard
-   **['Walk' stage reports on the CSDM Data Foundations dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-datafdn-dash-walk-tab.md)**  
Walk stage reports on the CSDM Data Foundations dashboard
-   **['Run' stage reports on the CSDM Data Foundations dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-datafdn-dash-run-tab.md)**  
Run stage reports on the CSDM Data Foundations dashboard
-   **['Fly' stage reports on the CSDM Data Foundations dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-datafdn-dash-fly-tab.md)**  
Fly stage reports on the CSDM Data Foundations dashboard
-   **[Document life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-document.md)**  
The CSDM framework provides standard fields and values that you can use to track the life cycle of an asset or a CI. The document life-cycle value pairs represent the overall life cycle of document assets \(contracts\) and CIs \(business process\) as related to their products.
-   **[Hardware life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-hardware.md)**  
The CSDM framework provides standard fields and values that you can use to track the life cycle of an asset or a CI. The hardware lifecycle states represent the overall life cycle of hardware assets and CIs as related to their products.
-   **[Location life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-location.md)**  
The CSDM framework provides standard fields and values that you can use to track the life cycle of an asset or a CI. The location life-cycle value pairs represent the overall life cycle of a location within common data.
-   **[Logical life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-logical.md)**  
The CSDM framework provides standard fields and values that you can use to track the life cycle of an asset or a CI. The logical life-cycle value pairs represent the overall life cycle of logical assets and CIs as related to their products.
-   **[Product life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-lifecycle-product.md)**  
The CSDM framework provides standard fields and values that you can use to track the life cycle of an asset or a CI. The product life-cycle value pairs represent the overall life cycle of a product model, a specific version, or a product configuration.

**Parent Topic:**[Common Service Data Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/common-service-data-model-csdm/csdm-landing-page.md)

