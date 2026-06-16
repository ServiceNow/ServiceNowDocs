---
title: Vulnerability Response Integration with Palo Alto Networks Prisma Cloud Compute release notes
description: Version history for the Vulnerability Response Integration with Palo Alto Networks Prisma Cloud Compute application on the ServiceNow Store .
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-palo-alto.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Vulnerability Response Integration with Palo Alto Networks Prisma Cloud Compute release notes

Version history for the Vulnerability Response Integration with Palo Alto Networks Prisma Cloud Compute application on the ServiceNow Store .

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.3.1 - June 2026 \(USEM\)**

    Changed: Updated Access Control Lists \(ACLs\) for the Palo Alto Networks Prisma Cloud Compute integration for queries on the app-vul-prisma repository to support internal security directives.

-   **Version 3.7.0 - June 2026**

    Changed: Updated Access Control Lists \(ACLs\) for the Palo Alto Networks Prisma Cloud Compute integration for queries on the app-vul-prisma repository to support internal security directives.

-   **Version 30.2.2 - April 2026 \(USEM\)**
    -   Fixed:
        -   The Image Clusters field on Container Vulnerable Items is now correctly populated from the Prisma Cloud Compute integration. The root cause was an empty data\_source field in the Configure Image Vulnerability Keys \(VI Granularity\) record, which prevented the cluster data from being synced.
        -   Prisma Cloud Compute integrations no longer log an erroneous "Loading import set table with error" message on import set runs. The Prisma API returns a final empty payload \(\{"results":null\}\) to signal completion. This payload no longer returns an error.
        -   Upgrading the Prisma Cloud Compute integration no longer overwrites customer-configured VI Granularity \(Configure Image Vulnerability Keys\) settings. Previously, upgrading from v3.2.x to v3.3.x reset the Cluster and Namespace options to their default settings and discarded any customizations.
        -   Container Vulnerable Items \(CVITs\) that were correctly auto-closed due to a namespace no longer reporting are no longer incorrectly reopened during subsequent integration runs. The post-integration job now considers namespace-level granularity when determining which CVITs to reopen.
-   **Version 3.6.2 - April 2026**
    -   Fixed:
        -   The Image Clusters field on Container Vulnerable Items is now correctly populated from the Prisma Cloud Compute integration. The root cause was an empty data\_source field in the Configure Image Vulnerability Keys \(VI Granularity\) record, which prevented the cluster data from being synced.
        -   Prisma Cloud Compute integrations no longer log an erroneous "Loading import set table with error" message on import set runs. The Prisma API returns a final empty payload \(\{"results":null\}\) to signal completion. This payload no longer returns an error.
        -   Upgrading the Prisma Cloud Compute integration no longer overwrites customer-configured VI Granularity \(Configure Image Vulnerability Keys\) settings. Previously, upgrading from v3.2.x to v3.3.x reset the Cluster and Namespace options to their default settings and discarded any customizations.
        -   Container Vulnerable Items \(CVITs\) that were correctly auto-closed due to a namespace no longer reporting are no longer incorrectly reopened during subsequent integration runs. The post-integration job now considers namespace-level granularity when determining which CVITs to reopen.
-   **Version 3.5.0 - December 2025**

    Fixed: Minor fixes for this release.

-   **Version 3.3.3 - August 2025**

    Changed: Deprecated the Prisma Projects \[sn\_sec\_cmn\_projects\] table in the Prisma Cloud Compute application scope and moved it to the security support common scope to support imported Projects for all container integrations.

-   **Version 3.2.2 - May 2025**
    -   Changed: A new column, Source severity, has been added to sn\_vul\_container\_image\_findings, which includes the severity level provided by the scanner.
    -   Fixed: Prisma container counts integration is made active OOTB.Remediation Owner should not be able to reassign CVITs from list view.
