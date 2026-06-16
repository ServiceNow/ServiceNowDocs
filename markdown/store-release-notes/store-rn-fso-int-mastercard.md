---
title: Financial Services Operations Integration with Mastercard release notes
description: Version history for the Financial Services Operations Integration with Mastercard application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-int-mastercard.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Financial Services Operations Integration with Mastercard release notes

Version history for the Financial Services Operations Integration with Mastercard application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.2.0 - May 2026**
    -   Changed:
        -   Updated Mastercard transaction lookup flows to not overwrite authorization date and time fields from Mastercard API response, allowing these fields to retain their original values from the transaction data
        -   Enhanced Mastercard integration flows to support new fields introduced in recent Mastercard API updates
-   **Version 2.0.1 - May 2026 \(Zurich\)**
    -   Changed:
        -   Updated Mastercard transaction lookup flows to not overwrite authorization date and time fields from Mastercard API response, allowing these fields to retain their original values from the transaction data
        -   Enhanced Mastercard integration flows to support new fields introduced in recent Mastercard API updates
-   **Version 2.1.0 - March 2026**
    -   Changed:
        -   Validate file type and size in accordance with Mastercom specifications
        -   Automatically zip attached documents prior to sending to Mastercard
-   **Version 2.0.0 - December 2025**
    -   New:
        -   Added New Subflows: Look Up Claim Details, Update Claim, Pending Queue, Load Data for Fraud and Chargeback, Look Up Authorization Details and Reverse Chargeback subflows.
        -   Created New Adapter Subflows: Multiple Mastercom adapter subflows added to enable seamless integration with Mastercard's system for automated dispute management.
        -   Enhanced Fraud and Dispute Flows: Integrated account status field from intake into the Report Fraud subflow, supporting more accurate reporting and downstream processing.
    -   Changed:
        -   Dispute Intake and Task Handling: Set dispute intake fields to read-only and updated task state mappings for improved data integrity and user experience.
        -   SLA and Event Queue Enhancements: Enhanced Mastercard dispute life cycle with new SLA definitions and event queue handling for merchant responses, ensuring timely processing and better tracking.
    -   Fixed: Fixed chargeback document execution failures when unsupported files are uploaded.
-   **Version 1.0.0 - August 2025**

    The ServiceNow Financial Services Operations Integration with Mastercard offers a streamlined and efficient solution for financial institutions to manage Mastercard disputes. By integrating with Mastercard's spoke actions, the application facilitates key dispute lifecycle events, including transaction search, chargeback creation, pre-arbitration, arbitration, and fraud reporting. This framework supports various dispute resolution use cases within ServiceNow, with out-of-the-box sub-flows for core integrations and the flexibility to extend the integration layer for custom business needs. The application's adapter layer simplifies the connection to dispute workflows, enabling effective and efficient dispute resolution.


**Parent Topic:**[ServiceNow Store - Financial Services release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-fso-highlight.md)

