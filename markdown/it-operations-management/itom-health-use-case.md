---
title: CMDB tables used by ITOM AIOps
description: ITOM AIOps relies on accurate data in CMDB tables to function as expected. Following CSDM guidelines when populating these tables improves the accuracy of service mapping and helps route alerts and incidents correctly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/itom-health-use-case.html
release: zurich
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [CMDB tables, CSDM v5, service mapping, CI, configuration items, service instance, Mapped Service Instance table, Configuration Item table, Dynamic CI Group table, alert routing, incident routing]
breadcrumb: [Applying the CSDM guidelines to ITOM AIOps, ITOM AIOps, IT Operations Management]
---

# CMDB tables used by ITOM AIOps

ITOM AIOps relies on accurate data in CMDB tables to function as expected. Following CSDM guidelines when populating these tables improves the accuracy of service mapping and helps route alerts and incidents correctly.

ITOM AIOps uses the following CMDB tables:

-   Mapped Application Service table `[cmdb_ci_service_discovered]`

    **Note:** With CSDM v5, the label for the table has changed from Application Service to Service Instance.

-   Configuration Item table `[ci_*]`
-   Dynamic CI Group table `[cmdb_ci_query_based_service]`

The diagram shows a conceptual map of CMDB tables and their relationships, structured according to CSDM guidelines. ITOM AIOps uses only the highlighted elements: the Service Instance table `[cmdb_ci_service_discovered]` and the Dynamic CI Group table `[cmdb_ci_query_based_service]`. The Configuration Item table `[ci_*]` is not highlighted separately, as it represents the broader CI class hierarchy that underlies most elements in the model. The remaining elements in the model support other ServiceNow products and processes, and are shown here for reference only.

\[Omitted image "itom-managed-tables-CSDM-v5.png"\] Alt text: CMDB tables used by ITOM AIOps within the CSDM v5 model.

For more information on the CSDM framework, see [Exploring the CSDM model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/csdm-content-frame-exploring.md).

