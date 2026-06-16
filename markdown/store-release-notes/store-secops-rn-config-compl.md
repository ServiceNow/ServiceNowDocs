---
title: Configuration Compliance release notes
description: Version history for the Security Operations Configuration Compliance application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-config-compl.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 22
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Configuration Compliance release notes

Version history for the Security Operations Configuration Compliance application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.6.0 - June 2026 \(USEM\)**
    -   New:
        -   Added configurable uniqueness for Tenable compliance tests, allowing administrators to control how test results are identified and preventing unintended overwrites.
        -   Extended the split test results framework to support Tenable compliance integrations.
        -   IT Remediation Owners can now manually create Remediation Tasks directly from the Security Exposure Management workspace list view in Configuration Compliance.
        -   Added out-of-the-box query range access control lists \(ACLs\) to strengthen data access security in the Configuration Compliance application.
    -   Changed:
        -   TheCreate Change andLink Change Request actions now automatically activate or deactivate based on ITSM Advanced plugin availability.
        -   Improved the Exception Management experience, including risk reduction workflows and questionnaires.
    -   Fixed:
        -   Fixed issues that could generate duplicate Remediation Tasks during task splitting, vulnerable item reopening, task rejection, task reopening from an Under Investigation state, and single-finding scenarios.
        -   Fixed an issue where manually created Remediation Tasks without associated findings could remain stuck in a Resolved state and could not be closed.
        -   Fixed an issue where the approvers list on Vulnerability Response exception rules did not refresh correctly after an extension request, which could result in duplicate email notifications.
        -   Fixed an issue that could generate duplicate approval records when requesting an extension for a Configuration Test Result exception rule.
        -   Fixed an issue where delegated approvers could not view the vulnerable items associated with their approval assignments.
        -   Fixed email notification issues that could trigger duplicate emails during scheduled updates to auto-exception rules.
        -   Fixed an issue where Change Requests could not be created from Remediation Tasks when the user session date format used day-first ordering \(dd/mm/yyyy or dd-mm-yyyy\).
        -   Fixed an issue that could cause post-integration jobs for Configuration Compliance to fail with a script error.
        -   Reduced excessive text indexing on large Vulnerability Response tables during upgrades to newer platform versions.
-   **Version 30.5.6 - June 2026 \(USEM\)**
    -   New:
        -   Configurable uniqueness for Tenable compliance tests, giving administrators control over how test results are identified to prevent unintended overwrites.
        -   Extended the split test results framework to support Tenable compliance integrations.
        -   IT Remediation Owners can now manually create a Remediation Task directly from the Security Exposure Management workspace list view in Configuration Compliance.
        -   Added out-of-the-box query range access controls lists for the Configuration Compliance app to harden security against unauthorized data exposure.
    -   Changed:
        -   TheCreate Change Request andLink Change Request actions now automatically activate or deactivate based on ITSM Advanced plugin availability.
        -   Updated Smart Assessment versioning for Configuration Compliance questionnaires, with improved version handling and reapply behavior.
        -   Improved the Exception Management flow, including the risk reduction path and questionnaire experience.
    -   Fixed:
        -   Eliminated duplicate Remediation Tasks created during task splitting, vulnerable item reopening, rejection or reopening of tasks under investigation, and single-finding scenarios.
        -   Manually created Remediation Tasks with no associated findings can now be closed correctly instead of remaining stuck in a Resolved state.
        -   The approvers list on Vulnerability Response exception rules now refreshes correctly after an extension request, and duplicate emails are no longer sent.
        -   Fixed duplicate approval records generated when requesting an extension on a Configuration Test Result exception rule.
        -   Delegated approvers can now view the vulnerable items mapped to their approval responsibility.
        -   Resolved email notification defects including repeated emails triggered by scheduled-job updates on auto exception rules.
        -   Fixed errors creating Change Requests from Remediation Tasks when the user's session date format uses day-first ordering \(dd/mm/yyyy or dd-mm-yyyy\).
        -   Fixed post-integration jobs failing on Configuration Compliance with a script error.
        -   Reduced excessive text indexing on large Vulnerability Response tables when upgrading to newer platform versions.
