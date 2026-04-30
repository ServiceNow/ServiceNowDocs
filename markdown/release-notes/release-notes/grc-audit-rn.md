---
title: Audit Management release notes
description: The ServiceNow Audit Management application supports activities related to planning audit engagements, executing engagements, and reporting findings to an audit committee. Audit Management was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
---

# Audit Management release notes

The ServiceNow® Audit Management application supports activities related to planning audit engagements, executing engagements, and reporting findings to an audit committee. Audit Management was enhanced and updated in the Xanadu release.

## Audit Management highlights for the Xanadu release

-   Manage your documents and work papers in Audit Management as cloud files.
-   Link cloud files to any GRC record and share a single cloud file with multiple records.
-   Upload documents from your local computer as cloud files and link them to any record in ServiceNow.
-   Use the lite roles introduced in Audit Management for lighter business operations.

See [Audit Management](https://www.servicenow.com/docs/access?context=c_GRCAudits&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Audit Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Generate an audit report for an engagement using Microsoft Word template](https://www.servicenow.com/docs/access?context=generate-audit-report&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Use the Audit Workspace to generate audit reports for an engagement using Microsoft Word template to collaborate with your auditors in an effortless and user-friendly manner. You can manage the generated report as a cloud file either on cloud \(Microsoft SharePoint\) or as a sys\_attachment that is attached to the engagement record.

-   **[Cloud document management](https://www.servicenow.com/docs/access?context=manage-cloud-docs-using-onedrive-int&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Upload documents from your local computer as cloud files and link them to any record in ServiceNow. You can upload files to a predefined folder path and location.

-   **[User role enhancements in Audit Management](https://www.servicenow.com/docs/access?context=r_InstallWAudit&version=xanadu&pubname=xanadu-governance-risk-compliance&section=r_RolesInstallWAudit&ft:locale=en-US)**

    The following roles have been added:

    -   Use the Audit approver \(sn\_audit.approver\) role to approve an engagement and audit plan. Anyone with this role can be a part of an approver list. This role is also classified as a lite operator role.
    -   Use the Audit reader \(sn\_audit.reader\) role to view the audit-related entities, such as engagements, plans, observations, and audit tasks. Anyone with this role has exclusive read access to all the entities in the Audit Management application. This role is also classified as a lite operator role.

## Changed in this release

-   **[Domain separation and Audit Management](https://www.servicenow.com/docs/access?context=audit-management-domain-separation&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Changes are made to the domain assignment process to manage data segregation by the Managed Service Providers related to the objects in Audit Management and Advanced Audit.

-   **[Role change for users approving workflows](https://www.servicenow.com/docs/access?context=r_InstallWAudit&version=xanadu&pubname=xanadu-governance-risk-compliance&section=r_RolesInstallWAudit&ft:locale=en-US)**

    Approvers for an engagement and audit plan can also use the Audit approver \(sn\_audit.approver\) role as a lite operator role to approve audit workflows.


## Activation information

Install Policy and Compliance Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

