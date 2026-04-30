---
title: Primary data integration
description: All primary data are synchronized based on the configurable scheduled job Fetch Spend Primary Data. For supplier primary data, if an update is made in the ERP, it is synchronized with Source-to-Pay \(S2P\) even if the scheduled job has not been triggered.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Primary data integration

All primary data are synchronized based on the configurable scheduled job Fetch Spend Primary Data. For supplier primary data, if an update is made in the ERP, it is synchronized with Source-to-Pay \(S2P\) even if the scheduled job has not been triggered.

The asset category and material group mapping tables are also populated by the same scheduled job. However, the address mapping table has to be populated manually. A procurement administrator must manually populate the S2P model categories and capitalization policy in the respective mapping tables on initial load.