-   **Version 15.9.0 - June 2026**
    -   New:
        -   Added query-level access controls to strengthen record visibility and security within the Configuration Compliance application.
        -   Added read-only field protections to support compliance with Australia Security Directive requirements.
    -   Fixed:
        -   Resolved an issue where custom date formats configured in system properties were not honored when extending auto-exception rules, preventing exception extension requests from advancing to In Review.
        -   Fixed an issue that could generate duplicate Remediation Tasks when a Configuration Test Result was reopened with auto-defer enabled.
        -   Fixed an issue where reopening a resolved Remediation Task did not reopen its associated resolved Test Results.
        -   Fixed an issue that could generate duplicate approval records when requesting an extension for a Configuration Test Result exception rule.
        -   Fixed an issue where the Remediation Status on Configuration Test Results could unexpectedly change between states.
-   **Version 30.3.4 - April 2026 \(USEM\)**
    -   New:
        -   Added configurable uniqueness keys for compliance test ingestion to prevent results from being overwritten when multiple tests share the same control identifier.
        -   Added system property management to the Advanced Settings page in the workspace.
        -   Added a Users and Groups list view to the workspace Admin console.
        -   Added support for mapping a single finding to a single remediation task for more granular tracking and remediation.
    -   Changed:
        -   Updated bulk deferral to validate that selected items are not already deferred, preventing duplicate actions and unintended field updates.
        -   Improved exception management in the risk reduction and questionnaire workflow.
        -   Updated remediation plans to display plan details after submission.
        -   Updated the Advanced Settings page to display error message notifications.
    -   Fixed:
        -   Fixed custom date formats \(for example, MM‑dd‑yyyy, dd/MM/yyyy\) not being processed when requesting exception rule extensions or creating changes from remediation tasks.
        -   Fixed remediation status on compliance test results incorrectly changing when no actual result update occurred.
        -   Fixed duplicate compliance integration records being created during instance deployment.
        -   Fixed remediation task rules incorrectly setting the assignment type to Manual instead of Rule.
        -   Fixed theOpened by field appearing empty on remediation tasks created from the workspace.
        -   Fixed duplicate remediation tasks being created for single findings, including after exception rejection or reopening.
        -   Fixed theUnassign action not appearing for remediation owners with the appropriate role.
        -   Fixed approval records not transitioning to the correct state when multiple deferrals targeted the same item.
        -   Fixed approval rules failing after upgrade due to missing migration of custom exception rule substates.
        -   Fixed excessive background jobs triggered by work note updates on test result groups, improving performance.
        -   Improved platform stability and performance, including faster daily collection jobs, optimized auto‑close and rollup queries, and unblocked task rule processing during data ingestion.
        -   Fixed duplicate search buttons on theAssigned To field in the remediation task change creation form.
-   **Version 15.7.3 - April 2026**
    -   New: Added configurable uniqueness keys for compliance test ingestion to prevent results from being overwritten when multiple tests share the same control identifier.
    -   Changed: Improved exception management in the risk reduction and questionnaire workflow.
    -   Fixed:
        -   Fixed custom date formats \(for example, MM‑dd‑yyyy, dd/MM/yyyy\) not being processed when requesting exception rule extensions or creating changes from remediation tasks.
        -   Fixed delegated approvers being unable to view mapped vulnerability items due to permission restrictions.
        -   Fixed remediation status on compliance test results incorrectly changing when no actual result update occurred.
        -   Fixed remediation task rules incorrectly setting the assignment type toManual instead ofRule when populated by a rule.
        -   Fixed theOpened by field appearing empty on remediation tasks created from the workspace.
        -   Fixed duplicate remediation tasks being created for single findings, including after exception rejection or reopening.
        -   Fixed vulnerability items remaining in theDeferred state after exception rule deletion instead of reverting to their original state.
        -   Fixed vulnerability items not closing after detections were closed when exception rule references were not properly cleared.
        -   Fixed repeated approval notification emails triggered by scheduled job updates on auto‑exception rules.
        -   Fixed duplicate search buttons appearing on theAssigned To field in the remediation task change creation form.
        -   Fixed questionnaire attachments not being visible even when the questionnaire was populated.
        -   Improved performance of the unified daily collection job and rollup queries.
-   **Version 15.6.1 - January 2026**

    Minor fixes for this release.

-   **Version 30.2.3 - January 2026 \(USEM\)**

    Minor fixes for this release.

