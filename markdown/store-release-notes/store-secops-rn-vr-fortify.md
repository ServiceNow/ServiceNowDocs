---
title: Fortify Application Vulnerability Integration release notes
description: Version history for the Fortify Application Vulnerability Integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-fortify.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Fortify Application Vulnerability Integration release notes

Version history for the Fortify Application Vulnerability Integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 31.0.1 - June 2026 \(USEM\)**
    -   The following enhancements and changes support internal security directives:
        -   Query ACLs added at the table-level and field wildcard for the Fortify app-import staging table \[sn\_vul\_fortify\_app\_import\] to align with ServiceNow Platform Security guidance.
        -   Preload and customization-detection fix scripts run exactly once per upgrade.
        -   Translation packaging updated so newly activated locales automatically pick up Fortify-specific translations without requiring an instance repair.
-   **Version 2.7.1 - September 2025**
    -   Fixed:
        -   Resolved the incorrect consolidation of vulnerabilities across different application releases in the Fortify On-Demand Integration. Previously, vulnerabilities were assigned using only the application ID, ignoring the release ID, causing all versions of an application to show identical vulnerability data.
        -   The integration now correctly uses both application ID and release ID to assign vulnerabilities to their specific application versions.
        -   One-time cleanup needs to be performed for the AVITs from Fortify and re-run both the application list and vulnerability list integrations to ensure accurate version-specific vulnerability mapping.
-   **Version 2.6.0 - May 2025**

    Fixes.

-   **Version 2.5.0 - November 2024**

    Minor fixes for this release.

-   **Version 2.4.2 - August 2024**

    Changed: The \[sn\_vul\_fortify.buffer\_hours\] property has been removed from system properties and added to the Fortify Vulnerability Integration instance parameters.

-   **Version 2.3.3 - June 2024**

    New: Auto close for application vulnerable items is supported for the Fortify integrations.

-   **Version 2.3.1 - May 2024**

    Changed: View details such as total processing times, average times for pre- and post-integration run processes, and reports on the integration run records.

-   **Version 2.2.2 - February 2024**
    -   New:
        -   You can reapply your configuration item \(CI\) lookup rules to update existing CIs \(scanned applications and product models\).
        -   Manually create remediation tasks \(AVULs\) for application vulnerable items \(AVITs\) from remediation task records on the Group Configuration tab.
    -   Fixed: Buffer time is a configurable parameter with the sn\_vul\_veracode.import\_starttime\_buffer system property. The buffer, in hours, is subtracted from Start Time \(delta\_start\_time\). The scanner imports results at the new derived delta start time.
-   **Version 2.2.1 - November 2023**
    -   New:
        -   The manage exceptions in ServiceNow and manage false positives in ServiceNow options on the Fortify configuration page can help you triage your imported application vulnerabilities with ServiceNow workflows. These options are activated by default.
            -   Manage exceptions in ServiceNow triages application vulnerable items \(AVI\) with the ServiceNow Exception management workflow. AVIs transition to Open, and you request exceptions from AVI records. Deactivate the option to preserve the Source states on AVIs imported from Fortify.
            -   Manage false positives in ServiceNow triages false positives with the ServiceNow False positive workflow. AVIs transition to Open, and you request false positives from AVI records. Deactivate the option to preserve the Source states on AVIs imported from Fortify.
-   **Version 2.1.0 - August 2023 \(Vancouver\)**

    New: New: A new product model lookup rule is activated by the system property, Use Product Model \[sn\_vul.use\_product\_model\]. This rule supports CSDM.

-   **Version 2.0.2 - March 2022**

    The Vulnerability Response integration with the Fortify on Demand product imports applications and application vulnerabilities to use with Application Vulnerability Response. Application Vulnerability Response is a feature in the ServiceNow Vulnerability Response application that helps you prioritize and remediate application vulnerabilities.


**Parent Topic:**[ServiceNow Store - Vulnerability Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

