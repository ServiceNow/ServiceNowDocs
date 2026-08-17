---
title: DMS integration
description: Integration with Dealer Management Systems \(DMS\) enables automatic retrieval of repair order data to streamline claim creation and processing in MCO.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-dms-integration-overview.html
release: australia
topic_type: concept
last_updated: "2026-07-13"
reading_time_minutes: 1
keywords: [DMS integration, Dealer Management System, STAR API, automotive integration, OEM integration]
breadcrumb: [Integrate, Manufacturing Commercial Operations]
---

# DMS integration

Integration with Dealer Management Systems \(DMS\) enables automatic retrieval of repair order data to streamline claim creation and processing in MCO.

Dealer Management Systems \(DMS\) are the system of record for repair orders, capturing repair details, part codes, and labor codes used to automate claim creation in MCO. The automotive industry uses the STAR \(Standards for Technology in Automotive Retail\) API standard for DMS-OEM integration, but some OEMs use non-STAR standards. MCO supports a flexible integration framework for both STAR and custom configurations, extendable to other systems used by industrial OEMs.

This integration automates claim and pre-approval creation from repair order data, reducing errors and effort in claim submission. It also updates claim status back to the DMS after assessment in MCO, so dealers can continue using the DMS as their primary interface.

Key capabilities:

-   Connects to STAR-based and custom DMS configurations across automotive and industrial OEMs.
-   Extracts repair order data, including part codes and labor codes, for claim processing.
-   Maps repair order fields to populate claim and pre-approval records automatically.
-   Synchronizes assessment outcomes back to the DMS in real time.
-   Preserves the dealer's existing DMS workflow without requiring a separate login.

**Related topics**  


[Set up inbound DMS integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-configure-dms.md)

[MCO Integration APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/manufacturing-integrate.md)