-   **Version 15.5.3 - December 2025**
    -   New:
        -   Introduced dynamic recalculation of Remediation Target \(RT\) dates when a finding’s risk rating changes. Administrators can configure recalculation rules to keep RT dates accurate and aligned with the latest risk updates, ensuring consistent and reliable SLA tracking.
        -   Added support for sn\_vul.add\_policy\_as\_key in Qualys integration:
            -   Applies to all existing users with fewer than 500K active Test Results.
            -   Applies to all new users with Qualys integration setups.
    -   Fixed:
        -   Resolved an issue where Remediation Tasks were reopening from Resolved to Under Investigation even when associated Test Results were not reopening.
        -   Prevented Test Results from reopening from False Positive when the scanner reported the test as Failed.
        -   Corrected a state rollup issue that moved Remediation Tasks from Resolved to Under Investigation after an integration run.
        -   Corrected behaviour where the Reapply flag was incorrectly set to Y when assignment rule updates were aborted, the flag now remains unchanged as intended.
        -   Improved handling of Reapply flag and assignment rule conditions.
        -   Removed creation of duplicate Remediation Tasks during split operations.
        -   Corrected deferred Test Result Groups incorrectly moving to Closed after the deferral period expired.
-   **Version 15.4.8 - September 2025**
    -   Fixed:
        -   The Reopen UI action is now compatible with the upgraded plugin \(V15.3.3\), ensuring proper functionality when reopening compliance records.
        -   Justification notes from Configuration Compliance remediation task exception requests are now correctly populated into corresponding fields in change approval records.
        -   The system now correctly identifies and processes relevant approval states, preserving unaffected approvals during workflow changes.
        -   Configuration Compliance remediation tasks now return to their previous state when level two approvals are cancelled, instead of being set to "Deferred".
        -   Compliance test results now accurately reflect the status of CIs. Results stay closed for retired or decommissioned CIs, and reopen automatically with new scanner results if the CI is reactivated.
-   **Version 15.4.3 - August 2025**
    -   Changed:
        -   CTR Granularity Configuration: You can now configure the granularity of Configuration Test Results \(CTR\) in Configuration Compliance. For example, if a database has five instances, the system generates five distinct test results one per instance offering improved visibility and flexibility in patch tracking.
        -   Refined State Management Logic: State roll-down from remediation tasks \(RTs\) to findings and roll-up from findings to RTs has been improved across all modules. Enhancements include better handling of mixed states \(e.g. Deferred and Closed\), support for closing tasks in sub-states like In-Review, and reopening based on the Assigned To field. False Positive transitions now align with scanner results as the source of truth, reducing manual effort and clarifying task ownership.
-   **Version 15.3.4 - June 2025**

    Fixed: The scheduled job Rollup test result values to remediation task and configuration test will check the status of the previous background job before starting a new one.

-   **Version 15.3.3 - May 2025**
    -   New:
        -   You can now configure advanced questionnaires as part of the exception management process using Smart Assessment. This improvement allows remediation owners to provide detailed context for exception requests and enables approvers to configure conditional questions to gather the right information needed for informed decision-making.
        -   If a questionnaire is marked as mandatory, the test results or remediation tasks remain in the 'Open' state until the questionnaire is completed and submitted. If the questionnaire is incomplete, the state change approval record is saved as 'Draft'. Only after completing the questionnaire can the user submit the exception request, which will then move the test result or remediation task to the 'In Review' state.
    -   Fixed:
        -   The creation of duplicate jobs for auto-close rules.
        -   When the deferral period for remediation tasks expires, the test result state does not revert to Open from Passed.
-   **Version 15.2.6 - March 2025**

    Fixed: An issue where the Request Extension functionality in version 25.0.4 in the Classic UI. The feature is now working as expected.

-   **Version 15.2.5 - February 2025**
    -   New: Introduced the ability to manually create Remediation Tasks \(RTs\) in the List View of Vulnerability Manager and IT Remediation Workspaces.
    -   Fixed:
        -   The 'sn\_sec\_cmn.risk\_score\_changes\_add\_worknote' system property has been introduced. When enabled, it populates the updated risk score calculation details in the work notes.
        -   A Remediation owner can now add work notes for the test results assigned to them.
        -   Resolved state management issues: The UI actions and validations in the Remediation Task form now align consistently with the current state.
        -   Now, a Remediation Owner can open and view the Vulnerability Entry records in the IT Remediation Workspace without a 403 error.
        -   An intermittent issue related to dates on the Request Exception modal, which was preventing the submission, has now been fixed.
        -   The issue where a rejection in the State Change Approval \(Exception Request\) incorrectly marked the rejected approval record as 'No Longer Required' has been resolved.
        -   Now, the Impacted CIs widget on the Home page of the IT Remediation Workspace is displayed properly.
