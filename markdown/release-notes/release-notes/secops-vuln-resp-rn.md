---
title: Vulnerability Response release notes
description: The ServiceNow Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Vulnerability Response was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-03-05"
reading_time_minutes: 13
---

# Vulnerability Response release notes

The ServiceNow® Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Vulnerability Response was enhanced and updated in the Zurich release.

## Vulnerability Response highlights for the Zurich release

-   If you are currently using Vulnerability Response and you want to upgrade to Unified Security Exposure Management \(USEM\), see [Unified Security Exposure Management release notes](secops-sem-rn.md) for more information about USEM and the Unified Security Exposure Management migration.
-   Import host vulnerability data from the Wiz scanners into Vulnerability Response VITs to help vulnerability managers assess your over-all cloud security posture.
-   With the sn\_vul.vulnerability\_analyst or sn\_vul.vulnerability\_admin role, create host remediation tasks manually in the Vulnerability Manager Workspace.
-   With the sn\_vul.remediation\_owner role, create host remediation tasks manually in the IT Remediation Workspace.

See [Vulnerability Response](https://www.servicenow.com/docs/access?context=vuln-landing-page&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information.

**Important:** Vulnerability Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Vulnerability Response to Zurich

If you are currently using Vulnerability Response, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Vulnerability Response and for upgrades to supported third-party integration applications.

The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table used for storing assets imported by the backfill integrations for the [Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US) is deprecated. If you are currently using the Vulnerability Response with Wiz integrations, after updating to new version 1.1, you must backdate any of your existing Wiz primary integrations by three days and run them. Please review more information about the Wiz integration at [SecOps articles on the Security Operations Community](https://www.servicenow.com/community/secops-articles/announcement-wiz-integration-with-servicenow-secops/ta-p/3325055).

For more information about the released versions of the Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Zurich release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

## New in the Zurich release

-   **[Remediation task rule execution mode](https://www.servicenow.com/docs/access?context=sem-grouping-multiple-findings-remediation-tasks-processing&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.

-   **[Unified Microsoft Defender Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=ms-defender-sem&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    The Microsoft Defender for Cloud and Microsoft Defender Threat and Vulnerability Management \(MS TVM\) plugins are now consolidated into a single plugin: Microsoft Defender Integration for Security Exposure Management. This consolidation deprecates the standalone Microsoft Defender for Cloud plugin. The unified plugin also introduces container image vulnerability ingestion from Microsoft Defender for Cloud, creating Container Vulnerable Items on your instance. A guided migration path is available to transfer existing data from the deprecated applications to the unified plugin.

-   **[Optimized Tenable.io Compliance Results ingestion](https://www.servicenow.com/docs/access?context=tenable-io-integrations-list&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Starting with v 6.1.3, the Tenable.io Compliance Results Integration is replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Qualys Integration – API enhancements](https://www.servicenow.com/docs/access?context=qualys-rest-messages&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Qualys Integration has been upgraded to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations. The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data.

-   **[Improved vulnerability assessment workflows](https://www.servicenow.com/docs/access?context=vr-ws-vuln-assessment&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**
    -   CI filtering for vulnerability assessments: You can now filter which configuration items are included in a vulnerability assessment using a condition builder.
    -   Business Application population on AVITs: AVITs created from SBOM assessment results now include Business Application information, helping you understand application impact and prioritize remediation.
    -   Priority roll‑down from vulnerability assessments: Updates to the priority of a vulnerability assessment now automatically roll down to associated VITs and AVITs, ensuring consistent prioritization based on the highest severity.
-   **[Enhanced Compensatory controls](https://www.servicenow.com/docs/access?context=requesting-approving-risk-reduction&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    When new vulnerable items are ingested and associated with a remediation task that already has an approved compensating control, the reduced risk rating is now automatically inherited by those new vulnerable items.

-   **[Enhancements to the Wiz Vulnerability Response Integration](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**
    -   The Universally Unique Identifier \(UUID\) that identifies detections for the Wiz Host Vulnerability integration will be mapped to a detection key.

        **Note:** This enhancement is supported for new customers only.

        For existing customers, the detection key for the Wiz Host Vulnerability integration is created using the combination of vulnerability, asset\_id, and proof.

    -   You can configure the **First** parameter for the Wiz Asset Integration to help you resolve 504 errors. You can reduce the page size if you are having memory issues or generating errors. The default value is 500.
-   **[Enhancements to Detection Key Configurations for Vulnerability Response](https://www.servicenow.com/docs/access?context=detection-key-configurations-for-vr&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Introduced configurable detection keys allowing customers to choose between Asset ID and Configuration Item, with validations, UI controls, and enhanced an existing schedule job to update existing detections.

-   **[Enhancements to the Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] is deprecated. After updating to version 1.1, you must backdate your existing primary Wiz integrations by three days and run them.

    The backfill integrations are activated by default.

    After you backdate and run your primary integrations, the following backfill integrations are no longer required:

    -   Host Vulnerability Backfill Integration
    -   Test Results Backfill Integration
    -   Host Test Results Backfill Integration
    -   Issues Backfill Integration
    Resource types filters are supported on the Host Vulnerability, Host Test Results, Test Results, and Issues tabs on the Wiz Configuration page.

    Additional attributes imported from Wiz that are not stored in the Discovered items \[sn\_sec\_cmn\_src\_ci\] table are stamped with `Asset Attributes` in this table.

    Test results from the Host misconfiguration integration are classified as result type 'host\_misconfiguration'.

    Data for resources that have the validated\_at\_runtime flag set to 'yes' is imported and populated on detections.

    The is\_ignored column is deprecated on the Host Test Results and Test Results Integrations. This column was replaced by the is\_result\_ignored column.

    The CMDB internet-facing field on the discovered item is mapped to Limited Internet Exposure on findings.

    Column length for the descriptions in the Host Vulnerability import table has been increased.

-   **[Improved remediation target date handling](https://www.servicenow.com/docs/access?context=sem-configure-remediation-target-rules&version=zurich&pubname=zurich-security-management&section=sem-recalculate-rt-date&ft:locale=en-US)**

    Remediation target \(RT\) dates now dynamically recalculate when a finding’s risk rating changes. Administrators can configure how recalculation occurs to ensure RT dates remain accurate and align with the latest risk updates, helping maintain consistent and reliable SLA tracking.

-   **[Identify Wiz Resource Types for import](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Identify the Resource Types \(assets\) that are reported by Wiz that you want to import with the Wiz Integration Resource Type configuration page in your ServiceNow AI Platform instance.

    The Resource Types that you select apply to all the primary Wiz vulnerability and compliance integrations except the Wiz Container Vulnerability Integration. See the [Wiz Vulnerability Response Integrations](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information about the vulnerability and compliance integrations.

-   **[Wiz Backfill Integrations](https://www.servicenow.com/docs/access?context=wiz-backfill&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Retrieve and process data stored on the Wiz Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table for assets that were not processed by the primary Host Vulnerability Integration with a specialized Wiz Backfill Integration.

    The Host Vulnerability Backfill Integration is activated by default.

    **Note:** The Wiz Asset Integration and the Wiz Container Vulnerability Integration do not have backfill integrations. The Wiz Asset Integration can discover assets and create and update discovered item records on the Discovered item \[sn\_sec\_cmn\_src\_ci\] table. The Wiz Container Vulnerability Integration imports and processes discovered container image records.

-   **[Import host vulnerability data with the Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Import host vulnerability findings related to virtual machines and serverless assets in your cloud environment with Wiz’s Host Vulnerability Integration. These findings are mapped to Host Vulnerable Items \(VITs\) within the Vulnerability Response application to support remediation workflows.

-   **[Modify the severity for a CVE or TPE](https://www.servicenow.com/docs/access?context=vmws-modify-reset-severity&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Vulnerability managers and vulnerability analysts can now adjust the severity of common vulnerabilities and exposures \(CVEs\) and third-party entries \(TPEs\) from the list view in the vulnerability manager workspace. The risk level of the associated vulnerabilities will be recalculated during the scheduled jobs based on the modified severity. You can also reset the severity to its original source value if required.

-   **[Questionnaire Support in Exception Management via Smart Assessment](https://www.servicenow.com/docs/access?context=vr-exception-management-smart-assessment&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Configure advanced questionnaires as part of the exception management process using Smart Assessment. This enhancement allows remediation owners to provide detailed context for exception requests and enables approvers to configure conditional questions to gather information for informed decision making.

    -   Collaboration and streamlined approval: Facilitate collaboration between your vulnerability management and remediation teams by streamlining the approval process with clear and complete exception justifications.
    -   Mandatory questionnaires: Block the submission of exception requests until mandatory questionnaires are completed. If a questionnaire is marked as mandatory, the test results and its associated remediation tasks remain in the 'Open' state until the questionnaire is completed and submitted.
    -   If the questionnaire is incomplete, the state change approval record is saved as 'Draft'. Only after completing the questionnaire can the user submit the exception request, which will then move the test results or remediation tasks to the 'In Review' state.
-   **[Lookup rules enhancements](https://www.servicenow.com/docs/access?context=working-unmatched-cis&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    When you reapply Lookup rules, Discovered items \(DIs\) that have been inactive for more than 90 days are ignored. These Discovered items \(DIs\) are also excluded from licensing considerations. Removing them from the lookup logic can improve performance and reduce processing time.

    -   Background job enhancements: New fields have been added to help you view successfully evaluate records, the time taken for processing, the time remaining, and an estimated number of records.
    -   Improved accuracy for non-CSDM Vulnerability Response users: A system property \(sn\_sec\_cmn.ci\_lifecycle\_status\_source\) has been introduced to help users who do not follow Common Service Data Model \(CSDM\) standards. This property ensures that Discovered items \(DIs\) and associated VITs are properly marked as Decommissioned and are excluded from the CI Lookup. Additionally, the Retired Configuration Items PA indicator has been updated to accurately reflect CIs based on the decommissioning flags.
    -   The scheduled job to create reconcile unmatched discovered items feature is deprecated. You can "Reapply Look up Rules" for selected or filtered items in the discovered items table view.
-   **[Tenable.cs integrations with the Vulnerability Response and Container Vulnerability Response application](https://www.servicenow.com/docs/access?context=tenable-cs-integrations-list&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    The Vulnerability Response Integration with Tenable application now supports data ingestion from Tenable.cs, enabling you to bring in cloud and container vulnerabilities directly into ServiceNow. This integration enhances your ability to prioritize and remediate vulnerabilities identified in Tenable cloud resources and container images. Key capabilities are:

    -   Importing vulnerabilities discovered by Tenable.cs in cloud hosts and container images into ServiceNow automatically.
    -   Enabling remediation workflows to triage, assign, and resolve the most critical vulnerabilities across cloud-native and containerized environments.
    -   Using the Setup Assistant to easily configure credentials and integration parameters—get started with minimal manual setup.
    -   Scheduling jobs to run periodically to import findings from Tenable.cs, create vulnerable items \(for cloud hosts\), create container vulnerable items and associate them with the relevant cloud resources and container image records.
-   **[Assess vulnerability exposure by publisher](https://www.servicenow.com/docs/access?context=vr-ws-exposure-publisher&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Starting with v5.0 of Vulnerability Exposure Assessment, a publisher-based assessment is introduced that enables you to assess the vulnerability impact by vendor. For example, Microsoft, and Red Hat. By focusing on recently disclosed vulnerabilities from critical vendors, you can prioritize remediation and proactively address threats, improving your overall security posture.

-   **[View risk score details of a vulnerable item in the Work notes section](https://www.servicenow.com/docs/access?context=vuln-calculators-rules&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Starting with v25.0.3 of Vulnerability Response, the system property **sn\_sec\_cmn.risk\_score\_changes\_add\_worknotes** is inactive by default. If you enable it, only then you can see all the changes related to the risk score of a vulnerable item in the Work notes section. Additionally, the work notes are updated only if there’s a change in the risk score.

-   **[Quick Start Tests for Vulnerability Response](https://www.servicenow.com/docs/access?context=available-quick-start-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that Vulnerability Response works as expected. If you customized Vulnerability Response, copy the quick start tests and configure them for your customizations.

-   **[Enhancements to exception rules handling](https://www.servicenow.com/docs/access?context=direct-deferral-of-vits-by-exception-rules-without-remediation-task-creation&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**
    -   Exception rules are reevaluated with nightly scheduled jobs.
    -   Vulnerable items that no longer match exception rule conditions are unlinked from remediation tasks.
    -   A deferred vulnerable item \(VIT\) is reopened if it doesn’t match any active exception rules.
    -   Exception rules don’t create remediation tasks. VITs are deferred directly and aren’t associated with a remediation task.
-   **[Tenable's endpoint scanning integration](https://www.servicenow.com/docs/access?context=tenable-io-integrations-list&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Support for Tenable's endpoint scanning integration to retrieve scan metadata. The integration fetches scan details using the last\_schedule\_id from existing asset data in Tenable.io.

-   **Reopened Count field on vulnerable items**

    Added the Reopened Count field on vulnerable items to track the number of times their states change from 'Closed' to 'Open' or to 'Active'.

-   **[Out-of-the-box vendor advisories via Common Security Advisory Framework \(CSAF\) integration](https://www.servicenow.com/docs/access?context=vuln-solution-mgmt&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    The following vendor advisories are configured out-of-the-box and are automatically activated when the Solution Management plugin is enabled: Redhat and Suse.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Enhanced UI experience in workspaces when reassigning vulnerable items](https://www.servicenow.com/docs/access?context=using-vulnerability-manager-workspace&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    When you reassign a record \(VIT, AVIT, CVIT, or CTR\) in workspace to a group you're not a member of, the system now confirms the reassignment and displays a clearer message explaining why the record is no longer visible. This helps you understand that access is now limited to the new assignment group, reducing confusion.


## Changed in this release

-   **[Granular VIT creation for Microsoft TVM recommendations](https://www.servicenow.com/docs/access?context=vr-configure-vi-key&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    You can now configure recommendation as a vulnerability item \(VIT\) key for Microsoft Threat &amp; Vulnerability Management \(TVM\). This enhancement enables each recommendation to generate a separate vulnerable item, offering more granular control for tracking, assigning, and managing remediation efforts, especially when different recommendations require actions from different teams.

-   **[Improved state management for remediation tasks and vulnerable items](https://www.servicenow.com/docs/access?context=vr-rt-states&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    State management logic for roll down of state from remediation tasks \(RTs\) to findings and roll up of state from findings to RTs has been refined across all modules. Updates improve accuracy by handling mixed item states \(a combination of Deferred and Closed\), supporting closure of tasks in sub-states like In-Review, and reopening tasks based on the Assigned To field. The update also improves handling of False Positive state transitions based on scanner results as source of truth. These enhancements reduce manual effort, clarify task ownership, and streamline remediation workflows.

-   **[Ability to manually cancel Exposure Assessment background jobs](https://www.servicenow.com/docs/access?context=vr-ws-exposure-assessment&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Vulnerability Admins and Event Managers can now cancel Exposure Assessment background jobs that were triggered with incorrect parameters or are taking longer than expected. This enhancement reduces downtime by removing the need to wait for the job to complete. Once cancelled, the sub-state is immediately set to User cancelled, and the state updates to Complete after the job is fully terminated; giving you better control and flexibility.

-   **[Configure maximum rows in related lists](https://www.servicenow.com/docs/access?context=vr-max-rows-rel-list&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    To improve readability and performance, you can now limit the number of rows shown in related lists on forms by setting the system property **sn\_vul\_cmn.related\_list.set\_max\_row**.

-   **[Qualys Integration – Detection Splitting](https://www.servicenow.com/docs/access?context=split-qualys-detections&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Use the Qualys Host Detection Integration to create a separate VIT for each vulnerability instance based on proof. This improves accuracy in vulnerability tracking and supports clearer team ownership during remediation.

-   **[Activate the Qualys QVS score integration](https://www.servicenow.com/docs/access?context=optional-modifications&version=zurich&pubname=zurich-security-management&section=enable-qualys-qvs-score&ft:locale=en-US)**

    Add Qualys-specific risk context to CVEs by importing QVS scores, helping you make more informed prioritization decisions.


## Activation information

Install Vulnerability Response and third-party integrations by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

