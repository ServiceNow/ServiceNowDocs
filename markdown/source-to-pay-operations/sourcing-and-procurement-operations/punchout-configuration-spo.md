---
title: Punchout configuration in SPO
description: Punchout configuration enables third-party suppliers to integrate their catalogs with SPO.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/punchout-configuration-spo.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Understanding punchout, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Punchout configuration in SPO

Punchout configuration enables third-party suppliers to integrate their catalogs with SPO.

The following configuration is required in SPO to enable punchout:

-   Enable suppliers for punchout: Confirm that suppliers are enabled for punchout. For each punchout supplier, a supplier record must be created, and select the **PunchOut** check box.
-   Configure the Third Party Registration \[sn\_spend\_intg\_third\_party\_registration\] table: Depending on the type of integration, configure one of the following configuration options:

    -   cXML PunchOut: If the record is marked for cXML PunchOut support, the cXML PunchOut Setup related list provides options for configuring various connection details.
    -   API Exchange: If the record is marked for API Exchange, the API Configuration related list provides options for setting up API-based integration with punchout systems.
    -   SpendInt API: If the record is marked for SpendInt API, configuration options for data load are available. This supports pre-punchout configuration for integrations.

For more information, see [Configure punchout for third-party site purchases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/configure-supplier-punchout.md).

**Parent Topic:**[Understanding punchout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/punchout-overview.md)

