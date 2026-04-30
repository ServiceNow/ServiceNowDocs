---
title: Container Vulnerability Response release notes
description: The ServiceNow Container Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Container Vulnerability Response was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-05-28"
reading_time_minutes: 3
---

# Container Vulnerability Response release notes

The ServiceNow® Container Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Container Vulnerability Response was enhanced and updated in the Yokohama release.

## Container Vulnerability Response highlights for the Yokohama release

-   With the sn\_vul\_container.vulnerability\_analyst or sn\_vul\_container.vulnerability\_admin role, create container remediation tasks manually in the Vulnerability Manager Workspace.
-   With the role sn\_vul\_container.remediation\_owner, create container remediation tasks manually in the IT Remediation Workspace.

See [Container Vulnerability Response](https://www.servicenow.com/docs/access?context=cvr-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) for more information.

**Important:** Container Vulnerability Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **Enhancements to the Vulnerability Manager and IT Remediation workspaces starting with version 2.13**

    The Unassign workflow is supported for container vulnerable items \(CVITs\) and remediation tasks \(CVULs\).

    -   Streamline vulnerability assignments in the workspaces with the **Unassign** UI action from the more actions menu on a CVIT.
    -   Reassign incorrectly assigned CVITs, clarify ownership for reassessment, and maintain accurate triage records in workspace views.
    -   You have the option to send unassign requests for approval prior to clearing the Assigned to and Assignment group fields on records.
    . You can use the following values imported from the Prisma Cloud Compute integration as conditions when you create or update your assignment rules to help you track ownership across your container environments.

    -   Cloud account IDs
    -   Image namespaces
    -   Registry
    -   Hosts
    -   Labels
    -   Status - Vendor status for a resolved \(`Fixed`\) vulnerability
-   **[Create container remediation tasks manually in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-create-remediation-task&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    With the sn\_vul\_container.vulnerability\_analyst or sn\_vul\_container.vulnerability\_admin role, you can create container remediation tasks manually by selecting some or all the records in the Container vulnerable items lists in the Vulnerability Manager Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating container remediation tasks.

-   **[Create container remediation tasks manually in the IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-create-remediation-task&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    With the role sn\_vul\_container.remediation\_owner, you can create container remediation tasks manually by selecting some or all the records in the Container vulnerable items’ lists in the IT Remediation Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating container remediation tasks.

-   **[Configure container vulnerable items \(CVITs\) granularity using Registry and data source](https://www.servicenow.com/docs/access?context=pcc-integration&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Starting with v2.12.2 of Container Vulnerability Response, you can configure the granularity of container vulnerable items \(CVITs\) using Registry information and data sources. Depending on the chosen data source, you can view either image or kubernetes information related to a CVIT record.

-   **[Additional columns in the container vulnerable items \(CVITs\) table](https://www.servicenow.com/docs/access?context=container-vul-items-fields&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Starting with v2.12.2 of Container Vulnerability Response, you can see the precise date and time when a CVIT was first discovered, last opened, resolved, and last found, ensuring clarity and accounting for different time zones.

-   **[View risk score details of a container vulnerable item in the Work Notes section](https://www.servicenow.com/docs/access?context=cvr-calculator-rules&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Starting with v2.12.2 of Container Vulnerability Response, the system property **sn\_sec\_cmn.risk\_score\_changes\_add\_worknotes** is inactive by default. If you enable it, only then you can see all the changes related to the risk score of a container vulnerable item in the Work notes section. Additionally, the work notes are updated only if there’s a change in the risk score.


## Activation information

Install Container Vulnerability Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

