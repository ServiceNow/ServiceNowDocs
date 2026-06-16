---
title: Operational Technology Hardware Vulnerability Assessment release notes
description: Version history for the Operational Technology Hardware Vulnerability Assessment application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-manufacturing-operational-tech-hardware-vuln-assess.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Operational Technology release notes, ServiceNow Store release notes]
---

# Operational Technology Hardware Vulnerability Assessment release notes

Version history for the Operational Technology Hardware Vulnerability Assessment application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.0.0 - June 2026**

    New: Certified for Australia Patch 3

-   **Version 3.1.0 - March 2026**

    New: Certified for Australia.

-   **Version 3.0.0 - December 2025**

    Changed: Minor fixes for this release.

-   **Version 1.0.3 - August 2025**
    -   New in Zurich release
        -   The following improvements are available in Hardware Vulnerability Assessment:
            -   Assessments without Normalization: Ability to assess discovery models without content available for normalization.
            -   Confidence Scores: New scoring mechanism for all types of assessments.
            -   Version Range Support: The range information provided by NVD is used to create assessments without explicitly creating CPEs in NVD.
            -   Partial assessment for partially normalized discovery model: Creates partial assessments for discovery models without firmware version. The partial assessments are done if the other versions of the discovery model have the same publisher and model.
            -   Expiring of assessments: If you update the firmware version of a CI, the corresponding normalized discovery model also updates. The assessment records based on the older firmware version expires while new assessments are generated for new firmware version.
-   **Version 1.0.2 - March 2025**
    -   New:
        -   Use OT Hardware Vulnerability Assessment to assess the vulnerabilities for the firmware of the OT Assets
        -   Operational Technology Hardware Vulnerability Assessment provides a thorough analysis of vulnerabilities within the hardware components of your Operational Technology \(OT\) systems, such as PLCs, DCS, SCADA systems, and other critical devices. It proactively identifies vulnerability risks. By assessing these vulnerabilities, organizations can address hardware weaknesses before they impact operational efficiency, safety, and compliance.
-   **Version 1.0.1 - February 2025**

    Operational Technology Hardware Vulnerability Assessment provides a thorough analysis of vulnerabilities within the hardware components of your Operational Technology \(OT\) systems, such as PLCs, DCS, SCADA systems, and other critical devices. It proactively identifies vulnerability risks. Organizations can assess these vulnerabilities and address hardware weaknesses before operational efficiency, safety, and compliance are impacted by the vulnerabilities.


**Parent Topic:**[ServiceNow Store - Operational Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-manufacturing-highlights.md)

