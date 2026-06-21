---
title: Combined Configuration Compliance release notes for upgrades from Washington DC to Yokohama
description: Consolidated page of all release notes for Configuration Compliance from Washington DC to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-washingtondc-yokohama/yokohama-washingtondc-configurationcompliance-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 14
breadcrumb: [Products combined by family]
---

# Combined Configuration Compliance release notes for upgrades from Washington DC to Yokohama

Consolidated page of all release notes for Configuration Compliance from Washington DC to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Configuration Compliance release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Configuration Compliance to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Configuration Compliance.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Enhancements to Security Posture Control version 3.0](https://www.servicenow.com/docs/access?context=spc-policies-overview&family=washingtondc&ft:locale=en-US)**

Close existing related test results \(findings\) if you publish a new version of a policy or delete a policy. If you choose to close test results, test result and remediation task states transition in accordance with the state transition processes of the Configuration Compliance application. See [Test result and remediation task state transitions in the Security Posture Control application](https://www.servicenow.com/docs/access?context=spc-findings-state-transition&family=washingtondc&ft:locale=en-US) and [Test result and remediation task state transitions in the Configuration Compliance application](https://www.servicenow.com/docs/access?context=cc-state-transition&family=washingtondc&ft:locale=en-US) for more information.

Editing activated policies is supported in Security Posture Control. Versions are tracked and version numbers are displayed on the policy record and its related test results in Configuration Compliance.

-   **[Requesting false positive for a set of test results from the Vulnerability Manager Workspace and IT Remediation Workspace](https://www.servicenow.com/docs/access?context=vmws-tr-false-positive&family=washingtondc&ft:locale=en-US)**

Raise a false positive request for a set of test results simultaneously from the remediation task \(CRG\#\) in the Vulnerability Manager Workspace and IT Remediation Workspace.

-   **[Requesting false positive for a remediation task \(CRG\#\) from the Vulnerability Manager Workspace and IT Remediation Workspace](https://www.servicenow.com/docs/access?context=vr-ws-mark-fp&family=washingtondc&ft:locale=en-US)**

Raise a false positive request for a remediation task from the Vulnerability Manager Workspace and IT Remediation Workspace.

-   **[Setting up questionnaire for false positive requests](https://www.servicenow.com/docs/access?context=configure-exception-management-configuration-compliance&family=washingtondc&ft:locale=en-US)**

Set up a questionnaire for the false positive request of Test Results and Remediation Tasks to acquire additional information about the requests.

-   **[Updating the risk score in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=config-compliance-calculator-rules&family=washingtondc&ft:locale=en-US)**

Update the risk score of a test result \(TR\) using the **Calculate Risk Score** button in the record view of a TR in the Vulnerability Manager Workspace as per vulnerability calculators.

-   **[Analyzing the vulnerability landscape in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-home-page&family=washingtondc&ft:locale=en-US)**

Get an overall summary of the active test results through visual representation of risk ratings, remediation progress, assignment groups workloads, and records in remediation tasks on the Home page of the Vulnerability Manager Workspace.

-   **[Acquiring the summary of a set of test results using filters](https://www.servicenow.com/docs/access?context=vmws-home-page-create-filter&family=washingtondc&ft:locale=en-US)**

Get the summary of a active set of test results by filtering those test results on the Home page of the Vulnerability Manager Workspace.

-   **[Displaying records in workspaces upon clicking the links in email notifications](https://www.servicenow.com/docs/access?context=t_DefineEmailNotifications&family=washingtondc&ft:locale=en-US)**

When links are clicked in an email notification, records open in either the Vulnerability Manager Workspace or IT Remediation Workspace based on the user's role.

-   **[Notifications on false positive and exception requests](https://www.servicenow.com/docs/access?context=cc-ex-mgmt-request-approve&family=washingtondc&ft:locale=en-US)**

Receive notifications and reminders on change approval records with false positive and exception requests by setting approval expiry and reminder dates on the approval rules.

-   **[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&family=washingtondc&ft:locale=en-US) for Configuration Compliance.**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Configuration Compliance still works. If you customized Configuration Compliance, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Identify Wiz Resource Types for import](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&family=xanadu&ft:locale=en-US)**

Identify the Resource Types \(assets\) reported by Wiz in your environment on the Wiz Integration Resource Type configuration page in your ServiceNow AI Platform instance that you want to import.

The Resource Types that you select apply to all the primary Wiz vulnerability and compliance integrations except the Wiz Container Vulnerability Integration.

-   **[Wiz Backfill Integrations](https://www.servicenow.com/docs/access?context=wiz-backfill&family=xanadu&ft:locale=en-US)**

Retrieve and process data stored on the Wiz Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table for missing assets that were not processed by the primary compliance integrations with specialized Wiz Backfill Integrations.

    -   Test Results Backfill Integration
    -   Host Test Results Backfill Integration
    -   Issues Backfill Integration
The Wiz Backfill Integrations are activated by default.

-   **[Wiz Host Test Result Vulnerability Integration](https://www.servicenow.com/docs/access?context=wiz-host-test-result-tab-filters&family=xanadu&ft:locale=en-US)**

Import test results associated with the resource type, `VIRTUAL MACHINE` with the Wiz Host Test Result Vulnerability Integration. This integration is activated by default.

-   **[New Properties module](https://www.servicenow.com/docs/access?context=installed-with-config-compliance&family=xanadu&ft:locale=en-US)**

Starting with v15.1 of Configuration Compliance, a new **Properties** module has been added to the navigation menu under the **Administration** section. This module enables direct modification of the values, offering a user-friendly method to manage and update system properties directly from the interface.

-   **[Customize the calculation of Age and Age closed durations of a test result](https://www.servicenow.com/docs/access?context=view-vuln-config-compl-test-results&family=xanadu&ft:locale=en-US)**

Starting with v15.1 of Configuration Compliance, the Age and Age Closed durations of a test result can be configured to be calculated from the date in the Created, Opened, or First Found fields.

-   **[Associating a Qualys Test with its Test Group](https://www.servicenow.com/docs/access?context=Qualys-cc-Integration&family=xanadu&ft:locale=en-US)**

You can associate a Qualys Test with its Test Group by enabling the **sn\_vulc.add\_policy\_as\_key** system property. This helps you to identify the Test Group to which a Test Result belongs to and differentiate Test records with the same Test id that are associated with different Test Groups.

-   **[Calculate the remediation target date of a remediation task with respect to the Last Opened date](https://www.servicenow.com/docs/access?context=cc-remed-target-rules&family=xanadu&ft:locale=en-US)**

Starting with v15.1 of Configuration Compliance, you can customize the calculation of the remediation target date of a remediation task to be calculated with respect to the Last Opened date.

-   **Open the search results in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-change-app-scope-search&family=xanadu&ft:locale=en-US) or [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-change-app-scope-search&family=xanadu&ft:locale=en-US) rather than the Classic UI**

Starting with v24.0.6 of Vulnerability Response, automatically open your search results in the Vulnerability Manager Workspace or IT Remediation Workspace rather than the Classic UI, by adjusting the application scope in the unified navigation bar to Vulnerability Manager Workspace or IT Remediation Workspace respectively. These application scopes are available to you based on your assigned role.

-   **[Vulnerability Manager Workspace access to the sn\_vulc.read role](https://www.servicenow.com/docs/access?context=installed-with-config-compliance&family=xanadu&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, as a user with the sn\_vulc.read role, you can view the test results in the Vulnerability Manager Workspace.

-   **Navigate to the List page in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&family=xanadu&ft:locale=en-US) or [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-list-page&family=xanadu&ft:locale=en-US) by selecting the links from the All menu**

Starting with v24.0.6 of Vulnerability Response, when you enable the 'sn\_vul\_cmn\_ws.navigate\_to\_workspace' system property, selecting predefined filter links in the Configuration Compliance module from the 'All' menu will automatically open these links in the List page in the Vulnerability Manager Workspace or IT Remediation Workspace based on your role.

-   **Hide the record count on the lists in the [Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&family=xanadu&ft:locale=en-US) and [IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-list-page&family=xanadu&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, you can hide the record count on the lists in the List page of the Vulnerability Manager Workspace and IT Remediation Workspace by adding the table names to the **glide.ui.list.seismic.omit.count** system property.

-   **[Enable automatic refresh for the Home page dashboard in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-home-page-create-filter&family=xanadu&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, when creating and editing filters on the Configuration Test Results tab on the Home page of the Vulnerability Manager Workspace, you can configure the widgets to refresh automatically. Otherwise, you can manually refresh the widgets by selecting the **Refresh** button on the Configuration Test Results tab.

-   **[Re-evaluating remediation properties for all records in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-reevaluate-remediation-parameters&family=xanadu&ft:locale=en-US)**

Starting with v24.0.6 of Vulnerability Response, you can evaluate the remediation properties for all the test results from the Configuration Test Results list by selecting the **All items** in the **Record selection** field of the Re-evaluate remediation properties modal in the Vulnerability Manager Workspace.

-   **[Re-evaluate remediation properties for test results in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-reevaluate-remediation-parameters&family=xanadu&ft:locale=en-US)**

Select the test results conditionally for reevaluating the following remediation properties in Vulnerability Manager Workspace:

    -   Assignments
    -   Remediation tasks
    -   Remediation target date
    -   Exceptions \(Vulnerability Response v24.0.6\)
    -   Risk score
-   **[Using bulk edit for test results in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-bulk-edit-overview&family=xanadu&ft:locale=en-US)**

Perform the following tasks on multiple test results simultaneously or a remediation task in Vulnerability Manager Workspace:

    -   [Assign test results to an assignment group for remediation](https://www.servicenow.com/docs/access?context=vmws-bulk-edit-assign&family=xanadu&ft:locale=en-US).
    -   [Request an exception in bulk](https://www.servicenow.com/docs/access?context=vmws-bulk-edit-request-exception&family=xanadu&ft:locale=en-US).
    -   [Mark test results as false positive in bulk](https://www.servicenow.com/docs/access?context=vmws-bulk-edit-request-false-positive&family=xanadu&ft:locale=en-US).
-   **[Populating additional information for the test results](https://www.servicenow.com/docs/access?context=view-vuln-config-compl-test-results&family=xanadu&ft:locale=en-US)**

The Age, Age closed, Closed date, Active, and Last open date columns have been added in the test results table.

The test results that aren’t in the Closed state are marked as true in the **Active** field. The **Active** field replaces the **Result** and **State** fields in the filter conditions of the default-saved filters across the All menu, Configuration Compliance Overview, Unified, Cybersecurity Executive, and Health dashboards.

-   **[CI compliance and test results compliance on a Test Group in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-list-page&family=xanadu&ft:locale=en-US)**

View the percentage of CI compliance and test results compliance on a Test Group in Vulnerability Manager Workspace.

-   **[Enabling or disabling the test results import for a Qualys test group in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=enable-disable-imports-qualys&family=xanadu&ft:locale=en-US)**

Enable or disable the import of test results for a Qualys test group in Vulnerability Manager Workspace.

-   **[Updating Rollup weights section in the roll up calculators](https://www.servicenow.com/docs/access?context=v11create-rollup-calc&family=xanadu&ft:locale=en-US)**

Other than the script format, an alternative approach of adding the weights in the Rollup Weights section for the rollup calculators has been introduced.

-   **[Percentage test result compliance in the Discovered Items table](https://www.servicenow.com/docs/access?context=discovered-items-fields&family=xanadu&ft:locale=en-US)**

The percentage of test results compliance of a CI is populated in the % Test Results Compliance column of the Discovered Item. To populate this value in the % Test Results Compliance column, set `calcTRComplianceForCI` to `true` in the **Update remediation metrics** scheduled job.

-   **[Quick Start Tests for Configuration Compliance](https://www.servicenow.com/docs/access?context=available-quick-start-tests&family=xanadu&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Configuration Compliance works as expected. If you customized Configuration Compliance, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Identify Wiz Resource Types for import](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&family=yokohama&ft:locale=en-US)**

Identify the Resource Types \(assets\) reported by Wiz in your environment on the Wiz Integration Resource Type configuration page in your ServiceNow AI Platform instance that you want to import.

The Resource Types that you select apply to all the primary Wiz vulnerability and compliance integrations except the Wiz Container Vulnerability Integration.

-   **[Wiz Backfill Integrations](https://www.servicenow.com/docs/access?context=wiz-backfill&family=yokohama&ft:locale=en-US)**

Retrieve and process data stored on the Wiz Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table for missing assets that were not processed by the primary compliance integrations with specialized Wiz Backfill Integrations.

    -   Test Results Backfill Integration
    -   Host Test Results Backfill Integration
    -   Issues Backfill Integration
The Wiz Backfill Integrations are activated by default.

-   **[Wiz Host Test Result Vulnerability Integration](https://www.servicenow.com/docs/access?context=wiz-host-test-result-tab-filters&family=yokohama&ft:locale=en-US)**

Import test results associated with the resource type, `VIRTUAL MACHINE` with the Wiz Host Test Result Vulnerability Integration. This integration is activated by default.

-   **[Create remediation tasks manually in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-create-remediation-task&family=yokohama&ft:locale=en-US)**

With the sn\_vulc.admin role, you can create remediation tasks manually by selecting some or all the records in the Configuration Test Results lists in the Vulnerability Manager Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating remediation tasks.

-   **[Create remediation tasks manually in the IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-create-remediation-task&family=yokohama&ft:locale=en-US)**

With the sn\_vulc.remediation\_owner role, you can create remediation tasks manually by selecting desired records in the Configuration Test Results lists in the IT Remediation Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating remediation tasks.

-   **[View risk score details of a test result in the Work notes section](https://www.servicenow.com/docs/access?context=config-compliance-calculator-rules&family=yokohama&ft:locale=en-US)**

Starting with v15.2.1 of Configuration Compliance, the system property **sn\_sec\_cmn.risk\_score\_changes\_add\_worknotes** is inactive by default. If you enable it, only then you can see all the changes related to the risk score of a test result in the Work notes section. Additionally, the work notes are updated only if there’s a change in the risk score.

-   **[Quick Start Tests for Configuration Compliance](https://www.servicenow.com/docs/access?context=available-quick-start-tests&family=yokohama&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Configuration Compliance works as expected. If you customized Configuration Compliance, copy the quick start tests and configure them for your customizations.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Configuration Compliance features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

-   **[Test result and remediation task state transitions](https://www.servicenow.com/docs/access?context=spc-findings-state-transition&family=xanadu&ft:locale=en-US)**

Enhancements to policy audits for Security Posture Control verify that retired assets are not evaluated by activated policies. If the state of an asset transitions from **Retired** back to **Active**, it is included in the next policy evaluation.

-   **[Non-zero risk score for passed test results](https://www.servicenow.com/docs/access?context=cc-rollupcalc-example&family=xanadu&ft:locale=en-US)**

The risk score is calculated for passed test results to determine how much risk is mitigated.

-   **[Deprecated the privilege to delete a test result for the Admin role](https://www.servicenow.com/docs/access?context=installed-with-config-compliance&family=xanadu&ft:locale=en-US)**

As an admin with the sn\_vulc.admin role, you can’t delete a test result. This privilege is now given to the sn\_vulc.delete granular role.


-   **[Updates to the Risk Score calculation for a Remediation Task](https://www.servicenow.com/docs/access?context=v11create-rollup-calc&family=xanadu&ft:locale=en-US)**

The average risk score of all the test results in a Remediation Task is considered for the risk score calculation of a Remediation task.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Configuration Compliance features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

-   The **Reason** field in the Resolve modal has been removed for a remediation task in the classic UI, Vulnerability Manager Workspace, and IT Remediation Workspace.
-   The **Close** button has been removed for a remediation task, in the classic UI, Vulnerability Manager Workspace, and IT Remediation Workspace.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Configuration Compliance features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Configuration Compliance.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Install Configuration Compliance by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

Install Configuration Compliance by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Configuration Compliance we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Configuration Compliance we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Configuration Compliance, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Configuration Compliance we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Configuration Compliance we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Address security gaps in your enterprise environments detected through the Security Posture Control application by automatically prioritizing, assigning, and resolving them with the Configuration Compliance application workflow. The Security Posture Control application requires a separate subscription.
-   Analyze the overall impact of test results with summary visualizations of all or prefiltered active test results on the new Vulnerability Manager Workspace landing page.

 See [Configuration Compliance](https://www.servicenow.com/docs/access?context=vr-config-compliance-landing&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Reevaluate the risk score, assignments, remediation target date, exceptions, and remediation task for a set of test results in Vulnerability Manager Workspace.
-   View the percentage of CI compliance and test results compliance on a Test Group in Vulnerability Manager Workspace.

 See [Configuration Compliance](https://www.servicenow.com/docs/access?context=vr-config-compliance-landing&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   With the sn\_vulc.admin role, create remediation tasks manually in the Vulnerability Manager Workspace.
-   With the sn\_vulc.remediation\_owner role, create remediation tasks manually in the IT Remediation Workspace.

 See [Configuration Compliance](https://www.servicenow.com/docs/access?context=vr-config-compliance-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-washingtondc-yokohama/rn-combined-intro.md)