-   **Version 15.1.6 - December 2024**
    -   Changed: When you select the Request Extension button to extend an exception rule, you have the option to extend both the deferred until date' and the exception rule valid to' date.
    -   Fixed: Tags added to the test results are displayed in the workspace list view if a tag is associated with it, and the Tags column is included in the list view.
-   **Version 15.1.5 - November 2024**
    -   New:
        -   Granular Role-based access control: Enhanced the role management in Vulnerability Manager Workspace \(for watch topics and lists\) and IT Remediation Workspace \(for lists\). This enables precise access control and configuration tailored to specific user roles. CC Analysts can now create watch topics.
        -   Workspace search: Efficiently search using the record numbers and open the records in either the Vulnerability Manager Workspace or IT Remediation Workspace, depending on your assigned role.
        -   Navigating to Workspaces from the All menu: If the 'sn\_vul\_cmn\_ws.navigate\_to\_workspace' system property is enabled, selecting predefined filter links in the Configuration Compliance module from the 'All' menu will automatically open these links in the Vulnerability Manager Workspace and IT Remediation Workspace based on your role.
        -   Remediation target configuration: The Remediation target rules can now be configured in such a way that the remediation target is calculated based on the Last Opened' date, offering more flexibility in tracking the remediation progress.
        -   Customizable Age calculation: The Age and Age Closed calculations of a test result can now be customized so that they are calculated from a choice of available date fields. That is, you can now select any of the available date fields such as last found, created, etc. with reference to which the Age and Age Closed values must be calculated. For more information on how to configure these age calculations, refer to the KB1703270 KB article.
        -   Refresh the Saved Filter visualizations: You can now refresh the visualizations for saved filters on the Vulnerability Manager Workspace Home page either once or daily. Additionally, you can manually update these visualizations on demand to reflect the latest data.
        -   Performance enhancement in the Workspaces: The glide.ui.list.seismic.omit.count' system property allows you to deactivate the record/row count display on the lists in the Vulnerability Manager Workspace and IT Remediation Workspace, optimizing performance for large datasets.
        -   You can now reevaluate the exception rules for a set of selected test results directly in the Vulnerability Manager Workspace instead of reevaluating these rules for all records in the classic UI.
        -   A new Properties module has been added to the navigation menu under the Administration section. This module enables direct modification of the flag values, offering a user-friendly method to manage and update system properties directly from the interface.
        -   Qualys Test Group/Policy reference from a Test Result and Test: By enabling a system property, the Test Group/Policy can be populated on a Test/Control and can be referenced from Test Result by dot walking to the Test. For additional guidance and prerequisites, see Qualys integration with Configuration Compliance and KB1644268 KB article.
    -   Fixed:
        -   Fixed the date-format issue for Test Result's Until and Resolution dates.
        -   The issue with log messages stating "Cannot read property 'assignment\_group' from null" after executing the Qualys PC Results Primary integration has been fixed.
-   **Version 15.0.1 - September 2024**

    Fixed: Test results in the "Deferred" state in remediation tasks will reopen after the remediation task's deferral time expires.

-   **Version 15.0.0 - August 2024**
    -   New:
        -   You can enable or disable the import of test results for a Qualys test group in the Vulnerability Manager Workspace.
        -   The % Test Result Compliance column in the Tests table displays the percentage of test results that are compliant with a test.
        -   The % Test Result Compliance column in the Test Groups table displays the percentage of test results that are compliant with all the tests of a test group.
        -   Every test is mapped with its test group for Microsoft Defender for Cloud Integration and Tenable integration.
        -   Added new columns in the Test Results table to support metrics calculation in parity with Vulnerability Response application.
        -   Starting with v23.0 of Vulnerability Response, you can now evaluate the assignments, remediation target dates, remediation tasks, and risk scores for specific test results in the Vulnerability Manager Workspace, instead of reapplying the rules for all test results in the classic UI.
        -   The Risk Score is now calculated for passed test results also.
    -   Changed:
        -   The Close button has been removed for a remediation task.
        -   When you resolve a remediation task, the resolution notes reflects in the work notes of all its test results.
    -   Fixed:
        -   Improvements to policy audits in the Security Posture Control application ensure that retired assets are not evaluated by activated policies. If the state of an asset transitions in test result and remediation tasks from Retired back to Active, it is included in the next policy evaluation.
        -   Renamed the Policies list to Test Groups in the Vulnerability Manager Workspace to maintain consistency with the classic UI.
        -   The Test Result Compliance percentage of a Configuration Item \(CI\) is now shown on its respective Discovered Item.
