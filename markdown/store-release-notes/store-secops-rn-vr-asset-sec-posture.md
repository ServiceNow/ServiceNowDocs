---
title: Asset Security Posture Management release notes
description: Version history for the Vulnerability Response Asset Security Posture Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-asset-sec-posture.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Asset Security Posture Management release notes

Version history for the Vulnerability Response Asset Security Posture Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 5.5.2 - June 2026**
    -   The following enhancements and changes support internal security directives. These changes are applied automatically upon upgrade and your customizations on impacted Access Control Lists \(ACLs\) are preserved:
        -   Updated query ACLs for the Asset Security Posture Management \(CAASM\) tables to align with ServiceNow Platform Security guidance.
        -   Renamed the read-only fix script to a per-plugin name to prevent update set conflicts with other Security Operations plugins.
-   **Version 5.5.1 - December 2025**

    New: The Service Graph Connector for XM Cyber \(XM Cyber SGC\) is supported in Security Posture Control.

-   **Version 5.3.5 - August 2025**

    Fixed: Asset profile-based filtering in custom insights.

-   **Version 5.3.4 - May 2025**
    -   New:
        -   Supporting changes for Amazon Web Services \(AWS\) Web Application Firewall \(WAF\) as a mitigation controls source.
        -   Supporting changes for the asset profiles feature introduced for SPC policies.
-   **Version 5.3.2 - February 2025**
    -   Fixed:
        -   Retired assets are filtered out from key insights.
        -   The logic for use cases on the Connectors and Dashboard pages.
        -   Conditions for policies that are included with the application.
-   **Version 5.1.2 - December 2024**

    Fixed: The "With IRM Exception" connection in policy builder now renders the properties properly.

-   **Version 4.0.0 - August 2024**

    New: Added Groups to custom insights that organize your reports on the Configured insights dashboard.

-   **Version 3.0.3 - June 2024**

    Fixed: The 'with-connector-data' connection filters for the applicable classes.The class filter evaluates base and child policy conditions for the list of supported classes.

-   **Version 3.0.2 - May 2024**
    -   New:
        -   Improvements to the policy builder:
            -   Select the Reported only by Connection to monitor assets that are reported from a few specific asset sources but not by any other sources.
            -   Select the First seen timestamp with the With CMDB Metadata Connection to look for assets that were first discovered within a given timeframe.
            -   Select Model name to query devices for specific model information to help you with security control coverage.
            -   Select 'Within the last n days' and type in a number of days up to 30. For example, you can monitor assets with last logon data from Active Directory in last 3 days.
-   **Version 2.0.2 - March 2024**
    -   Fixed:
        -   Updates to support the base policies for the Service Graph Connector for Tenable.
        -   Minor issues with dashboard widgets and drill-down logic on the Home page in the Security Posture Control Workspace.
        -   Staging table entries are created for policies that don't perform a CMDB query as expected.
-   **Version 2.0.0 - February 2024**
    -   New:
        -   Activate policies included with the application and start auditing your assets with key use cases.
        -   View your asset inventory for the enterprise on the Home page in the workspace.
        -   Use your own policies or the policies included with the application to create custom insights.
        -   Use the supported custom insight widgets to create the following types of visualizations on the Custom insights dashboard:
            -   Comparison charts.
            -   Policy Match counts.
            -   Policy match percentages.
            -   Policy match trends.
-   **Version 1.0.1 - August 2023 \(Vancouver\)**

    Initial release: This plugin provides you with an inventory of your enterprise assets and identifies their security tool coverage gaps. Assets identified as missing endpoint protection agents, for example, are associated with vulnerability data from third-party vulnerability assessment tools to give you visibility into combinations of the high-risk security lapses on your enterprise assets.


**Parent Topic:**[ServiceNow Store - Vulnerability Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

