---
title: Configuration Compliance release notes
description: The ServiceNow Configuration Compliance application enables you to prioritize and remediate the most critical configuration-related vulnerabilities in your environment quickly and efficiently. Configuration Compliance was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-09-29"
reading_time_minutes: 2
---

# Configuration Compliance release notes

The ServiceNow® Configuration Compliance application enables you to prioritize and remediate the most critical configuration-related vulnerabilities in your environment quickly and efficiently. Configuration Compliance was enhanced and updated in the Yokohama release.

## Configuration Compliance highlights for the Yokohama release

-   With the sn\_vulc.admin role, create remediation tasks manually in the Vulnerability Manager Workspace.
-   With the sn\_vulc.remediation\_owner role, create remediation tasks manually in the IT Remediation Workspace.

See [Configuration Compliance](https://www.servicenow.com/docs/access?context=vr-config-compliance-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) for more information.

**Important:** Configuration Compliance is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Identify Wiz Resource Types for import](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Identify the Resource Types \(assets\) reported by Wiz in your environment on the Wiz Integration Resource Type configuration page in your ServiceNow AI Platform instance that you want to import.

    The Resource Types that you select apply to all the primary Wiz vulnerability and compliance integrations except the Wiz Container Vulnerability Integration.

-   **[Wiz Backfill Integrations](https://www.servicenow.com/docs/access?context=wiz-backfill&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Retrieve and process data stored on the Wiz Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table for missing assets that were not processed by the primary compliance integrations with specialized Wiz Backfill Integrations.

    -   Test Results Backfill Integration
    -   Host Test Results Backfill Integration
    -   Issues Backfill Integration
    The Wiz Backfill Integrations are activated by default.

-   **[Wiz Host Test Result Vulnerability Integration](https://www.servicenow.com/docs/access?context=wiz-host-test-result-tab-filters&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Import test results associated with the resource type, `VIRTUAL MACHINE` with the Wiz Host Test Result Vulnerability Integration. This integration is activated by default.

-   **[Create remediation tasks manually in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-create-remediation-task&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    With the sn\_vulc.admin role, you can create remediation tasks manually by selecting some or all the records in the Configuration Test Results lists in the Vulnerability Manager Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating remediation tasks.

-   **[Create remediation tasks manually in the IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-create-remediation-task&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    With the sn\_vulc.remediation\_owner role, you can create remediation tasks manually by selecting desired records in the Configuration Test Results lists in the IT Remediation Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating remediation tasks.

-   **[View risk score details of a test result in the Work notes section](https://www.servicenow.com/docs/access?context=config-compliance-calculator-rules&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Starting with v15.2.1 of Configuration Compliance, the system property **sn\_sec\_cmn.risk\_score\_changes\_add\_worknotes** is inactive by default. If you enable it, only then you can see all the changes related to the risk score of a test result in the Work notes section. Additionally, the work notes are updated only if there’s a change in the risk score.

-   **[Quick Start Tests for Configuration Compliance](https://www.servicenow.com/docs/access?context=available-quick-start-tests&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that Configuration Compliance works as expected. If you customized Configuration Compliance, copy the quick start tests and configure them for your customizations.


## Activation information

Install Configuration Compliance by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

