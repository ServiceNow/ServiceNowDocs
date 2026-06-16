---
title: Vulnerability Response Integration with Palo Alto Prisma Cloud release notes
description: Version history for the Vulnerability Response Integration with Palo Alto Prisma Cloud on the ServiceNow Store .
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-palo-alto-prisma-cloud.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Vulnerability Response Integration with Palo Alto Prisma Cloud release notes

Version history for the Vulnerability Response Integration with Palo Alto Prisma Cloud on the ServiceNow Store .

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.2.0 - June 2026 \(USEM\)**

    Changed: Updated Access Control Lists \(ACLs\) for queries on the app-vul-prismacloud repository in the Prisma Cloud \(Redlock\) integration to align with internal security directives.

-   **Version 30.1.2 - April 2026 \(USEM\)**

    Fixed: Disabling a Prisma Cloud policy now correctly deactivates the associated Compliance Test, allowing related test results to auto-close as expected.

-   **Version 2.8.2 - April 2026**

    Fixed: Disabling a Prisma Cloud policy now correctly deactivates the associated Compliance Test, allowing related test results to auto-close as expected.

-   **Version 2.8.0 - December 2025**
    -   New: Updated the discovered item state to CI Decommissioned based on resource\_deleted information from Prisma.
    -   Changed: Formatted remediation details into a more readable format.
-   **Version 2.7.0 - May 2025**

    Fixed: Duplicate remediation tasks for Prisma test results are no longer being created.

-   **Version 3.1.3 - February 2025**
    -   Changed:
        -   Registry can now be added as a CVIT granular key.
        -   The CVIT granularity configuration includes two options \(Scanner or Discovery Information\) to allow selection of granularity based on scanner or discovery data, depending on whether the ITOM plugin is installed.
        -   Added path as a unique key for findings key. This means, a package can be present in multiple locations leading to multiple findings
        -   Populate Cloud Resource Type in Discovered Items upon executing Prisma Host Integration
-   **Version 2.6.2 - May 2024**

    Fixed: Improvements have been made to better handle Azure-related alerts in Palo Alto Prisma Cloud.

-   **Version 2.6.0 - November 2023**
    -   Fixed:
        -   When the scanner reopens test results, the resolution field is cleared.
        -   When test results in deferred state are reingested by the scanner, their state is either determined as Open or Deferred depending on the deferral expiration window.
-   **Version 2.5.3 - October 2023**
    -   Fixed:
        -   Added a new comprehensive integration which runs weekly and pulls all the alerts which were updated in the past week.
        -   Updated Prisma alert integration to pull data based on status update since the last successful run time.
-   **Version 2.7.2 - August \(Vancouver\)**

    Changed: On running Prisma integrations, the Last Pass field will be populated on the test results.

-   **Version 2.4.1 - June 2023**

    Fixed: Earlier, a cloud resource with the same resource id in different cloud accounts is associated with the same discovered item as the source id was populated only with resource id. Due to this, the test results and discovered items of the secondary accounts were missed. This issue has been fixed. From this release, the source id of discovered item is populated with the combination of resource id, type, account, and region so that any new asset with a different account is associated with the correct cloud resource, and discovered items and test results are created accordingly.

-   **Version 2.4.0 - May 2023**

    Version 2.4.0 certified for Utah, Tokyo, and San Diego.

-   **Version 2.3.1 - February 2023**

    Changed: Framework updates to use 'Security Support Common' common code instead of Vulnerability Response.

-   **Version 2.2.1 - November 2022**

    Changed: Updated the cloud lookup rules to make them extensible to support various resource types.

-   **Version 2.1.0 - September 2022**
    -   New: Seed data for cloud resource types
    -   Changed: Updated the cloud CI lookup rules
    -   Fixed: Added support for tag sets
-   **Version 2.0.0 - May 2022**

    The Vulnerability Response Integration with Palo Alto Prisma Cloud integration application facilitates ingestion of policies and alerts from Prisma Cloud, as tests and test results respectively, in the Configuration Compliance application. With the right configuration, the test results can be managed seamlessly by assigning appropriate risk scores, and grouping and assigning them to relevant users and groups.


