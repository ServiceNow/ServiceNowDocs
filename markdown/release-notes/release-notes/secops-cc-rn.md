---
title: Configuration Compliance release notes
description: The ServiceNow Configuration Compliance application enables you to prioritize and remediate the most critical configuration-related vulnerabilities in your environment quickly and efficiently. Configuration Compliance was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-09-29"
reading_time_minutes: 7
---

# Configuration Compliance release notes

The ServiceNow® Configuration Compliance application enables you to prioritize and remediate the most critical configuration-related vulnerabilities in your environment quickly and efficiently. Configuration Compliance was enhanced and updated in the Xanadu release.

## Configuration Compliance highlights for the Xanadu release

-   Reevaluate the risk score, assignments, remediation target date, exceptions, and remediation task for a set of test results in Vulnerability Manager Workspace.
-   View the percentage of CI compliance and test results compliance on a Test Group in Vulnerability Manager Workspace.

See [Configuration Compliance](https://www.servicenow.com/docs/access?context=vr-config-compliance-landing&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) for more information.

**Important:** Configuration Compliance is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Identify Wiz Resource Types for import](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Identify the Resource Types \(assets\) reported by Wiz in your environment on the Wiz Integration Resource Type configuration page in your ServiceNow AI Platform instance that you want to import.

    The Resource Types that you select apply to all the primary Wiz vulnerability and compliance integrations except the Wiz Container Vulnerability Integration.

-   **[Wiz Backfill Integrations](https://www.servicenow.com/docs/access?context=wiz-backfill&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Retrieve and process data stored on the Wiz Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table for missing assets that were not processed by the primary compliance integrations with specialized Wiz Backfill Integrations.

    -   Test Results Backfill Integration
    -   Host Test Results Backfill Integration
    -   Issues Backfill Integration
    The Wiz Backfill Integrations are activated by default.

-   **[Wiz Host Test Result Vulnerability Integration](https://www.servicenow.com/docs/access?context=wiz-host-test-result-tab-filters&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Import test results associated with the resource type, `VIRTUAL MACHINE` with the Wiz Host Test Result Vulnerability Integration. This integration is activated by default.

-   **[New Properties module](https://www.servicenow.com/docs/access?context=installed-with-config-compliance&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v15.1 of Configuration Compliance, a new **Properties** module has been added to the navigation menu under the **Administration** section. This module enables direct modification of the values, offering a user-friendly method to manage and update system properties directly from the interface.

-   **[Customize the calculation of Age and Age closed durations of a test result](https://www.servicenow.com/docs/access?context=view-vuln-config-compl-test-results&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v15.1 of Configuration Compliance, the Age and Age Closed durations of a test result can be configured to be calculated from the date in the Created, Opened, or First Found fields.

-   **[Associating a Qualys Test with its Test Group](https://www.servicenow.com/docs/access?context=Qualys-cc-Integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    You can associate a Qualys Test with its Test Group by enabling the **sn\_vulc.add\_policy\_as\_key** system property. This helps you to identify the Test Group to which a Test Result belongs to and differentiate Test records with the same Test id that are associated with different Test Groups.

-   **[Calculate the remediation target date of a remediation task with respect to the Last Opened date](https://www.servicenow.com/docs/access?context=cc-remed-target-rules&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v15.1 of Configuration Compliance, you can customize the calculation of the remediation target date of a remediation task to be calculated with respect to the Last Opened date.

-   **Open the search results in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-change-app-scope-search&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) or [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-change-app-scope-search&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) rather than the Classic UI**

    Starting with v24.0.6 of Vulnerability Response, automatically open your search results in the Vulnerability Manager Workspace or IT Remediation Workspace rather than the Classic UI, by adjusting the application scope in the unified navigation bar to Vulnerability Manager Workspace or IT Remediation Workspace respectively. These application scopes are available to you based on your assigned role.

-   **[Vulnerability Manager Workspace access to the sn\_vulc.read role](https://www.servicenow.com/docs/access?context=installed-with-config-compliance&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, as a user with the sn\_vulc.read role, you can view the test results in the Vulnerability Manager Workspace.

-   **Navigate to the List page in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) or [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) by selecting the links from the All menu**

    Starting with v24.0.6 of Vulnerability Response, when you enable the 'sn\_vul\_cmn\_ws.navigate\_to\_workspace' system property, selecting predefined filter links in the Configuration Compliance module from the 'All' menu will automatically open these links in the List page in the Vulnerability Manager Workspace or IT Remediation Workspace based on your role.

-   **Hide the record count on the lists in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) and [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, you can hide the record count on the lists in the List page of the Vulnerability Manager Workspace and IT Remediation Workspace by adding the table names to the **glide.ui.list.seismic.omit.count** system property.

-   **[Enable automatic refresh for the Home page dashboard in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-home-page-create-filter&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, when creating and editing filters on the Configuration Test Results tab on the Home page of the Vulnerability Manager Workspace, you can configure the widgets to refresh automatically. Otherwise, you can manually refresh the widgets by selecting the **Refresh** button on the Configuration Test Results tab.

-   **[Re-evaluating remediation properties for all records in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-reevaluate-remediation-parameters&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Starting with v24.0.6 of Vulnerability Response, you can evaluate the remediation properties for all the test results from the Configuration Test Results list by selecting the **All items** in the **Record selection** field of the Re-evaluate remediation properties modal in the Vulnerability Manager Workspace.

-   **[Re-evaluate remediation properties for test results in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-reevaluate-remediation-parameters&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Select the test results conditionally for reevaluating the following remediation properties in Vulnerability Manager Workspace:

    -   Assignments
    -   Remediation tasks
    -   Remediation target date
    -   Exceptions \(Vulnerability Response v24.0.6\)
    -   Risk score
-   **[Using bulk edit for test results in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-bulk-edit-overview&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Perform the following tasks on multiple test results simultaneously or a remediation task in Vulnerability Manager Workspace:

    -   [Assign test results to an assignment group for remediation](https://www.servicenow.com/docs/access?context=vmws-bulk-edit-assign&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US).
    -   [Request an exception in bulk](https://www.servicenow.com/docs/access?context=vmws-bulk-edit-request-exception&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US).
    -   [Mark test results as false positive in bulk](https://www.servicenow.com/docs/access?context=vmws-bulk-edit-request-false-positive&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US).
-   **[Populating additional information for the test results](https://www.servicenow.com/docs/access?context=view-vuln-config-compl-test-results&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The Age, Age closed, Closed date, Active, and Last open date columns have been added in the test results table.

    The test results that aren’t in the Closed state are marked as true in the **Active** field. The **Active** field replaces the **Result** and **State** fields in the filter conditions of the default-saved filters across the All menu, Configuration Compliance Overview, Unified, Cybersecurity Executive, and Health dashboards.

-   **[CI compliance and test results compliance on a Test Group in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    View the percentage of CI compliance and test results compliance on a Test Group in Vulnerability Manager Workspace.

-   **[Enabling or disabling the test results import for a Qualys test group in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=enable-disable-imports-qualys&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Enable or disable the import of test results for a Qualys test group in Vulnerability Manager Workspace.

-   **[Updating Rollup weights section in the roll up calculators](https://www.servicenow.com/docs/access?context=v11create-rollup-calc&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Other than the script format, an alternative approach of adding the weights in the Rollup Weights section for the rollup calculators has been introduced.

-   **[Percentage test result compliance in the Discovered Items table](https://www.servicenow.com/docs/access?context=discovered-items-fields&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The percentage of test results compliance of a CI is populated in the % Test Results Compliance column of the Discovered Item. To populate this value in the % Test Results Compliance column, set `calcTRComplianceForCI` to `true` in the **Update remediation metrics** scheduled job.

-   **[Quick Start Tests for Configuration Compliance](https://www.servicenow.com/docs/access?context=available-quick-start-tests&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that Configuration Compliance works as expected. If you customized Configuration Compliance, copy the quick start tests and configure them for your customizations.


## UI changes

-   **[Renamed the Is deprecated field in the Test Group form](https://www.servicenow.com/docs/access?context=view-vuln-config-compl-policies&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The **Is deprecated** field in the Test Group form is renamed to **Is imported**.

-   **[Renamed the Mark Deprecated button to Disable imports in the Test Group form](https://www.servicenow.com/docs/access?context=view-vuln-config-compl-policies&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The **Mark Deprecated** button in the Test Group form is renamed to **Disable Imports**.

-   **[Test Group mapping with Tests for Tenable and Microsoft Defender integrations](https://www.servicenow.com/docs/access?context=view-vuln-config-compl-policies&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The test groups are mapped with the Tests associated with the Tenable and Microsoft Defender integrations.

-   **[View the test result compliance percentage of a CI in the Discovered Items list](https://www.servicenow.com/docs/access?context=discovered-items-fields&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The percentage of the test results that are compliant with the tests associated with a Configuration Item \(CI\) is populated in the % Test Results Compliance column of the Discovered Item list. To populate this value in the % Test Results Compliance column, set the `calcTRComplianceForCI` parameter to `true` in the **Update remediation metrics** scheduled job.


## Changed in this release

-   **[Test result and remediation task state transitions](https://www.servicenow.com/docs/access?context=spc-findings-state-transition&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Enhancements to policy audits for Security Posture Control verify that retired assets are not evaluated by activated policies. If the state of an asset transitions from **Retired** back to **Active**, it is included in the next policy evaluation.

-   **[Non-zero risk score for passed test results](https://www.servicenow.com/docs/access?context=config-compliance-risk-calculator-example&version=xanadu&pubname=xanadu-security-management&section=cc-rollupcalc-example&ft:locale=en-US)**

    The risk score is calculated for passed test results to determine how much risk is mitigated.

-   **[Deprecated the privilege to delete a test result for the Admin role](https://www.servicenow.com/docs/access?context=installed-with-config-compliance&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    As an admin with the sn\_vulc.admin role, you can’t delete a test result. This privilege is now given to the sn\_vulc.delete granular role.


-   **[Updates to the Risk Score calculation for a Remediation Task](https://www.servicenow.com/docs/access?context=v11create-rollup-calc&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The average risk score of all the test results in a Remediation Task is considered for the risk score calculation of a Remediation task.


## Removed in this release

-   The **Reason** field in the Resolve modal has been removed for a remediation task in the classic UI, Vulnerability Manager Workspace, and IT Remediation Workspace.
-   The **Close** button has been removed for a remediation task, in the classic UI, Vulnerability Manager Workspace, and IT Remediation Workspace.

**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

