---
title: IT Asset Management purchase order invoice processing
description: The integration of IT Asset Management \(com.snc.sn\_spend\_asset\) with Sourcing and Procurement Operation enhances exception handling for ITAM-driven purchase order invoices in Accounts Payable Operations APO \(app-spend-itam\), enhancing accurate routing and faster resolution while improving overall operational efficiency.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrating APO with other applications, Accounts Payable Operations, Finance and Supply Chain]
---

# IT Asset Management purchase order invoice processing

The integration of IT Asset Management \(com.snc.sn\_spend\_asset\) with Sourcing and Procurement Operation enhances exception handling for ITAM-driven purchase order invoices in Accounts Payable Operations APO \(app-spend-itam\), enhancing accurate routing and faster resolution while improving overall operational efficiency.

In IT Asset Management \(ITAM\), assets are created when you acknowledge the receipt of the requested items. As part of the Better Together integration, all the received asset is handled within IT Asset Management \(ITAM\).

After receiving of the goods is completed, receiving slips are generated in ITAM. You can view the created assets in the **Assets** tab of the ITAM purchase order. For more information, see [Receiving assets in IT Asset Management](../../sourcing-procurement-operations/concept/itam-spo-receiving-assets.md).

During the invoicing process, Accounts Payable Operations checks if the purchase order originates from ITAM using the reference field. It validates the received quantity against the purchase order using the receiving slips and if discrepancies are found, then insufficient goods receipt exception is triggered. APO automatically triggers an email and notifies the ITAM 'Assigned to' user mentioned in the ITAM PO about the exception. Once the exceptions are resolved, APO automatically re-validates the invoices. The invoice status changes from “Review Needed” to “Review Complete”.

The benefits of Better Together integration with ITAM are:

-   Leverage APO functionalities and process invoices faster and efficiently
-   Automated exception handling for ITAM-PO invoices becomes more accurate and timely
-   Operational efficiency and reduced manual intervention

## Plugin dependencies for the APO-ITAM better together feature

The following are the plugin dependencies that are required to use Asset Management Integration for Accounts Payable Operations:

-   Invoice Case Management \[sn\_ap\_cm\]
-   Accounts Payable Operations \[sn\_ap\_apm\]
-   Accounts Payable Invoice Processing \[sn\_pr\]
-   Accounts Payable Operations with Document Intelligence \[sn\_ap\_ic\]
-   Asset Management Integration for Sourcing and Procurement Operations plugin \[sn\_spend\_asset\]
-   Source-to-Pay Common Architecture \[sn\_shop\]
-   Source-to-Pay Integration Framework \[sn\_spend\_intg\]
-   Supplier Common Architecture \[sn\_slm\]
-   Common Service Delivery \[sn\_spend\_sdc\]
-   Source-to-Pay Workspace \[sn\_spend\_workspace\]
-   Supplier Collaboration Portal \[sn\_supplier\_sp\]
-   ERP Integration Framework \[sn\_fcms\_intg\]
-   Finance Common Architecture \[sn\_fin\]