-   **Version 3.1.4 - March 2025**

    Fixed: As issue with validating the mapping between clusters and namespaces, when the granularity option is set to "cluster" and "namespace" in ServiceNow, CVITs are created based on the combination of the lists for namespaces and clusters. We are introducing a solution that uses the "host" field to accurately determine the cluster-to-namespace mappings, ensuring proper functionality for different CVIT granularity combinations.

-   **Version 3.0.4 - January 2025**

    Fixed: Now, the 'First Found' field is populated for the Vulnerable Items and Detections from the Prisma Host scanners.

-   **Version 3.0.3 - November 2024**
    -   New:
        -   Prisma Cloud Compute Host Integration can now scan vulnerabilities on the running hosts. The Prisma Host APIs enable retrieval of comprehensive vulnerability information for a specific host and enable assignment and remediation workflows.
        -   Prisma Cloud Compute Registry Integration integrating with Palo Alto Prisma Registry scanning API will import vulnerabilities with comprehensive vulnerability information on the docker images in registry and enable assignment and remediation workflowsWith the integration of registry scanning, we are introducing an additional metering component.
-   **Version 2.8.2 - September 2024**

    Changed: When you add path as granularity for findings in the integration instance parameter, the system includes path as one of the unique keys while creating the findings.

-   **Version 2.8.0 - August 2024**

    Fixed: If projects are not configured in Prisma console and you select the Use projects flag on the Prisma configuration page, then an error message will be displayed.

-   **Version 2.7.10 - May 2024**

    Fixed: Localization issues have been fixed.

-   **Version 2.7.4 - February 2024**
    -   Fixed:
        -   ID request parameter is used instead of name in the registry API request.
        -   Added null checks in PrismaVulnerabilitiesProcessor script include while processing findings.
-   **Version 2.7.3 - November 2023**

    Minor fixes for this release.

-   **Version 2.7.2 - August 2023 \(Vancouver\)**

    New:

    -   The Prisma Cloud Compute integration run status dashboard is now available in the Next Experience UI.
    -   The Vulnerability Response Integration with the Prisma Cloud Compute application adds or updates the exploit and remediation\_notes information on the Common Vulnerabilities and Exposures \(CVEs\) that are created by it.
-   **Version 2.5.0 - May 2023**

    Fixed: Container Vulnerable Items \(CVIT\)s are created as expected only for base images that are used to fetch registry scan data.

-   **Version 2.4.0 - February 2023**
    -   Fixed:
        -   Create CVITs for an image without tags. A placeholder record with the name "No tags are defined for this container image" is created in cmdb\_ci\_container\_repository\_entry table to avoid downstream errors.
        -   Along with the CVITs created from 'vulnerabilities' attribute under 'history' in the response payload, we now process the data with 'layerTime': '0' from 'vulnerabilities' attribute outside 'history'.
-   **Version 2.3.1 - November 2022**
    -   Fixed:
        -   Resized the Image and Base Image attributes on the Prisma Vulnerabilities Import set table to avoid data truncation.
        -   Fixed the Prisma Containers Count integration to use the same configuration as Prisma Vulnerabilities Import integration.
-   **Version 2.2.1 - August 2022**
    -   New: The report\_view access control lists \(ACLs\) that govern who can see reports in dashboards and elsewhere are enabled by default in the Tokyo release.
    -   Fixed: The handling of integration process failure in Prisma Cloud Compute.
-   **Version 2.1.0 - May 2022**

    New: Added multiple data sources to the Prisma Vulnerabilities Integration and Prisma Base Images integration to enable parallel processing of the imported data.

-   **Version 2.0.4 - April 2022**
    -   Fixed:
        -   Populate the Docker image labels in to the CMDB key value table.
        -   Fixed the configuration page load issue in the Domain Separation enabled environment.
-   **Version 2.0.2 - March 2022**

    Import vulnerabilities detected by Prisma Cloud Compute in deployed container images into ServiceNow platform and enable remediation workflow involving security and application development teams.


