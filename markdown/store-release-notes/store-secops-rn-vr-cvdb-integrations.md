---
title: CVDB Integrations release notes
description: Version history for the ServiceNow CVDB Integrations application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-cvdb-integrations.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# CVDB Integrations release notes

Version history for the ServiceNow® CVDB Integrations application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.2.0 - June 2026**

    Changed: Renamed the plugin formerly known as "CVDB Integrations" to "Integrations for Central Vulnerability Database" to align with standard naming conventions.

-   **Version 1.0.1 - April 2026**
    -   CVDB Integrations extends the Central Vulnerability Database \(CVDB\) by connecting it to additional authoritative vulnerability intelligence sources — starting with the Japanese Vulnerability Notes \(JVN\) and the European Union Vulnerability Database \(EUVD\). Prior to these integrations, customers relying on the CVDB had visibility limited to sources already bundled with the base plugin. CVDB Integrations closes this gap by ingesting, normalizing, and deduplicating advisories from regional databases and mapping them to the CVDB data model.
    -   Each integration parses the source-specific advisory format and maps fields to the CVDB schema — including CVE IDs, affected softwares, severity scores, references, and timestamps. Advisories that carry a CVE identifier are linked to the corresponding canonical CVDB record; advisories without a CVE are persisted as non-CVE records with a unique canonical identifier \(e.g., JVN-YYYY-XXXXX, EUVD-YYYY-XXXXX\). A deduplication and canonicalization layer ensures that the same vulnerability reported by multiple sources is grouped rather than duplicated.
    -   Source attribution and field-level provenance are preserved for every ingested record. Customers can filter vulnerabilities by source in the VR UI, and the API exposes source metadata to support downstream automation. Monitoring and alerting support is included to surface ingestion failures and track daily advisory counts.

**Parent Topic:**[ServiceNow Store - Vulnerability Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

