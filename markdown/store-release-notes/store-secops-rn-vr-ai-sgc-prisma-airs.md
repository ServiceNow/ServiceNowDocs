---
title: AI Service Graph Connector for Prisma AIRS release notes
description: Version history for the ServiceNow AI Service Graph Connector for Prisma AIRS application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-ai-sgc-prisma-airs.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Vulnerability Response version history release notes, ServiceNow Store - Security Operations version history release notes, ServiceNow Store version history release notes]
---

# AI Service Graph Connector for Prisma AIRS release notes

Version history for the ServiceNow® AI Service Graph Connector for Prisma AIRS application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.1.1 - September 2026**
    -   New: Prisma SGC asset integration is now supported. Customers can now import and manage digital assets for all Prisma SGC asset types, with product models, digital asset records, configuration items, and relationships automatically created and mapped. All asset types are validated during import, and required field mappings are reviewed for accuracy.
    -   Changed: Metrics publishing now respects domain separation. When publishing vulnerability scan metrics, the system now creates or updates records per domain, ensuring tenant data is isolated and not overwritten across domains. The local create/update probe has been removed, and domain handling is managed automatically based on the session. Customers must configure the run-as user to ensure correct domain separation.
-   **Version 1.0.1 - June 2026**

    This integration imports AI inventory data from Palo Alto Prisma AIRS and populates ServiceNow CMDB. In addition to inventory data, this integration also imports key metrics related to AI model vulnerabilities, validation findings \(automated red teaming results\) that can be viewed in AI control tower.


**Parent Topic:**[ServiceNow Store - Vulnerability Response version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

