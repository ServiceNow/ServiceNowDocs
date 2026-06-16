---
title: Vendor Risk Management integration with EcoVadis release notes
description: Version history for the Vendor Risk Management integration with EcoVadis application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-vendor-risk-mgmt-ecovadis.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# Vendor Risk Management integration with EcoVadis release notes

Version history for the Vendor Risk Management integration with EcoVadis application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.0 - June 2026 \(Australia\)**
    -   Changed:
        -   Added strict read-only enforcement to EcoVadis data fields to prevent unauthorized modifications.
        -   Implemented query ACL security controls for CVE-2025-3648 vulnerability mitigation.
-   **Version 21.1.1 - December 2025 \(Zurich\)**

    Changed: Changes have been made to enable sn\_vdr\_risk\_asmt.vendor\_risk\_admin to perform the necessary integration configurations, eliminating the need for a system administrator to do it.

-   **Version 20.1.1 - May 2025**

    Changed: Matching criteria has been updated to improve identification of a third-party from risk score providers score feed.

-   **Version 18.1.0 - June 2024**

    Fixed: Removed possible script injection vulnerability in an encoded query script.

-   **Version 15.0.3 - August 2022**

    Fixed: Added additional security checks to the EcoVadis API call

-   **Version 14.1.2 - March 2022**

    New: Added ability to request an EcoVadis rating for a vendor from within ServiceNow

-   **Version 13.0.1 - December 2021**

    The ServiceNow Vendor Risk Management application helps customers manage their third party risk management \(TPRM\) programs across a broad number of risk domains. Environmental, Social, and Goverance \(ESG\) is one of those risk domains that may necessitate the need to import information from content providers such as EcoVadis.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