-   **Version 14.12.4 - May 2024**
    -   New:
        -   In the Vulnerability Manager and IT Remediation Workspaces, mark a Remediation Task as false positive with approval workflow.
        -   In the Vulnerability Manager and IT Remediation Workspaces, mark a subset of Test Results as false positive, by automatically creating a new Remediation Task with the selected Test Results and submitting for approval.
        -   Edit activated policies, save changes, publish, and exit edit mode with UI actions on policy records in the Security Posture Control application. Versions are tracked and version numbers are displayed on policy records and their related test results in Configuration Compliance.
        -   If you publish a new version of a policy or delete a policy in the Security Posture Control application, you have the option to close its existing related test results \(findings\). Test result and remediation task states transition in accordance with the state transition processes of the Configuration Compliance application.
    -   Changed: Remediation Target can be calculated from the Last Pass Date. When last pass date is empty, the remediation target is calculated from Created Date.
-   **Version 14.11.2 - February 2024**
    -   New:
        -   List modules from the navigation menu to open in the Vulnerability Manager workspace home page with auto-selection of the corresponding saved filter with enhanced user experience.
        -   Address security gaps in your enterprise environments detected through the Security Posture Control application and automatically prioritize, assign, and resolve them with the Configuration Compliance application workflow. The Security Posture Control application requires a separate subscription.
    -   Changed: Changes in the Test result and Remediation Task form for the workspace -Added the state details, updated reference links for configuration test, UI sections and Tab Title.
    -   Fixed:
        -   Fixed rename changes from test result group to remediation task for upgrade customers to version 14.9
        -   Resolution will not be cleared when we reopen the test results.
        -   Fixed date functions in OOTB client scripts when we use a hyphen as the separator.
        -   Risk rating of the test result changing to none when the test result marked as fixed.
        -   Fixed remediation target date time issue when the timezone is changed.
-   **Version 14.10.2 - November 2023**

    New: A deferred remediation task moves to its original state when the exception due date reaches the target date. As a remediation owner, you can now request extension for a deferred remediation task by clicking Request Extension.

-   **Version 14.9.3 - October 2023 \(Vancouver\)**

    Fixed: Remediation Status on a test result will be set upon AutoClose.

-   **Version 14.9.2 - August 2023 \(Vancouver\)**
    -   New:
        -   The Last Pass field is captured for the Test Results.
        -   Implemented split task, request exception and create change for configuration compliance remediation tasks in the workspaces.
    -   Changed:
        -   Test Result Group has been renamed to Remediation Task.
        -   When the configuration item associated with a discovered item changes, the configuration item on the passed test results associated with the discovered item also changes now.
    -   Fixed: Deferral Date and Deferred by fields will be populated when a Remediation task is deferred.
-   **Version 14.8.6 - June 2023**

    Fixed: For Advanced Risk Rule Calculators, the resulting risk score information in the sample scenarios was being populated with incomplete information. This issue has been fixed. The resulting risk score information is now correctly populated.

-   **Version 14.8.3 - May 2023**
    -   New: Introduced OOB table cleaner records on the test results and test result groups.
    -   Fixed: Integration processes were timing out after one hour, even if the import queue entry was still being processed. As a result, the integration run status was being updated as 'Error'. Starting from V14.8.2, timestamps \(heartbeats\) are sent periodically to indicate that the queue is alive and processing valid data.
-   **Version 14.7.5 - March 2023**
    -   Changed: The system property 'auto\_defer\_test\_result\_in\_active\_exception\_window' is now set to 'false' by default.
    -   Fixed: The Unassign button on test result groups was not working earlier. This has been fixed.
-   **Version 14.7.3 - February 2023**
    -   New:
        -   Added support for workspace for Configuration Compliance
        -   Added configuration for risk score to risk rating mapping
        -   Reduced dependency of Configuration Compliance on Vulnerability Response \(VR\). For native Cloud Security Posture Management \(CSPM\), VR is not required.
    -   Changed: The 'Policy' table is renamed to Test Group.
-   **Version 14.5.4 - November 2022**
    -   New: Two new Qualys Integrations for importing test results to Configuration Complaince with new sets of Qualys APIs: Qualys PCRS Policy Host Integration and Qualys PCRS Test Results Integration. You might see better performance with the new APIs.
    -   Changed:
        -   You might see performance improvements when running Assignment Rules and Remediation Target Rules.
        -   For Test Result Groups \(TRGs\) created from group rules, group rules are automatically reapplied when assignment rules are reapplied.
        -   On a test result record, choose a date in the data field to calculate the remediation target for resolution. The remediation target is based on the date you select.
