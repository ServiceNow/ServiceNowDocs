---
title: Punchout configuration in SPO
description: You must configure punchout for third-party suppliers.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Understanding Punchout, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Punchout configuration in SPO

You must configure punchout for third-party suppliers.

The following configuration is required in SPO to enable punchout:

-   Enable suppliers for PunchOut: Ensure that suppliers are enabled for PunchOut. For each punchout supplier, a supplier record must be created, and the PunchOut checkbox should be selected.
-   Configure the Third Party Registration table \(sn\_spend\_intg\_third\_party\_registration\): Depending on the type of integration, configure one the following configuration options:

    -   cXML PunchOut: If the record is marked for cXML PunchOut support, the cXML PunchOut Setup related list allows you to configure various connection details.
    -   API Exchange: If the record is marked for API Exchange, the API Configuration related list provides options for setting up API-based integration with PunchOut systems.
    -   SpendInt API: If the record is marked for SpendInt API, configuration options for data load are available. This supports pre-PunchOut configuration for integrations.

For more information, see [Configure punchout for third-party site purchases](../task/configure-supplier-punchout.md).

**Parent Topic:**[Understanding Punchout](punchout-overview.md)

