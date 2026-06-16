---
title: Microsoft Azure SQL Database spoke release notes
description: Version history for the Integration Hub Microsoft Azure SQL Database spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-azure-sql.html
release: store
topic_type: reference
last_updated: "2024-11-07"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft Azure SQL Database spoke release notes

Version history for the Integration Hub Microsoft Azure SQL Database spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.0 - November 2024**
    -   New:
        -   Microsoft Azure SQL Database Spoke now makes use of the default alias for Microsoft Resource Management Spoke \(sn\_azure\_rm\_spoke.Microsoft\_Azure\_Resource\_Management\)
        -   New Actions with latest design pattern of complex object outputs, retry policy, connection &amp; credentials, and error evaluation making use of the new connection &amp; credential alias:
            -   Database Management: Create Generic Database \(create\_generic\_database\), Create Hyperscale Database \(create\_hyperscale\_database\), Create VCore Database \(create\_vcore\_database\), Delete Database \(delete\_database\_v2\),Get Hyperscale SKU Template \(Metadata\) \(get\_hyperscale\_sku\_template\_metadata\),Get Properties Template \(Metadata\) \(get\_properties\_template\_metadata\),Get SKU Template \(Metadata\) \(get\_sku\_template\_metadata\),Look up Database \(look\_up\_database\),Look up Operational Status \(look\_up\_operational\_status\),Rename Database \(rename\_database\_v2\),Update Database \(update\_database\_v2\)
    -   Removed:
        -   Deprecated old credential alias Azure\_database \(sn\_azure\_sql\_spoke.Azure\_database\)
        -   Deprecated Actions that make use of old credential alias:
            -   Create Database: Create Database - Generic \(Deprecated\) \(create\_database\_\_generic\),Create Database - Hyperscale \(Deprecated\) \(create\_database\_\_hperscale\),Create Database - vCore \(Deprecated\) \(create\_database\_\_vcore\),Get Properties - Template \(Deprecated\) \(get\_properties\_\_template\),Get Sku - Hyperscale Template \(Deprecated\) \(get\_sku\_\_hyperscale\_template\),Get Sku - Template \(Deprecated\) \(sku\_template\_\_dynamic\)
            -   Database Management: Delete Database \(Deprecated\) \(delete\_database\),Get Database \(Deprecated\) \(get\_database\),List By Elastic Pool \(Deprecated\) \(list\_by\_elastic\_pool\),List By Server \(Deprecated\) \(list\_by\_server\), Operational Status \(Deprecated\) \(operational\_status\),Rename Database \(Deprecated\) \(rename\_database\),Update Database \(Deprecated\) \(update\_database\)
-   **Version 1.0.4 - September 2023**

    Fixed: The license requirements.

-   **Version 1.0.3 - April 2023**

    Fixed: Improve installation performance of spoke.

-   **Version 1.0.2 - July 2021**

    Patch release of the Azure DevOps Boards spoke for IntegrationHub. This version adds KMF modules for additional security of password2 fields and Rome compatibility.

-   **Version 1.0.1 - March 2020**

    Provides actions to automate Microsoft Azure SQL Database management.


**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