-   **Version 14.3.5 - August 2022**
    -   New:
        -   With the Unassign UI action, remediation owners can remove their assignment from records that they determine are not their responsibility. The Unassign feature is available on Test result group \(TRG\) records. The Unassign UI action clears the Assigned to and Assignment group fields and sends notifications to admins in a daily digest that records are not assigned. Records updated with this feature are displayed on the Unassigned module for Configuration Compliance. A daily scheduled job counts the records that are updated and aggregates them by the assignment rules that initially assigned them. You can use the counts that are displayed for each assignment rule to help you monitor how effective your assignment rules are.
        -   Track the number of times a test result or a test result group is deferred in the Multiple deferrals module. A scheduled job, set deferral counts, runs daily to post counts for records that are deferred more than once in the Deferral count column in the Multiple deferrals module for Configuration Compliance.
-   **Version 14.0.1 - May 2022**

    New: Automatically close test results related to retired CIs: You can automatically close test results associated with retired configuration items. If the Configuration Management Database \(CMDB\) changes the life cycle stage status of the configuration item to retired, you can choose to automatically close the associated test results. Enable the system property sn\_vulc.auto\_close\_test\_results\_linked\_to\_retired\_CIs to auto-close TRs that are associated with retired CIs.

-   **Version 13.1.1 - March 2022**
    -   New:
        -   With the Auto-Close test results module, reduce the number of stale, failed test results in your environment.
        -   Use the flow designer instead of the workflow to approve exception requests for exception management, exception rules, and false positive management.
        -   Use exception rules to automatically defer new and existing test results that can't be remediated or deferred immediately.
        -   Use the Exception Management module to create a questionnaire to add to the exception request. This questionnaire provides a better understanding of the reason for requesting the exception.
        -   For Risk Calculators in Configuration Compliance generate risk scores by providing custom fields and weights to suit your requirement.
-   **Version 13.0.0 - February 2022**

    No new features or updates are included with this version. This version ensures that features from the last release are compatible with the San Diego family release.

-   **Version 12.2.1 - October 2021**

    New: Verify that your assets are in compliance with your policies and controls with imports from the Tenable.io product. The Tenable.io product in the Tenable Vulnerability Integration imports policies, controls \(test results\), and configuration tests for processing in the Configuration Compliance application.

-   **Version 12.1.3 - June 2021**
    -   New: The integration run record displays metrics and the duration of each stage of a run.
    -   Changed:
        -   Modifications to support the newly updated background job framework that ensures that jobs are executed in a resource-optimized manner.
        -   Modifed the scope of the events that are generated after an integration run is completed so they are compatible with any third-party scanner.
    -   Fixed:
        -   Performance issues with reapplying assignment rules and group rules.
        -   The Remediation target rule field is populated as expected.
-   **Version 12.0.1 - February 2021**

    The following list highlights the new features and updates to the application. For more details about these new features and updates, see the ServiceNow Store release notes and Configuration Compliance release notes links for your family release in the Supporting Links section on this page.

-   **Version 11.1.5 - November 2020**
    -   New:
        -   With remediation target rules, define the expected time frames for remediating test results and send status notifications to users and groups.
        -   Request to defer the remediation of test results or test result groups for a specified period. Request, review, and approve exception requests with an approval workflow consistent with Vulnerability Response.
        -   Use IRE to create new CIs in the CMDB when an existing CI cannot be matched with an imported host from third-party vulnerability assessment products.
-   **Version 11.0.0 - October 2020**

    New: Version 11.0.0 certified for Orlando and Paris.

-   **Version 10.3.3 - June 2020**
    -   New:
        -   Recertified for version 10.3.3.
        -   Risk rollup calculators have been added. View the most current risk scores and risk ratings on configuration tests and test result groups.
-   **Version 10.0.0 - March 2020**

    New: Recertified for Orlando.

-   **Version 9.0.1 - November 2019**
    -   New:
        -   Added Test Result Group Rules
        -   Added Assignment Rules
        -   Added remediation owner role \(contained in the itil role\)
-   **Version 8.0.9 - July 2019**

    Configuration Compliance exposes configuration-related security vulnerabilities of highest impact to business operations. It streamlines the remediation process across frequently-isolated information security, IT operations, and business process stakeholders.


