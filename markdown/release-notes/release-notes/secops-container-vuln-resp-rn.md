---
title: Container Vulnerability Response release notes
description: The ServiceNow Container Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Container Vulnerability Response was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-05-29"
reading_time_minutes: 4
---

# Container Vulnerability Response release notes

The ServiceNow® Container Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Container Vulnerability Response was enhanced and updated in the Xanadu release.

## Container Vulnerability Response highlights for the Xanadu release

-   Reevaluate the risk score, assignments, remediation target date, exceptions, and remediation task for a specific set of container vulnerable items in Vulnerability Manager Workspace.

See [Container Vulnerability Response](https://www.servicenow.com/docs/access?context=cvr-landing&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) for more information.

**Important:** Container Vulnerability Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[New Properties module](https://www.servicenow.com/docs/access?context=installed-with-cvr-data&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v2.11.3 of Container Vulnerability Response, a new **Properties** module has been added to the navigation menu under the **Administration** section. This module enables direct modification of the values, offering a user-friendly method to manage and update system properties directly from the interface.

-   **[Create auto-close rules for Container Vulnerability Response](https://www.servicenow.com/docs/access?context=cvr-create-auto-close-rules&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v2.11.3 of Container Vulnerability Response, define auto-close rules with advanced conditions to automatically close older or stale CVITs based on defined filter criteria on container vulnerabilities.

-   **[Customize the calculation of Age and Age closed parameters of a container vulnerable item](https://www.servicenow.com/docs/access?context=container-vul-items-fields&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v2.11.3 of Container Vulnerability Response, the Age and Age Closed durations of a Container Vulnerable Item can be configured to be calculated from the date in the Created, Opened, or First Found fields.

-   **Open the search results in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-change-app-scope-search&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) or [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-change-app-scope-search&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) rather than the Classic UI**

    Starting with v24.0.6 of Vulnerability Response, automatically open your search results in the Vulnerability Manager Workspace or IT Remediation Workspace rather than the Classic UI, by adjusting the application scope in the unified navigation bar to Vulnerability Manager Workspace or IT Remediation Workspace respectively. These application scopes are available to you based on your assigned role.

-   **[Vulnerability Manager Workspace access to the sn\_vul\_container.read\_all role](https://www.servicenow.com/docs/access?context=installed-with-cvr-data&version=xanadu&pubname=xanadu-security-management&section=roles-installed-cvr&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, as a user with the sn\_vul\_container.read\_all role, you can view the container vulnerable items in the Vulnerability Manager Workspace.

-   **[IT Remediation Workspace access to the sn\_vul\_container.read\_assigned role](https://www.servicenow.com/docs/access?context=installed-with-cvr-data&version=xanadu&pubname=xanadu-security-management&section=roles-installed-cvr&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, as a user with the sn\_vul\_container.read\_assigned role, you can view the container vulnerable items assigned to you and your assignment groups in the IT Remediation Workspace and remediate them.

-   **Navigate to the List page in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) or [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) by selecting the links from the All menu**

    Starting with v24.0.6 of Vulnerability Response, when you enable the 'sn\_vul\_cmn\_ws.navigate\_to\_workspace' system property, selecting predefined filter links in the Container Vulnerability Response module from the 'All' menu will automatically open these links in the List page in the Vulnerability Manager Workspace or IT Remediation Workspace based on your role.

-   **Hide the record count on the lists in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) and [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, you can hide the record count on the lists in the List page of the Vulnerability Manager Workspace and IT Remediation Workspace, by adding the table names to the **glide.ui.list.seismic.omit.count** system property.

-   **[Enable automatic refresh for the Home page dashboard in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-home-page-create-filter&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, when creating and editing filters on the Container Vulnerabilities tab on the Home page of the Vulnerability Manager Workspace, you can configure the widgets to automatically refresh. Otherwise, you can manually refresh the widgets by selecting the **Refresh** button on the Container Vulnerabilities tab.

-   **[Re-evaluating remediation properties for all records in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-reevaluate-remediation-parameters&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, you can evaluate the remediation properties for all the Container Vulnerable Items from the Container Vulnerable Items list by selecting the **All items** in the **Record selection** field of the Re-evaluate remediation properties modal in the Vulnerability Manager Workspace.

-   **[Re-evaluate the remediation properties for container vulnerable items in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-reevaluate-remediation-parameters&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Select the container vulnerable items conditionally for reevaluating the following remediation properties in Vulnerability Manager Workspace:

    -   Assignments
    -   Remediation tasks
    -   Remediation target date
    -   Exceptions \(Vulnerability Response v24.0.6\)
    -   Risk score
-   **[Enhanced processing performance of scheduled job](https://www.servicenow.com/docs/access?context=installed-with-cvr-data&version=xanadu&pubname=xanadu-security-management&section=scheduled-jobs-installed-cvr&ft:locale=en-US)**

    The **Rollup container vulnerable item values to vulnerability and group** scheduled job is enhanced to create background jobs with multithreading capabilities. This upgrade involves segmenting the job into several smaller child jobs, which are executed either in parallel or concurrently. This modification enables processing of multiple records simultaneously, thus significantly speeding up the overall task.

-   **[for Container Vulnerability Response](https://www.servicenow.com/docs/access?context=quick-start-tests&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that Container Vulnerability Response works as expected. If you customized Container Vulnerability Response, copy the quick start tests and configure them for your customizations.

-   **[Vulnerability Response Prisma Registry Integration](https://www.servicenow.com/docs/access?context=pcc-integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Now you can ingest the static image findings obtained from the Prisma registry scan into the ServiceNow Container Vulnerability Response.


## Changed in this release

-   **[Deprecated the privilege to delete a container vulnerable item for the Admin role](https://www.servicenow.com/docs/access?context=installed-with-cvr-data&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    As an admin with the sn\_vul.vulnerability\_admin role, you can't delete a container vulnerable item. This privilege is now given to the sn\_vul.delete granular role.


## Removed in this release

The **Close** button has been removed for a remediation task in the classic UI, Vulnerability Manager Workspace, and IT Remediation Workspace.

**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

