---
title: Dispute Content Pack for US Regulations release notes
description: Version history for the Dispute Content Pack for US Regulations application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-dispute-content-pack-us-regulations.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Dispute Content Pack for US Regulations release notes

Version history for the Dispute Content Pack for US Regulations application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.2.0 - March 2026**
    -   New:
        -   Added validation checks to Reg Z resolution limit SLA to prevent triggering when required billing data \(billing\_cycle\_days or statement\_generation\_date\) is missing.
        -   Added "Reg Z limit" duration script using billing\_cycle\_days and statement\_generation\_date from sold product.
        -   Added new fields "Dispute reported date" and flag "Acknowledge sent" to the Card disputes transactions table.
    -   Changed:
        -   Updated Reg Z Resolution and Acknowledgement SLAs to start from dispute\_reported\_date with custom duration calculation.
        -   Updated the acknowledgement duration for Regulation Z \(Reg Z\) SLA to 30 days to align with regulatory compliance requirements.
        -   Updated following Reg E SLAs to start from "Dispute reported date" field:
            -   Reg E 90day resolution limit
            -   Reg E acknowledgement
            -   Reg E 45day resolution
        -   Updated following Reg E SLAs duration type formula to be \(elapsedDays = gs.dateDiff\(current.card\_dispute\_transaction.dispute\_reported\_date, current.sys\_created\_on, true\)\)
            -   Reg E 20day provisional
            -   Reg E 10day provisional
            -   Reg E PC reversal
-   **Version 1.1.3 - December 2025**

    Changed: Provisional Credit SLAs Schedule Update: Reg E provisional credit SLAs are updated to calculate breach time dynamically based on the case creation date, ensuring greater accuracy in the dispute resolution process.

-   **Version 1.1.2 - October 2025**

    Fixed: REG E SLA Timing Accuracy - Fixed an issue where Regulation E SLAs were not being calculated correctly for Provisional Credit tasks. The condition was corrected to use cardDisputeTransaction.parent\_case instead of just parent\_case, ensuring proper SLA tracking. Additionally, retroactive start was enabled on the created field for card dispute transactions, ensuring accurate timing calculations.

-   **Version 1.1.0 - March 2025**

    Changed: Changed the SLA definitions to Card disputes transaction table instead of Card disputes service.

-   **Version 1.0.0 - August 2024**

    The Dispute Content Pack for US Regulations application is designed to support monitoring dispute cases effectively and take necessary actions. This application provides SLA definitions pertaining to Regulation E \(Reg E\) and Regulation Z \(Reg Z\), and track the dispute cases during life cycle


