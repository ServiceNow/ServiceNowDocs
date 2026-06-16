---
title: Vulnerability Response Integration with Black Duck release notes
description: Version history for the Vulnerability Response Integration with Black Duck application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-int-blackduck.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Vulnerability Response Integration with Black Duck release notes

Version history for the Vulnerability Response Integration with Black Duck application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.2.1 - June 2026 \(USEM\)**
    -   The following enhancements and changes support internal security directives:
        -   Query ACLs added to Black Duck configuration and project tables: sn\_vul\_blackduck\_config and sn\_vul\_blackduck\_project, plus narrow field-specific ACLs for u\_source on the Black Duck app-import and project-import staging tables to align with ServiceNow Platform Security guidance.
        -   Fix scripts run exactly once per upgrade.
        -   Fix script renamed to a per-plugin name to prevent update set conflicts with other Security Operations plugins.
    -   Fixed: CVDB framework alignment — Four missing columns added to sn\_vul\_blackduck\_cvd\_attributes: short\_description, source\_risk\_score, v3\_impact\_subscore, status\_updated\_on so the CVD attributes table fully matches what the Black Duck integration produces. The UI list and form sections now expose these values.
-   **Version 30.1.1 - April 2026 \(USEM\)**
    -   New: Enhancements to Black Duck AVIT mapping to include componentVersionName.
    -   Fixed:
        -   Black Duck integration configuration so it correctly stores the MID Server name instead of the internal sys\_id when saving credentials. This enhancement resolves ECC queue entries that are stuck in the "Ready" state with the error message,"No response for ECC message request after waiting for 30 seconds in ECC Queue."
        -   Integration now gracefully handles deleted or archived projects. Integration runs continue processing remaining projects even when individual projects return 404 errors. Activate the sn\_vul\_blackduck.mark\_unseen\_projects\_inactive property to automatically deactivate projects no longer present in Black Duck.
-   **Version 1.1.2 - April 2026**
    -   New: Enhancements to Black Duck AVIT mapping to include componentVersionName.
    -   Fixed:
        -   Black Duck integration configuration so it correctly stores the MID Server name instead of the internal sys\_id when saving credentials. This enhancement resolves ECC queue entries that are stuck in the "Ready" state with the error message,"No response for ECC message request after waiting for 30 seconds in ECC Queue."
        -   Integration now gracefully handles deleted or archived projects. Integration runs continue processing remaining projects even when individual projects return 404 errors. Activate the sn\_vul\_blackduck.mark\_unseen\_projects\_inactive property to automatically deactivate projects no longer present in Black Duck.
-   **Version 1.1.1 - December 2025**

    Removed: Admin override check has been removed from the ACLs.

-   **Version 1.0.5 - May 2024**

    Integrate your Black Duck account with ServiceNow Vulnerability Response to prioritize and remediate application vulnerabilities.


