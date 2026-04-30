---
title: Vulnerability Response release notes
description: The ServiceNow Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Vulnerability Response was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-02-26"
reading_time_minutes: 6
---

# Vulnerability Response release notes

The ServiceNow® Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Vulnerability Response was enhanced and updated in the Yokohama release.

## Vulnerability Response highlights for the Yokohama release

-   With the sn\_vul.vulnerability\_analyst or sn\_vul.vulnerability\_admin role, create host remediation tasks manually in the Vulnerability Manager Workspace.
-   With the sn\_vul.remediation\_owner role, create host remediation tasks manually in the IT Remediation Workspace.

See [Vulnerability Response](https://www.servicenow.com/docs/access?context=vuln-landing-page&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) for more information about the Vulnerability Response application. See the [Vulnerability Response Compatibility Matrix and Release Schema Changes](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) Knowledge Base article for more information about released Security Operations applications and their version compatibility.

**Important:** Vulnerability Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Identify Wiz Resource Types for import](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Identify the Resource Types \(assets\) that are reported by Wiz that you want to import with the Wiz Integration Resource Type configuration page in your ServiceNow AI Platform instance.

    The Resource Types that you select apply to all the primary Wiz vulnerability and compliance integrations except the Wiz Container Vulnerability Integration. See the [Wiz Vulnerability Response Integrations](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) for more information about the vulnerability and compliance integrations.

-   **[Wiz Backfill Integrations](https://www.servicenow.com/docs/access?context=wiz-backfill&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Retrieve and process data stored on the Wiz Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table for assets that were not processed by the primary Host Vulnerability Integration with a specialized Wiz Backfill Integration.

    The Host Vulnerability Backfill Integration is activated by default.

    **Note:** The Wiz Asset Integration and the Wiz Container Vulnerability Integration do not have backfill integrations. The Wiz Asset Integration can discover assets and create and update discovered item records on the Discovered item \[sn\_sec\_cmn\_src\_ci\] table. The Wiz Container Vulnerability Integration imports and processes discovered container image records.

-   **[Create host remediation tasks manually in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-create-remediation-task&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    With the sn\_vul.vulnerability\_analyst or sn\_vul.vulnerability\_admin role, you can create host remediation tasks manually by selecting some or all the records in the Host vulnerable items’ lists in the Vulnerability Manager Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating host remediation tasks.

-   **[Create host remediation tasks manually in the IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-create-remediation-task&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    With the sn\_vul.remediation\_owner role, you can create host remediation tasks manually by selecting desired records in the Host vulnerable items’ lists in the IT Remediation Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating host remediation tasks.

-   **[Questionnaire Support in Exception Management via Smart Assessment](https://www.servicenow.com/docs/access?context=vr-exception-management-smart-assessment&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Configure advanced questionnaires as part of the exception management process using Smart Assessment. This enhancement allows remediation owners to provide detailed context for exception requests and enables approvers to configure conditional questions to gather information for informed decision making.

    -   Collaboration and streamlined approval: Facilitate collaboration between your vulnerability management and remediation teams by streamlining the approval process with clear and complete exception justifications.
    -   Mandatory questionnaires: Block the submission of exception requests until mandatory questionnaires are completed. If a questionnaire is marked as mandatory, the test results and its associated remediation tasks remain in the 'Open' state until the questionnaire is completed and submitted.
    -   If the questionnaire is incomplete, the state change approval record is saved as 'Draft'. Only after completing the questionnaire can the user submit the exception request, which will then move the test results or remediation tasks to the 'In Review' state.
-   **[Lookup rules enhancements](https://www.servicenow.com/docs/access?context=working-unmatched-cis&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    When you reapply Lookup rules, Discovered items \(DIs\) that have been inactive for more than 90 days are ignored. These Discovered items \(DIs\) are also excluded from licensing considerations. Removing them from the lookup logic can improve performance and reduce processing time.

    -   Background job enhancements: New fields have been added to help you view successfully evaluate records, the time taken for processing, the time remaining, and an estimated number of records.
    -   Improved accuracy for non-CSDM Vulnerability Response users: A system property \(sn\_sec\_cmn.ci\_lifecycle\_status\_source\) has been introduced to help users who do not follow Common Service Data Model \(CSDM\) standards. This property ensures that Discovered items \(DIs\) and associated VITs are properly marked as Decommissioned and are excluded from the CI Lookup. Additionally, the Retired Configuration Items PA indicator has been updated to accurately reflect CIs based on the decommissioning flags.
    -   The scheduled job to create reconcile unmatched discovered items feature is deprecated. You can "Reapply Look up Rules" for selected or filtered items in the discovered items table view.
-   **[Tenable.cs integrations with the Vulnerability Response and Container Vulnerability Response application](https://www.servicenow.com/docs/access?context=tenable-cs-integrations-list&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    The Vulnerability Response Integration with Tenable application now supports data ingestion from Tenable.cs, enabling you to bring in cloud and container vulnerabilities directly into ServiceNow. This integration enhances your ability to prioritize and remediate vulnerabilities identified in Tenable cloud resources and container images. Key capabilities are:

    -   Importing vulnerabilities discovered by Tenable.cs in cloud hosts and container images into ServiceNow automatically.
    -   Enabling remediation workflows to triage, assign, and resolve the most critical vulnerabilities across cloud-native and containerized environments.
    -   Using the Setup Assistant to easily configure credentials and integration parameters—get started with minimal manual setup.
    -   Scheduling jobs to run periodically to import findings from Tenable.cs, create vulnerable items \(for cloud hosts\), create container vulnerable items and associate them with the relevant cloud resources and container image records.
-   **[Assess vulnerability exposure by publisher](https://www.servicenow.com/docs/access?context=vr-ws-exposure-publisher&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Starting with v5.0 of Vulnerability Exposure Assessment, a publisher-based assessment is introduced that enables you to assess the vulnerability impact by vendor. For example, Microsoft, and Red Hat. By focusing on recently disclosed vulnerabilities from critical vendors, you can prioritize remediation and proactively address threats, improving your overall security posture.

-   **[View risk score details of a vulnerable item in the Work notes section](https://www.servicenow.com/docs/access?context=vuln-calculators-rules&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Starting with v25.0.3 of Vulnerability Response, the system property **sn\_sec\_cmn.risk\_score\_changes\_add\_worknotes** is inactive by default. If you enable it, only then you can see all the changes related to the risk score of a vulnerable item in the Work notes section. Additionally, the work notes are updated only if there’s a change in the risk score.

-   **[Quick Start Tests for Vulnerability Response](https://www.servicenow.com/docs/access?context=available-quick-start-tests&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that Vulnerability Response works as expected. If you customized Vulnerability Response, copy the quick start tests and configure them for your customizations.

-   **Enhancements to exception rules handling**
    -   Exception rules are reevaluated with nightly scheduled jobs.
    -   Vulnerable items that no longer match exception rule conditions are unlinked from remediation tasks.
    -   A deferred vulnerable item \(VIT\) is reopened if it doesn’t match any active exception rules.
    -   Exception rules don’t create remediation tasks. VITs are deferred directly and aren’t associated with a remediation task.
-   **[Tenable's endpoint scanning integration](https://www.servicenow.com/docs/access?context=tenable-io-integrations-list&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Support for Tenable's endpoint scanning integration to retrieve scan metadata. The integration fetches scan details using the last\_schedule\_id from existing asset data in Tenable.io.

-   **Reopened Count field on vulnerable items**

    Added the Reopened Count field on vulnerable items to track the number of times their states change from 'Closed' to 'Open' or to 'Active'.

-   **[Out-of-the-box vendor advisories via Common Security Advisory Framework \(CSAF\) integration](https://www.servicenow.com/docs/access?context=vuln-solution-mgmt&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    The following vendor advisories are configured out-of-the-box and are automatically activated when the Solution Management plugin is enabled: Redhat and Suse.


## Activation information

Install Vulnerability Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

