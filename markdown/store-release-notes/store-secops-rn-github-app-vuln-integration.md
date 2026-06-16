---
title: Github Application Vulnerability Integration release notes
description: Version history for the Github Application Vulnerability Integration application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-github-app-vuln-integration.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Github Application Vulnerability Integration release notes

Version history for the Github Application Vulnerability Integration application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.2.1 - June 2026\(USEM\)**
    -   The following enhancements and changes support internal security directives:
        -   Query ACLs added to table-level and field wildcards across all seven GitHub plugin tables: sn\_vul\_github\_config, code\_scanning\_import, secret\_scanning\_import, secret\_scanning\_locations\_import, dependabot\_import, repos\_import, orgs\_import to align with ServiceNow Platform Security guidance.
    -   Fixed:
        -   GHSA / CVE prefix normalization — The GitHub code-scanning and secret-scanning processors previously prepended GHSA- to all rule IDs, producing malformed sn\_vul\_app\_vul\_entry records \(for example, GHSA-GHSA-\* and GHSA-CVE-\*\). The processors now classify each rule ID and route accordingly: CVE-\* rule IDs are used as-is and route to sn\_vul\_nvd\_entry; GHSA-\* advisory IDs receive a single GH- prefix; other CodeQL rule IDs receive a GH-GHSA- prefix; already GH-prefixed IDs are not re-prefixed. A scheduled cleanup job remediates existing malformed records on customer instances and self-deactivates once finished.
        -   Dependabot duplicate-advisory handling — A GH- prefix is added to GitHub-sourced advisories in sn\_vul\_app\_vul\_entry so Dependabot alerts whose GHSA advisory IDs collide with other sources no longer fail to create AVITs. Existing records are updated automatically.
        -   Generic-secret migration job stability — The "Mark scantype to generic secret" scheduled job no longer loops on constraint violations and reliably deactivates when no more migration work remains.
-   **Version 2.4.2 - June 2026**
    -   The following enhancements and changes support internal security directives:
        -   Query ACLs added for table-level and field wildcard across all seven GitHub plugin tables: sn\_vul\_github\_config, code\_scanning\_import, secret\_scanning\_import, secret\_scanning\_locations\_import, dependabot\_import, repos\_import, orgs\_import to align with ServiceNow Platform Security guidance.
    -   Fixed:
        -   GHSA / CVE prefix normalization — The GitHub code-scanning and secret-scanning processors previously prepended GHSA- to all rule IDs, producing malformed sn\_vul\_app\_vul\_entry records, for example, GHSA-GHSA-\* and GHSA-CVE-\*. The processors now classify each rule ID and route accordingly: CVE-\* rule IDs are used as-is and route to sn\_vul\_nvd\_entry; GHSA-\* advisory IDs receive a single GH- prefix. Other CodeQL rule IDs receive a GH-GHSA- prefix; already GH-prefixed IDs are not re-prefixed. A scheduled cleanup job remediates existing malformed records on customer instances and self-deactivates once finished.
        -   Dependabot duplicate-advisory handling — A GH- prefix is added to GitHub-sourced advisories in sn\_vul\_app\_vul\_entry so Dependabot alerts whose GHSA advisory IDs collide with other sources no longer fail to create AVITs. Existing records are updated automatically.
        -   Generic-secret migration job stability — The "Mark scantype to generic secret" scheduled job no longer loops on constraint violations and reliably deactivates when no more migration work remains.
-   **Version 30.2.0 - April 2026 \(USEM\)**

    Fixed: Updated GitHub integration configuration ACL to allow users with sn\_vul\_github.configure\_integrationrole to create records in sn\_vul\_github\_configtable. This role replaces the nobodyrole, which was overly restrictive.

-   **Version 2.4.1 - April 2026**

    Fixed: Updated GitHub integration configuration ACL to allow users with the sn\_vul\_github.configure\_integrationrole to create records in the sn\_vul\_github\_configtable. This role replaces the nobodyrole which was overly restrictive.

-   **Version 2.3.1 - December 2025**

    Removed: Admin override check has been removed from the ACLs.

-   **Version 2.3.0 - August 2025**

    Fixed: Addressed an issue where the GitHub Repositories Integration was encountering 404 errors when attempting to retrieve custom property values for discovered applications, despite initially receiving successful 200 responses.

-   **Version 2.2.0 - June 2025**

    Fixed: Resolved a gap where AVITs were not created if the CVE was absent in the response. The system is now made to fall back to using the GHSA ID to create a third-party entry with associated CWEs, ensuring that all findings are processed and AVITs are created without omissions. An issue was addressed where some updates were missing when deltas were pulled from GitHub Dependabot Alerts. A conditional query parameter was introduced using the sort field to ensure complete and consistent data retrieval.

-   **Version 2.1.0 - May 2025**

    Fixed: Ability to create separate AVITs for vulnerabilities within the same package but different paths in Dependabot alerts by enhancing the uniqueness of source\_avit\_id. This fixes the issue of collapsing multiple occurrences into a single AVIT.

-   **Version 2.0.1 - March 2025**
    -   New: We have introduced a new integration 'GitHub Organizations Integration" which can fetch the Organization's data created within an enterprise GitHub account, when an enterprise API is selected on the configuration screen
    -   Fixed:
        -   Enterprise API Configuration is now enabled.
        -   OAuth authentication issues have been fixed.
        -   Pagination issues have been resolved with Dependabot integration.
-   **Version 2.0.0 - February 2025**
    -   Fixed:
        -   Issue resulting in the 422 Error response from the GitHub API for the Secret Scanning Integration.
        -   Uniform repository naming convention across GitHub integrations.
        -   'Topics' attribute from the API response payload to the GitHub data model to accommodate longer strings and prevent truncation.
        -   False error message, '\[operation\] has been refused due to table's cross-scope access policy' displayed on the configuration page.
        -   'Last found' and 'First found' values to accurately reflect these dates on the Secret Scanning Integration.
-   **Version 1.2.2 - August 2024**
    -   New:
        -   Two GitHub Secret Scanning Integrations import vulnerabilities that result from potentially exploitable Client Secrets as well as their locations.
            -   GitHub Secret Scanning Integration - This integration imports the vulnerabilities for the potentially exploitable Client Secrets.
            -   GitHub Secret Scanning Location Integration - This integration provides the locations of the Client Secrets in the system.
-   **Version 1.1.3 - May 2024**
    -   New:
        -   Import your application data with the GitHub Repos Integration
        -   The GitHub Repos Integration imports application information from your GitHub repositories and stores it in the Discovered Applications table. The GitHub CodeScan and Dependabot integrations require the current application data that is imported by the GitHub Repos Integration.
        -   Improvements to the setup for the Authentication Type \(OAuth\) credentials on the GitHub Configuration page.
-   **Version 1.0.4 - February 2024**
    -   New:
        -   You can reapply your configuration item \(CI\) lookup rules to update existing CIs \(scanned applications and product models\).
        -   Manually create remediation tasks \(AVULs\) for application vulnerable items \(AVITs\) from remediation task records on the Group Configuration tab.
-   **Version 1.0.2 - November 2023**

    Integrate your Veracode deployment with ServiceNow Vulnerability Response to prioritize and remediate application vulnerabilities.


**Parent Topic:**[ServiceNow Store - Vulnerability Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

