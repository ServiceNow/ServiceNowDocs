---
title: Vulnerability Response release notes
description: The ServiceNow Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Vulnerability Response was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-09-29"
reading_time_minutes: 8
---

# Vulnerability Response release notes

The ServiceNow® Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Vulnerability Response was enhanced and updated in the Xanadu release.

## Vulnerability Response highlights for the Xanadu release

-   Reevaluate the risk score, assignments, remediation target date, exceptions, and remediation task for a set of vulnerable items in the Vulnerability Manager Workspace.
-   Reassess the vulnerable item records from the workspace.
-   Navigate to the Exposure Assessment page in the Vulnerability Manager Workspace or Vulnerability Assessment Workspace from the All menu with the Vulnerability Response Pro or Enterprise subscription.
-   View risk rating-related changes in the Work notes section.
-   Access information on how an item's risk score is adjusted according to modifications in the vulnerability calculators.

See [Vulnerability Response](https://www.servicenow.com/docs/access?context=vuln-landing-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) for more information about Vulnerability Response. See the [Vulnerability Response Compatibility Matrix and Release Schema Changes](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) Knowledge Base article for more information about released Security Operations applications and their version compatibility.

**Important:** Vulnerability Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Identify Wiz Resource Types for import](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Identify the Resource Types \(assets\) that are reported by Wiz that you want to import with the Wiz Integration Resource Type configuration page in your ServiceNow AI Platform instance.

    The Resource Types that you select apply to all the primary Wiz vulnerability and compliance integrations except the Wiz Container Vulnerability Integration. See the [Wiz Vulnerability Response Integrations](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) for more information about the vulnerability and compliance integrations.

-   **[Wiz Backfill Integrations](https://www.servicenow.com/docs/access?context=wiz-backfill&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Retrieve and process data stored on the Wiz Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table for assets that were not processed by the primary Host Vulnerability Integration with a specialized Wiz Backfill Integration.

    The Host Vulnerability Backfill Integration is activated by default.

    **Note:** The Wiz Asset Integration and the Wiz Container Vulnerability Integration do not have backfill integrations. The Wiz Asset Integration can discover assets and create and update discovered item records on the Discovered item \[sn\_sec\_cmn\_src\_ci\] table. The Wiz Container Vulnerability Integration imports and processes discovered container image records.

-   **[Create solutions from scanners](https://www.servicenow.com/docs/access?context=vuln-solution-mgmt&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, solution records can now be configured to be created from scanners such as Tenable, Qualys, and Microsoft Threat and Vulnerability Management \(MS TVM\). These solutions are set as preferred in the absence of options from software vendors.

-   **[Activate or deactivate CVEs for exposure assessment](https://www.servicenow.com/docs/access?context=vr-ws-activate-deactivate-cves&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with version 4.0.1 of Vulnerability Exposure Assessment, if a Common Vulnerability Entry \(CVE\) has not been updated or had vulnerable items \(VITs\) created in the past 30 days, the exposure assessment record for that CVE is automatically marked as inactive. However, you can manually activate or deactivate these records. Additionally, the scheduled job **Check potential vulnerability**exposure regularly scans for such CVEs to designate them as inactive. If there is an update, it marks them as active.

-   **[Split detections from Tenable and Microsoft TVM scanners](https://www.servicenow.com/docs/access?context=vuln_integrations&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, you can split the detections from Tenable and Microsoft Threat and Vulnerability Management \(MS TVM\) scanners, enabling the creation of a unique vulnerable item \(VIT\) for each detected vulnerability instance. This split enables the assignment of VITs to various remediation teams, enhancing the management and tracking of vulnerabilities. 

-   **[New Properties module](https://www.servicenow.com/docs/access?context=installed-with-vr&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, a new **Properties** module has been added to the navigation menu under the **Administration** section. This module enables direct modification of the values, offering a user-friendly method to manage and update system properties directly from the interface.

-   **[Deletion of classification rules and application on discovered items](https://www.servicenow.com/docs/access?context=delete-vulnerability-classification-rule&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, if a classification rule is deleted or deactivated, it’s no longer applied to the discovered item and the data in the **Classification** and **Classification\_type** fields get cleared.

-   **[Exceptions for CI creation](https://www.servicenow.com/docs/access?context=ci-creation-using-IRE&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, if Identification and Reconciliation engine \(IRE\) encounters exceptions that prevent the creation of configuration items \(CIs\), the specifics of these exceptions are recorded in the Additional Information field.

-   **[View configuration item history](https://www.servicenow.com/docs/access?context=reapply-discovered-items-ci-changes&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, you can view the updates to a CI in the Discovered Item table. Information including the previous CI, the updated CI, and the user who made the changes is documented in the Audit History related list.

-   **[Customize the calculation of Age and Age closed values of a vulnerable item](https://www.servicenow.com/docs/access?context=vulnerable-item-fields&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, the Age and Age Closed durations of a Vulnerable Item can be configured to be calculated from the date in the Created, Opened, or First Found fields.

-   **Open the search results in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-change-app-scope-search&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) or [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-change-app-scope-search&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) rather than the Classic UI**

    Starting with v24.0.6 of Vulnerability Response, automatically open your search results in the Vulnerability Manager Workspace or IT Remediation Workspace rather than the Classic UI, by adjusting the application scope in the unified navigation bar to Vulnerability Manager Workspace or IT Remediation Workspace respectively. These application scopes are available to you based on your assigned role.

-   **[Vulnerability Manager Workspace access to the sn\_vul.read\_all role](https://www.servicenow.com/docs/access?context=installed-with-vr&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, as a user with the sn\_vul.read\_all role, you can view the host vulnerable items in the Vulnerability Manager Workspace.

-   **[IT Remediation Workspace access to the sn\_vul.read\_assigned role](https://www.servicenow.com/docs/access?context=installed-with-vr&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, as a user with the sn\_vul.read\_assigned role, you can view the host vulnerable items assigned to you and your assignment groups in the IT Remediation Workspace and remediate them.

-   **Navigate to the List page in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) or [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) by selecting the links from the All menu**

    Starting with v24.0.6 of Vulnerability Response, when you enable the 'sn\_vul\_cmn\_ws.navigate\_to\_workspace' system property, selecting predefined filter links in the Vulnerability Response module from the 'All' menu will automatically open these links in the List page in the Vulnerability Manager Workspace or IT Remediation Workspace based on your role.

-   **Hide the record count on the Host Vulnerable Items list in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) and [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, you can hide the record count on the lists in the List page of the Vulnerability Manager Workspace and IT Remediation Workspace by adding the table names to the **glide.ui.list.seismic.omit.count** system property.

-   **[Enable automatic refresh for the Home page dashboard in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-home-page-create-filter&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, when creating and editing filters in the Host Vulnerabilities tab on the Home page of the Vulnerability Manager Workspace, you can configure the widgets to refresh automatically. Otherwise, you can manually refresh the widgets by selecting the **Refresh** button on the Host Vulnerabilities tab.

-   **[Re-evaluating remediation properties for all records in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-reevaluate-remediation-parameters&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, you can evaluate the remediation properties for all the Vulnerable Items from the Host Vulnerable Items list by selecting the **All items** option in the **Record selection** field of the Re-evaluate remediation properties modal in the Vulnerability Manager Workspace.

-   **[Reevaluate the remediation properties for vulnerable items in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-reevaluate-remediation-parameters&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Select the vulnerable items conditionally for reevaluating the following remediation properties in the Vulnerability Manager Workspace:

    -   Assignments
    -   Remediation tasks
    -   Remediation target date
    -   Exceptions \(Vulnerability Response v24.0.6\)
    -   Risk score
-   **[Navigate to the Exposure Assessment page in workspaces from the All menu](https://www.servicenow.com/docs/access?context=vr_sw_expsure_task&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    With the Vulnerability Response Pro or Enterprise subscription, you’re redirected to the Exposure Assessment page in the Vulnerability Manager Workspace or Vulnerability Assessment Workspace based on your role, on selecting the Exposure Assessment link in the All menu.

-   **[Common Security Advisory Framework \(CSAF\) scanner mapping is optional](https://www.servicenow.com/docs/access?context=import-csaf-file&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The Scanner mapping field is now optional for the following Common Security Advisory Framework \(CSAF\) import methods:

    -   File import
    -   Advisories
    -   CSAF URL
-   **[Multiple vendors supported for CSAF through Rolie feed](https://www.servicenow.com/docs/access?context=import-csaf-url&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Import vulnerability solutions from CSAF aggregators or trusted providers via URL import supporting Resource-Oriented Lightweight Information Exchange \(ROLIE\) feed. These vulnerability solutions are automatically mapped to the correct vendor and vulnerable items \(VITs\) based on the Common Vulnerabilities and Exposures \(CVEs\).

-   **[Enhanced processing performance of scheduled job](https://www.servicenow.com/docs/access?context=installed-with-vr&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The **Rollup vulnerable item values to vulnerability and group** scheduled job is enhanced to create background jobs with multithreading capabilities. This upgrade involves segmenting the job into several smaller child jobs, which are executed either in parallel or concurrently. This modification enables processing of multiple records simultaneously, thus significantly speeding up the overall task.

-   **[Workflow deprecation and replacement by flow designer](https://www.servicenow.com/docs/access?context=cj-common-vuln-tasks&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The following workflows have been deprecated and replaced by the flow designer:

    -   Exception Rule State Approval
    -   Remediation Task State Approval
    -   Vulnerability Response - Scan Vulnerability
    -   Vulnerable Item State Approval
    -   Vulnerability Response - Scan Vulnerable Item
    .

-   **[Risk score updates in the Notes section](https://www.servicenow.com/docs/access?context=vuln-calculators-rules&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Access information on how an item's risk score is adjusted according to modifications in the vulnerability calculators. These details are available in the Notes section and include:

    -   Calculator group name
    -   Calculator name
    -   Field values along with their weightage and impact on the risk score
    -   Final risk score
-   **[Vulnerability Crisis Management \(VCM\) is available as a separate subscription in the store](https://www.servicenow.com/docs/access?context=vulnerability-crisis-management&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v1.0.1 of Vulnerability Crisis Management, the application is available as a separate subscription in the store. You can access Vulnerability Crisis Management from the Vulnerability Assessment workspace only if you have fine- grained entitlement or have installed the application from the store. Previously, Vulnerability Crisis Management was included with the Vulnerability Emergency Response plugin.

-   **[Vulnerability Exposure Response is renamed as Vulnerability Exposure Assessment](https://www.servicenow.com/docs/access?context=vr-ws-exposure-assessment&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v3.2.2, the Vulnerability Emergency Response plugin has been renamed as Vulnerability Exposure Assessment.


## Changed in this release

-   **[Deprecated the privilege to delete a vulnerable item for the Admin role](https://www.servicenow.com/docs/access?context=installed-with-vr&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    As a vulnerability admin \[sn\_vul.vulnerability\_admin\], you can’t delete a vulnerable item. This privilege is now given to the sn\_vul.delete granular role.

-   **[Deprecated the privilege to delete source records for the sn\_vul.admin and sn\_vul.admin\_solutions roles](https://www.servicenow.com/docs/access?context=installed-with-vr&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The privilege to delete the source records has been deprecated for the sn\_vul.admin and sn\_vul.admin\_solutions roles. This privilege is given to the sn\_vul\_cmn.delete granular role.


## Removed in this release

The **Close** button has been removed for a remediation task in the Classic UI, Vulnerability Manager Workspace, and IT Remediation Workspace.

**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

