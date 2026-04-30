---
title: Application Vulnerability Response release notes
description: The ServiceNow Application Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Application Vulnerability Response is included as part of the ServiceNow Vulnerability Response application. Application Vulnerability Response was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-10-28"
reading_time_minutes: 9
---

# Application Vulnerability Response release notes

The ServiceNow® Application Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Application Vulnerability Response is included as part of the ServiceNow® Vulnerability Response application. Application Vulnerability Response was enhanced and updated in the Xanadu release.

## Application Vulnerability Response highlights for the Xanadu release

-   Reevaluate the risk score, assignments, remediation target date, exceptions, and remediation task for a specific set of application vulnerable items in the Vulnerability Manager Workspace.
-   Integrate with supported third-party scanners to import vulnerability data.
-   Compare application vulnerability-related data and determine if application vulnerabilities are found in an application.
-   Prioritize, remediate, and manage application vulnerable items \(AVI\)s. Each application vulnerability represents a vulnerability entry in the CWE or third-party libraries.
-   Identify the components used in your organization's applications and determine your potential exposure to risks associated with using open-source software from Software Bill of Materials \(SBOM\) files that you upload into your instance.

See [Application Vulnerability Response](https://www.servicenow.com/docs/access?context=avr-landing&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) for more information.

**Important:** Vulnerability Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Application Vulnerability Response to Xanadu

-   For information about the new features of Vulnerability Response, see [Vulnerability Response release notes](secops-vuln-resp-rn.md).
-   For more information about the released versions of the Application Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Xanadu release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

## New in the Xanadu release

-   **[Customize the calculation of Age and Age closed parameters of a application vulnerable item](https://www.servicenow.com/docs/access?context=avm-vul-items-fields&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, the Age and Age Closed durations of am Application Vulnerable item can be configured to be calculated from the date in the Created, Opened, or First Found fields.

-   **Open the search results in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-change-app-scope-search&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) or [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-change-app-scope-search&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) rather than the Classic UI**

    Starting with v24.0.6 of Vulnerability Response, automatically open your search results in the Vulnerability Manager Workspace or IT Remediation Workspace rather than the Classic UI, by adjusting the application scope in the unified navigation bar to Vulnerability Manager Workspace or IT Remediation Workspace respectively. These application scopes are available to you based on your assigned role.

-   **[Vulnerability Manager Workspace access to the sn\_vul.app\_read\_all role](https://www.servicenow.com/docs/access?context=installed-with-avm&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, as a user with the sn\_vul.app\_read\_all role, you can view the application vulnerable items in the Vulnerability Manager Workspace.

-   **[IT Remediation Workspace access to the sn\_vul.app\_read\_assigned role](https://www.servicenow.com/docs/access?context=installed-with-avm&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, as a user with the sn\_vul.app\_read\_assigned role, you can view the application vulnerable items assigned to you and your assignment groups in the IT Remediation Workspace and remediate them.

-   **Navigate to the List page in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) or [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) by selecting the links from the All menu**

    Starting with v24.0.6 of Vulnerability Response, when you enable the 'sn\_vul\_cmn\_ws.navigate\_to\_workspace' system property, selecting predefined filter links in the Application Vulnerability Response module from the 'All' menu will automatically open these links in the List page in the Vulnerability Manager Workspace or IT Remediation Workspace based on your role.

-   **Hide the record count on the lists in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) and [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, you can hide the record count on the lists in the List page in the Vulnerability Manager Workspace and IT Remediation Workspace, by adding the table names to the **glide.ui.list.seismic.omit.count** system property.

-   **[Enable automatic refresh for the Home page dashboard in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-home-page-create-filter&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, when creating and editing filters in the Application Vulnerabilities tab on the Home page of the Vulnerability Manager Workspace, you can configure the widgets to refresh automatically. Otherwise, you can manually refresh the widgets by selecting the **Refresh** button on the Application Vulnerabilities tab.

-   **[Re-evaluating remediation properties for all records in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-reevaluate-remediation-parameters&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, you can evaluate the remediation properties for all the Application Vulnerable Items from the Application Vulnerable Items list by selecting the **All items** in the **Record selection** field of the Re-evaluate remediation properties modal in the Vulnerability Manager Workspace.

-   **New Properties module**

    Starting with v24.0.6 of Application Vulnerability Response, a new **Properties** module has been added to the navigation menu under the **Administration** section. This module enables direct modification of the values, offering a user-friendly method to manage and update system properties directly from the interface.

-   **[View, classify, and assign software license information you upload with your SBOM files](https://www.servicenow.com/docs/access?context=vr-sbom-license-overview&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Use the License administration module in the SBOM Workspace to help you determine your over-all license compliance and risk exposure to the open-source and vendor-supplied software components you use in your application development.

    -   View all the licenses that are used in your organization in the License administration module.
    -   Classify existing licenses as: "Permitted", "Restricted", "Banned", or "Unclassified", and create new licenses.
    -   For unassigned or missing licenses, you can manually assign licenses to components used by your applications.
-   **[Closed application vulnerable items in the SBOM Workspace reopen automatically](https://www.servicenow.com/docs/access?context=vr-sbom-config-sbom-response&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    A **Closed** application vulnerable item \(AVIT\) for a component with an associated vulnerability is reopened automatically and visible in the SBOM Workspace if the following conditions are met:

    -   The Reopen AVITs if detected \(sn\_sbom\_resp.reopen\_avits\_if\_detected\) system property is activated. This system property is activated by default.
    -   The AVIT with the associated vulnerability is detected again by a third-party integration's vulnerability scans or the component with the vulnerability is part of a subsequent SBOM upload.
    -   The substate of the **Closed** AVIT is not one of the following: **Mitigation Control in Place**, **Not Affected**, or **False Positive**. AVITs with these substates are not reopened by the system property.
    Deactivate the system property only if you do not want **Closed** AVITs to reopen automatically.

-   **[Reevaluate the remediation properties for application vulnerable items in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-reevaluate-remediation-parameters&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Select the application vulnerable items conditionally for reevaluating the following remediation properties in the Vulnerability Manager Workspace:

    -   Assignments
    -   Remediation tasks
    -   Remediation target date
    -   Exceptions \(Vulnerability Response v24.0.6\)
    -   Risk score
-   **[Software Bill of Materials enhancements for CycloneDX SBOM files](https://www.servicenow.com/docs/access?context=vr-sbom-exploring&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The following enhancements were made to support SBOM files in CycloneDX format:

    Import additional information in CycloneDX SBOM files with the \(**sn\_sbom\_core.collect\_properties**\) property. This property is deactivated by default. Activate the property to import information that is generally not supported. Any information imported from these properties is uploaded to the SBOM Component Property \[sn\_sbom\_comp\_property\] table for the following:

    -   Uploaded SBOM files
    -   Metadata
    -   Individual vulnerabilities
    -   Components
    View imported component data for declared and concluded licenses for SBOM files in versions 1.4 and later of CycloneDX in two new license fields:

    -   **Declared**
    -   **Concluded**
    SBOM parsing support is enhanced for the following CycloneDX versions and component types:

    -   Version 1.5: Platform, Data, Device driver, Machine Learning model
    -   Version 1.6: Cryptographic
-   **[Enhancements to SBOM Response for PaCE](https://www.servicenow.com/docs/access?context=vr-sbom-exploring&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The Policy as Code Engine \(PaCE\) application is available for SBOM Response.

    -   Determine if components are stale or abandoned with the **Run PaCE policies for SBOM Response** scheduled job. The scheduled job is deactivated by default.
    -   View components that are identified as stale or abandoned as `Non-compliant` in the PaCE interface that is available in the SBOM Workspace.
-   **[Upload SBOM files to the ServiceNow AI Platform® from your GitHub repositories](https://www.servicenow.com/docs/access?context=vr-sbom-exploring&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Determine if SBOM files generated in your CI/CD \(continuous integration and continuous delivery/deployment\) pipelines have been successfully queued in your ServiceNow AI Platform instance.

    -   Protect your environments from potentially harmful components during software development cycles with GitHub Actions that you initiate from your GitHub environment.
    -   Obtain any required GitHub Actions for SBOM upload in the GitHub Marketplace.
-   **[Enhancements to Bill of Materials records for the Veracode Vulnerability Integration](https://www.servicenow.com/docs/access?context=veracode-vuln-integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    **Veracode** is mapped to the **Source** field for records in the Bill of Materials \[sn\_sbom\_doc\] table for the Veracode SBOM files that you upload.

-   **[Remediation Task Rules for Container Vulnerability Response](https://www.servicenow.com/docs/access?context=remediate-cvr&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Define and group container vulnerable items automatically based on the remediation task rules.

-   **[GitHub Secrets Scanning](https://www.servicenow.com/docs/access?context=github-vuln-integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Ingest secrets detected in your organization’s code along with the application security testing results, enabling ease of accessibility for developers to mitigate these results.

-   **[Enhanced processing performance of scheduled job](https://www.servicenow.com/docs/access?context=installed-with-avm&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The **Rollup application vulnerable item values to vulnerability and group** scheduled job is enhanced to create background jobs with multithreading capabilities. This upgrade involves segmenting the job into several smaller child jobs, which are executed either in parallel or concurrently. This modification enables processing of multiple records simultaneously, thus significantly speeding up the overall task.

-   **[Quick Start Tests](https://www.servicenow.com/docs/access?context=available-quick-start-tests&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) for Application Vulnerability Response**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that Application Vulnerability Response works as expected. If you customized Application Vulnerability Response, copy the quick start tests and configure them for your customizations.

-   **Set the Veracode integration to update SCA findings**

    You can select the scan that takes precedence for the final updates for SCA findings data imported from Veracode. On the Veracode configuration page, ‘Default’ is the set value until you change it. You must select the Include SCA findings check box and choose one from the list:

    -   Agent – the agent scan results make the final updates to SCA finding
    -   Upload – the upload scan results make the final updates to SCA finding
    -   Default – the last scan processed, either the agent or upload scan, makes the final updates to SCA findings
    **Note:** If you do not select the Include SCA findings check box on the configuration page, the scan you selected from the list is not used, and the last scan that is processed makes the final updates.

-   **Add and delete support for applications in Veracode imported from the ServiceNow AI Platform**

    Set the value for the \[sn-vul-veracode.app-mark-unseen-apps-inactive\] system property to ‘true’ to prevent errors if the Platform requests applications already deleted by Veracode. If this property is set to ‘true’ \(activated\), the successful import of the Application List Integration marks any unseen applications in the Platform as ‘inactive’.

-   **[Application Penetration testing enhancements](https://www.servicenow.com/docs/access?context=pen_test_workspace_avr&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    New workspace that permits you to use the penetration testing workflow in the Next Experience UI. Alignment of penetration testing for mobile application security with the recognized standards of the Mobile Application Security Verification Standard \(MASVS\) via a questionnaire in the penetration testing workflow.


## Removed in this release

The **Close** button has been removed for a remediation task in the classic UI, Vulnerability Manager Workspace, and IT Remediation Workspace.

## Activation information

Install Application Vulnerability Response by requesting it from the ServiceNow Store. Application Vulnerability Response is included as a part of the Vulnerability Response application. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

