---
title: Application Vulnerability Response release notes
description: The ServiceNow Application Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Application Vulnerability Response was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 9
---

# Application Vulnerability Response release notes

The ServiceNow® Application Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Application Vulnerability Response was enhanced and updated in the Zurich release.

## Application Vulnerability Response highlights for the Zurich release

-   If you are currently using Application Vulnerability Response and you want to upgrade to Unified Security Exposure Management \(USEM\), see [Unified Security Exposure Management release notes](secops-sem-rn.md) for more information about USEM and the Unified Security Exposure Management migration.
-   Monitor your penetration test requests and findings, as well as your team's overall progress in the Penetration Test Workspace.
-   Reevaluate the risk score, assignments, remediation target date, exceptions, and remediation task for a specific set of application vulnerable items in the Vulnerability Manager Workspace.
-   Integrate with supported third-party scanners to import vulnerability data.
-   Compare application vulnerability-related data and determine if application vulnerabilities are found in an application.
-   Prioritize, remediate, and manage application vulnerable items \(AVIT\)s. Each application vulnerability represents a vulnerability entry in the Common Weakness Enumeration \(CWE\) or third-party libraries.
-   With the sn\_vul.app\_sec\_manager role, create application remediation tasks manually in the Vulnerability Manager Workspace.

See [Application Vulnerability Response](https://www.servicenow.com/docs/access?context=avr-landing&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information.

**Important:** Application Vulnerability Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Application Vulnerability Response to Zurich

-   If you are currently using Application Vulnerability Response, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Application Vulnerability Response and for upgrades to supported third-party integration applications.
-   For information about the new features of Vulnerability Response, see the [Vulnerability Response release notes](secops-vuln-resp-rn.md).
-   For more information about the released versions of the Application Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Zurich release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

## New in the Zurich release

-   **[Enhanced Compensatory controls](https://www.servicenow.com/docs/access?context=requesting-approving-risk-reduction&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    When new vulnerable items are ingested and associated with a remediation task that already has an approved compensating control, the reduced risk rating is now automatically inherited by those new vulnerable items.

-   **[Improved vulnerability assessment workflows](https://www.servicenow.com/docs/access?context=vr-ws-vuln-assessment&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**
    -   CI filtering for vulnerability assessments: You can now filter which configuration items are included in a vulnerability assessment using a condition builder.
    -   Business Application population on AVITs: AVITs created from SBOM assessment results now include Business Application information, helping you understand application impact and prioritize remediation.
    -   Priority roll‑down from vulnerability assessments: Updates to the priority of a vulnerability assessment now automatically roll down to associated VITs and AVITs, ensuring consistent prioritization based on the highest severity.
-   **[Remediation task rule execution mode](https://www.servicenow.com/docs/access?context=sem-grouping-multiple-findings-remediation-tasks-processing&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.

-   **[GitHub Application Vulnerability Integration – Generic secrets support](https://www.servicenow.com/docs/access?context=github-vuln-integration&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    The GitHub Secret Scanning Integration now imports generic secrets in addition to standard secrets from your GitHub repositories. A new Manage generic secrets in ServiceNow configuration option lets you control whether generic secrets are ingested. Imported secrets are mapped to Application Vulnerable Items \(AVIs\) with the scan type Secret, while generic secrets are mapped with the scan type Generic Secret.

-   **Enhancements to Application Vulnerability Response**

    The Unassign workflow is supported for application vulnerable items \(AVITs\) and remediation tasks \(AVULs\).

    -   Streamline application vulnerability assignments with the **Unassign** UI action from the more actions menu on an AVIT.
    -   Reassign incorrectly assigned AVITs, clarify ownership for reassessment, and maintain accurate triage records in workspace views.
    -   You have the option to send unassign requests for approval prior to clearing the Assigned to and Assignment group fields on records.
-   **[SBOM document upload via Github Action](https://www.servicenow.com/docs/access?context=vr-sbom-supported-apps&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Upload valid Software Bill of Material \(SBOM\) documents to ServiceNow platform with the help of GitHub Action.

-   **[Create application remediation tasks manually in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-create-remediation-task&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    With the sn\_vul.app\_sec\_manager role, you can create application remediation tasks manually by selecting some or all the records in the Application vulnerable items’ lists in the Vulnerability Manager Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating application remediation tasks.

-   **[Create application remediation tasks manually in the IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-create-remediation-task&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    With the sn\_vul.app\_security\_champion role, you can create application remediation tasks manually by selecting desired records in the Application vulnerable items’ lists in the IT Remediation Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating application remediation tasks.

-   **[Tenable Web Application Scanning Vulnerability Response Integration](https://www.servicenow.com/docs/access?context=tenable-was-integration&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    The Tenable.was integration now supports on‑demand execution of both application and vulnerability imports, allowing you to quickly ingest web applications, findings, and scan metadata into ServiceNow. Imported data automatically populates Discovered Applications, Vulnerability Entries, Scan Summaries, and AVITs, with full visibility through integration run tracking.

-   **[Manual Ingestion of Vulnerabilities for Application Vulnerability Integration](https://www.servicenow.com/docs/access?context=manual-ingestion-of-vulnerabilities-for-application-vulnerability-response&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Import AVITs from external sources via a standardised template \(e.g., CSV, Excel\) and manage Penetration test findings lifecycle. Now, you can ingest vulnerability data, including details such as affected application, vulnerability description, severity, remediation recommendations, including other necessary details. This enhancement allows you to simplifies the process of consolidating vulnerability data from diverse sources into a centralised Penetration test workspace.

-   **[Penetration Test Workspace](https://www.servicenow.com/docs/access?context=penetration-testing-dashboard&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Monitor your penetration test requests and findings as well as your team's overall progress in the Penetration Test Workspace. Prioritize tests that need your attention, track findings, and view assignments with the following data visualizations on the dashboard:

    -   Important items.
    -   Penetration test requests that are critical and by state.
    -   Reported findings.
    -   Overall remediation progress based on assignment.
-   **[Enhancements to Penetration Test Assessment Requests](https://www.servicenow.com/docs/access?context=pen_test_dashboard_components&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Along with Full Penetration, Focused, and Re-test, the following assessment types are included for Penetration Test Assessment Requests forms in the Penetration Test Workspace:

    -   Emergency Release - Supports emergency releases that are required for rapid software updates to address critical issues like security vulnerabilities.
    -   Bug Bounty Program - Rewards ethical hackers to find and report security vulnerabilities.
    -   Release Approvals - Ensure that all necessary checks are completed before deploying new software.
    -   One-off reviews - Assess specific projects outside regular development and release cycles to evaluate performance and implement improvements.
    -   Executive Interest - Report on senior management's engagement and support for critical projects within the organization.
    Enhancements to the Release Approval and Release Notes fields help you ensure quality and security for your pen test findings.

    The following states have been added to the Release approval field:

    -   **Not Applicable** \(Default\).
    -   **Approved**.
    -   **Denied**.
    You can add details to justify your release approvals in the Release notes field.

-   **[Associate CWEs for manual AVIT creation from Penetration Test Assessment Requests](https://www.servicenow.com/docs/access?context=penetration-testing-dashboard&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    On the Penetration test findings tab on Penetration Test Assessment Requests, you have the option to associate Common Weakness Enumerations \(CWE\)s or Common Vulnerabilities and Exposures \(CVE\)s in the **Vulnerability** field for manually created AVITs.

-   **Create change requests in Application Vulnerability Response**

    Users with the sn\_vul.app\_sec\_manager and sn\_vul.app\_sec\_champion roles as well as users with the sn\_vul.app\_developer role who have the ITIL role can create change requests from remediation tasks in the Application Vulnerability Response application. Create change requests to expedite your investigation for application vulnerabilities \(AVIT\)s that require manual intervention.

    -   Create change requests with prepopulated information for scanned applications that are classified as configuration items \(CI\)s.
    -   The change request workflow in Application Vulnerability Response is similar to the workflow supported in Vulnerability Response. For more information about the Vulnerability Response change request workflow, see [Change management for Vulnerability Response](https://www.servicenow.com/docs/access?context=vuln-change_mgmnt_ovrvw&version=zurich&pubname=zurich-security-management&ft:locale=en-US).
    **Note:** Change requests are supported for Application Vulnerability Response only if the discovered application is associated with a configuration item \(CI\). You must set `Product model` to **False** in the Use Product Model \[sn\_vul.use\_product\_model\] system property to associate a discovered application with a CI.

-   **[Enhancements to the Software Bill of Materials Workspace](https://www.servicenow.com/docs/access?context=sbom-landing&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**
    -   You can delete multiple BOM entity records and their related components with bulk edit from the Software Bill of Materials SBOM SBOM Workspace.
    -   Any Application Vulnerable Items \(AVIT\)s that are associated with deleted BOM entities automatically transition to **Closed**.
-   **[View risk score details of a vulnerable items in the Work notes section](https://www.servicenow.com/docs/access?context=avm-calculators-rules&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Starting with v25.0.3 of Application Vulnerability Response, the system property **sn\_sec\_cmn.risk\_score\_changes\_add\_worknotes** is inactive by default. If you enable it, only then you can see all the changes related to the risk score of an application vulnerable item in the Work notes section. Additionally, the work notes are updated only if there’s a change in the risk score.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Configure maximum rows in related lists](https://www.servicenow.com/docs/access?context=avm-configuring&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    To improve readability and performance, you can now limit the number of rows shown in related lists on forms by setting the system property **sn\_vul\_cmn.related\_list.set\_max\_row**.

-   **[Improved state management for remediation tasks and vulnerable items](https://www.servicenow.com/docs/access?context=vr-rt-states&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    State management logic for roll down of state from remediation tasks \(RTs\) to findings and roll up of state from findings to RTs has been refined across all modules. Updates improve accuracy by handling mixed item states \(a combination of Deferred and Closed\), supporting closure of tasks in sub-states like In-Review, and reopening tasks based on the Assigned To field. The update also improves handling of False Positive state transitions based on scanner results as source of truth. These enhancements reduce manual effort, clarify task ownership, and streamline remediation workflows.


## Activation information

Install Vulnerability Response and third-party integrations by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

