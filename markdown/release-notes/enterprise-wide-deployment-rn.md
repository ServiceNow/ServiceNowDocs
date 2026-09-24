---
title: SPM Enterprise-Wide Deployment release notes
description: The ServiceNow SPM Enterprise-Wide Deployment application provides data partitioning capabilities for Strategic Portfolio Management \(SPM\) tables that enable organizations to separate and control record visibility across functions such as departments and business units. See the following sections for release notes by version.The version 1.0.5 release restricts system administrator access to partition data by default. Administrators can enable access across all partitions through the system property if required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/enterprise-wide-deployment-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Strategic Portfolio Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# SPM Enterprise-Wide Deployment release notes

The ServiceNow® SPM Enterprise-Wide Deployment application provides data partitioning capabilities for Strategic Portfolio Management \(SPM\) tables that enable organizations to separate and control record visibility across functions such as departments and business units. See the following sections for release notes by version.

## About Enterprise-Wide Deployment

-   Separate and control record visibility across functions using partitions.
-   Enforce partition visibility automatically across Project Workspace, Portfolio Planning Workspace, Resource Management Workspace, and Strategic Planning Workspace.
-   Assign the EWD PMO role to users who require visibility across all partitions, such as PMO leads and portfolio managers.

See [SPM Enterprise-Wide Deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/ewd-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Enterprise-Wide Deployment by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store.

-   **Upgrade information**

    After upgrading to SPM Enterprise-Wide Deployment v1.0.5, the system administrators loose access to the partitioned-data that they don't have the respective partition role assigned. Set the **sn\_spm\_ewd.allow\_admin\_access\_to\_all\_partitions** system property to `true` if system administrators must continue accessing all the partitioned-data even though they don't have the respective partition role. For details, see [Configure administrator access to all partitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/configure-admin-access-to-all-partitions.md).


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-business-management-rn-landing.md)

## Version 1.0.5

The version 1.0.5 release restricts system administrator access to partition data by default. Administrators can enable access across all partitions through the system property if required.

### What's changed

-   **[Restrict system administrator access to partitioned data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/configure-admin-access-to-all-partitions.md)**

    Restrict system administrators from accessing partition-protected data through a new configurable system property. The system property **sn\_spm\_ewd.allow\_admin\_access\_to\_all\_partitions** controls whether system administrators can access all partitions by default. By default, this property is set to `false`, which means system administrators must have the appropriate partition role to access partition-protected data.

    Users with the system administrator or sn\_spm\_ewd.ewd\_admin role can configure this property. This enforces strict data governance policies at all security levels and prevents unintended access to sensitive partition data. When partition access restrictions apply, all user roles, including system administrators, are subject to uniform partition role validation.


