---
title: Card data security release notes
description: Version history for the Card data security application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-card-data-security.html
release: store
topic_type: reference
last_updated: "2026-04-09"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Card data security release notes

Version history for the Card data security application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.1.1 - April 2026**
    -   Updated:
        -   Improved how card numbers are revealed in the dispute workspace to enhance privacy and security for users.
        -   Enhanced data security by adding support for verifi skyflow, helping protect sensitive information.
        -   Reduced maintenance by simplifying extraction of script includes, removing unnecessary client scripts.
-   **Version 1.1.0 - March 2026**
    -   New:
        -   Added UIB Page, page collection for the right contextual panel to display the Issue and Merchant tab in Attachments.
        -   Added the Card Disputes – Transaction Attachment page with page collection tabs.
        -   Added a card number reveal component to the Dispute Workspace.
        -   Added UX Page, UX script, Data broker to reveal the PAN.
        -   Added an Attachments component to the Issuer tab in the right contextual panel.
        -   Added Get File Metadata and Download REST messages to display content in the right contextual panel.
        -   Added Download and View Documents actions.
        -   Added a plugin dependency on com.sn\_card\_sec\_cntr for the Data Security plugin.
-   **Version 1.0.1 - August 2025**

    Card data security improves the security of disputes processing by protecting sensitive card data. It achieves this by tokenizing card details as they enter the ServiceNow network, enabling secure communication with card networks and core banking systems. Tokenization replaces sensitive card data with a non-sensitive equivalent, significantly reducing the risk of data breaches and fraud. This helps businesses adhere to industry standards like the Payment Card Industry Data Security Standard \(PCI DSS\).


**Parent Topic:**[ServiceNow Store - Financial Services release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-fso-highlight.md)

