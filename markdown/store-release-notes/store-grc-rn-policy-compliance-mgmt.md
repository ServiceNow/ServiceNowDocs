---
title: GRC: Policy and Compliance Management release notes
description: Version history for the GRC: Policy and Compliance Management on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-policy-compliance-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 16
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Policy and Compliance Management release notes

Version history for the GRC: Policy and Compliance Management on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.2 - June 2026 \(Australia\)**
    -   New:
        -   Enabled versioning support for Smart assessment-based Control attestation templates.
        -   Enabled Audit entries support for Control and Control objectives.
        -   Query range ACLs enhancements:
            -   Consistent access control — All tables include standardized query range security ACLs. These ACLs ensure that authenticated users with appropriate read permissions can query records consistently across the platform.
            -   Seamless upgrade experience — New query ACL rules are installed automatically during upgrade, with no administrator action required. Automated upgrade scripts handle the transition, including detecting and processing previously customized ACLs to ensure existing processes continue without interruption.
        -   Post-upgrade review for customized ACLs:
            -   If the instance includes administrator-modified query range ACLs, review those records after upgrade to confirm they align with the intended access policy.
    -   Changed:
        -   Email notification links for Policy and Compliance Management now redirect users to the appropriate workspace based on their access permissions.
        -   Added stale action reset logic to allow recovery and prevent blockage of the Item generation action queue.
    -   Fixed:
        -   The Supplemental guidance fields on controls are not updating with the latest changes from control objectives.
        -   Date formatting issue in the policy exception request system, where extension dates were not carrying over correctly from Employee portal to Native UI.
        -   Business rules using current.update\(\) which is not recommended.
        -   -   -   Security fix for ACL bypass in Policy related script included.
-   ACL added for Script field on Article template to mitigate vulnerability concerns.
-   Item generation action queue processor job sets incorrect processing duration in the action event queue table.
-   Citation to control records were being created in Citation to control table even for empty references
-   Non-admin users are unable to create indicators on controls
-   After closure the IRM issue source changes to AD-HOC
-   Policy Exception Extension "Restart workflow" business rule is erroring out
-   Duplicate risk statements are showing in control objectives related list
-   Ackowledgements are getting created on the next day of the first ackowledgement date on the policy.
-   Policy Exception Server‑Side validation enforces default 30‑day limit
-   **Version 22.0.2 - March 2026**
    -   New:
        -   Workflow introduced on control objectives \(on Workspaces only; necessary changes for the items below done in Policy and Compliance Management\):
            -   Major and minor updates can be done on a separate record instead of the current active record.
            -   Owners and owning groups added on control objectives.
            -   Dynamic approvals enabled.
            -   Auto-publish of control objectives based on the Effective date
            -   Workflows/reports updated to exclude working drafts.
            -   All control objectives will have a record nature as the current version, and active ones will be published by default.
            -   On classic UI, users will see a message to navigate to Workspaces for using the workflow.
    -   Changed: Minor update done on a control objective will not move a control back to draft \(on Workspaces only\)
    -   Fixed:
        -   When issues are manually created and controls are tagged, the first control status remains compliant or empty, while the rest move to non-compliant.
        -   Published Compliance policy reverts to Review state when updated with a new Valid to date.
        -   Invalid ATF step update content appears in installation logs for GRC: Policy and Compliance Management.
        -   Duplicate Indicator tasks generated on indicator template updates.
        -   Error occurs when raising an Exception to a policy.
        -   Schedule job "set\_attestation\_frequency" triggers text index event influx.
        -   Compliance score remains 100% despite minor non-compliance.
        -   Failure in notifying Control Attestors through email for Attestations.
        -   Horizontal privilege escalation via Related list API.
-   **Version 21.1.3 - December 2025 \(Zurich\)**
    -   New:
        -   Introduction of the ability to associate controls to citations.
        -   Reflection of the compliance score on citations and authority documents based on the associated controls to citations.
        -   Enhanced reports on citation and authority documents overview pages to consider the associated citations to controls.
        -   Enhanced reports on the Compliance homepage to consider the associated citations to controls.
        -   Auto-populated citation to control associations on upgrade.
        -   On Policy exceptions, approvers can now review important details for the exception before approving or rejecting a Policy exception and a Policy exception extension in a pop-up.
        -   For manual indicators, the system will not create new indicator tasks if the control is marked exempt or is within a policy exception period.
        -   Control objective requirements are available for control objectives and control requirements for controls.
        -   Lifecycle users on objects will follow the Entity-based access permissions defined.
        -   GRC choices across the product can now be activated and deactivated with the new active field on the GRC choice table.
    -   Fixed:
        -   Revisited the dependency on the System Administrator for functional use cases and ensured only functional roles are assigned appropriately.
        -   Tracking license for Policy exception approvers using dynamic approvals.
        -   Support for enforcement of security when adding or updating records in related lists through the Multi Record Associator.
        -   The associated issue was not closed when a control is retired.
        -   GRC Business User Lite could not view Issues or Policy Exceptions where they were added to the Watch List.
        -   High memory consumption due to a job which populates homepage data.
        -   Security fixes for inadequate access control on tables.
        -   Mapping controls to a policy exception in the Review state.
        -   Smart Attestation flow on controls did not trigger with automation.
        -   Unable to request policy exception extension.
        -   Wrong sys\_ui\_message entries for Widget titles in the Compliance dashboard.
        -   Controls with incomplete issues were moving back to the Compliant state.
        -   Smart Assessment Engine, Copy of Default Template "GRC Attestation" could be published.
        -   Policy reference field was fetching all policies when trying to create a new policy exception record through the issue related list.
        -   Control attestations were visible on the Employee Center without a defined role.
-   **Version 21.0.3 - September 2025**
    -   New: Indexed source support has been added for Controls.
    -   Fixed: The following issues have been resolved:
        -   Policy exception approvals were being approved even when the required risk rating was missing.
        -   GRC Employee users were unable to accept assigned policy acknowledgements in the UI16 interface.
        -   On Washington and earlier glide version instances, both workflow and Flow Designer flows were being triggered for policy exceptions.
-   **Version 21.0.2 - August 2025**
    -   New:
        -   Policy exception extension approval using GRC Approval Configurator.
        -   Policy exception approval using GRC Approval Configurator.
        -   Feature roles supported on Policy and Compliance Management tables.
        -   Automated application of entity based access on newly created objects for tables where entity based access is already enabled \(available from the Yokohama platform onwards\).
    -   Changed: Updated control attestation to support the replacement of multi-select field 'Assessment template categories' with a single select field 'Purpose' on Smart Assessment templates.
    -   Fixed:
        -   Updated the reference qualifier for the Approver field on the Policy table to accommodate lite operators during the approval process.
        -   Resolved cross-scope issues in the functional domain scheduled job.
        -   Fixed issue where the GRC Business User Lite role was unable to open the request extension popup.
        -   Fixed localization issues.
        -   Resolved issue where Compliance Manager, GRC Business User, and GRC Business User Lite roles could not update the Description field on a Policy Exception.
        -   Fixed Query Range ACL error on the Control Objective overview page.
        -   Fixed Accessibility issues.
        -   Resolved issue where control records were not properly updated when a Smart Assessment Control Attestation was cancelled.
        -   Fixed validation issue with the Valid to field on the Policy form.
        -   Resolved issue where users were unable to Return to Draft controls in the Monitor state if they lacked access to all entities.
        -   Corrected the activity log to show the last approver's name in the Approved by comment instead of the first approver for a policy record.
        -   Fixed issue in GRC where the Group Issue By functionality did not create new parent issues or reactivate previously deactivated ones.
        -   Resolved issue where the Request Approval button for Policy Exceptions in the New state was unresponsive for GRC Business User Lite.
        -   Fixed KB link issue in Policy Acknowledgement through Employee Center where the KB could not be found despite being published.
        -   Resolved error message invalid value on the update when rejecting a policy exception.
        -   Fixed issue where indicators of type Basic did not function as expected when domain separation was enabled.
        -   Corrected default value application for the Sample Size column on the Indicator table.
-   **Version 20.2.0 - June 2025**

    New: Added query-range ACLs for policy exception and policy related tables.

-   **Version 20.1.3 - May 2025**
    -   New: Entity based access enabled for Controls, Attestations, Policy exception to control \(Yokohama Patch 2+\)
    -   Changed:
        -   Security attributes introduced to replace scripts in applicable ACLs
        -   Supporting changes for Knowledge management workflow to flow migration on Governance, Risk, and Compliance knowledge base and on publish and retire flows for KB article for a policy
    -   Fixed:
        -   Policy record gets stuck in an irrecoverable "Awaiting approval" State when the last approval is granted at or after the first acknowledgment date
        -   Policy Exception records are closing automatically before valid to-date
        -   Smart Attestations are not generating for controls
        -   Accessibility and reflow issues on Authority Document and Citations Overview and Sidebar
        -   ACL bypass via the 'Request Extension' Service Portal Widget
        -   Policy review flow to be run as Compliance Admin instead of System
        -   Missing report view ACLs for tables
        -   ACL Bypass via "questionnaire\_view" UI Macro
        -   Non-admin users are unable to publish the policy because the 'Request Approval' button is not functioning.
        -   The field "valid to" date is showing the wrong message on the Policy form
        -   On clicking the Import Policy Text UI action - Images do not render and there are misalignments \(Xanadu Patch 7, Yokohama Patch 1\)
        -   The details field is missing in the Attestation designer after Xanadu Upgrade \( Xanadu Patch 8, Yokohama Patch 2\)
        -   Re-publishing the Policy is showing empty "Revised by" in Policy and Compliance \(Xanadu Patch 7, Yokohama Patch 1\)
    -   Removed: The sys\_db\_object payload files shipped which were overwriting customizations on sn\_compliance\_control sys\_db\_object entry
-   **Version 20.0.4 - February 2025**
    -   New:
        -   Compliance score rollup on entity hierarchy
        -   Performance improvements in Compliance scoring
        -   Enable or disable redlining document text sync by default through a property
        -   Trigger control attestations based on the created or updated date of the last completed attestation
    -   Changed: Attestation frequency introduced on control
    -   Fixed:
        -   Policy approval showing the system user as the user who approved the record in the activity stream
        -   Description of Policy exception record's Overview tab in Workspace shows the details from the "Justification" field
        -   Accept and Reject buttons do not appear in policy acknowledgment on the Employee Center
        -   Control name and control description get cleared when linked to the control objective, even when the Inherit from control objective option is unchecked
        -   Broken images on knowledge articles created from policies for the users who do not have access to the policy
        -   Localisation issues on the dashboard
        -   Most non-compliant entities report on the Authority document overview page that it is not loading data \(Workspace\)
        -   Auto-navigation to the Overview tab on a policy after actions on the policy text tab \(Workspace\)
        -   Most non-compliant entities report on the Authority document overview page that it is not loading data \(Workspace\)
-   **Version 19.1.1 - November 2024**
    -   Changed: Security fixes
    -   Fixed:
        -   Policy exception date validations
        -   Policy exception should be closed after valid to date
        -   When connecting a policy to cloud document, fixed folder location validations
        -   Control attestation should be visible to the compliance user before it is submitted
        -   Issue should be created when an indicator task is failed
-   **Version 19.0.2 - August 2024**
    -   New: Support for the Cyber Risk Institute \(CRI\) accelerator. Ability to map CRI assessment questions to control objectives. Perform CRI assessments on entities and create controls based on assessment responses. Evaluate the control compliance status based on the assessment response.
    -   Changed:
        -   When authoring policies, enable users to collaborate on policy text by connecting Google documents to the policy.
        -   When authoring policies, enable collaboration on SharePoint.
        -   Migrated workflows to flow designer.
    -   Fixed:
        -   Attestation is not getting canceled when control is moved to a draft or retired state.
        -   When the attestation template is updated on the control objective, the attestation on the associated control should be updated.
        -   Users with compliance admin roles should be able to create attestation templates. Included attestation creator role in the compliance admin role.
        -   Incorrect entity name displayed on control attestations.
        -   When a policy exception is canceled, associated task SLAs should be canceled.
-   **Version 18.1.4 - June 2024**

    New: Migrated classic dashboards to the Analytics workspace.

-   **Version 18.0.2 - February 2024**
    -   New:
        -   Managing documents on Microsoft OneDrive.
        -   Policy authoring on Google Drive.
    -   Changed:
        -   Dynamic approvals for policies.
        -   Parallel processing for indicators to reduce overall run time.
    -   Fixed:
        -   The duplicate Add button is displayed while configuring new relationships for control objectives.
        -   Standard control is not retired when an entity is added to an entity type associated with a common control if the control is active.
        -   Document redlining does not grant access to cloud documents.
        -   Controls do not automatically copy the supplemental guidance from control objective to the associated controls.
        -   Active indicator tasks should be cancelled when the indicator is retired.
        -   Indicators become active even when indicator templates are inactive.
        -   When a retired control moved back to draft, an indicator is not generated even if indicator template is already active.
-   **Version 17.0.1 - August 2023**
    -   Changed: Ability to see knowledge articles on employee center.
    -   Fixed:
        -   New Button is not coming up in the downstream controls related list on entities
        -   Confidential records are listed on service portal for users who created them but don't have access.
        -   When policy is deleted, control objectives are made inactive.
        -   Data retention policies for attestations.
        -   Users with business user and business user lite role are not able to read authority documents and citations.
        -   Not able to extend exception for already granted exceptions.
-   **Version 16.0.3 - February 2023**
    -   New:
        -   Ability to create Common controls and associate Reliant entities.
        -   Ability to associate multiple Policies/Authority Documents/Control objectives/Controls to one issue and vice-versa.
    -   Changed:
        -   Support for Localization
        -   Access controls for viewing reports
        -   Support for Accessibility standards
    -   Fixed:
        -   Business users and lite users are able to update the approval group and approver for Policy Exception.
        -   Indicators do not get re-activated on activating Controls.
        -   The control status is not changing to compliant when the indicator result is passed.
        -   Policy exception creation does not populate related fields automatically.
        -   Error handling for missing Approval rule when "Request additional approval" on Policy exception with source as Policy.
        -   On Authority Document, the error message 'Valid To date cannot be in the past' that is always shown, even when the field is not filled in.
        -   Lite users are not able to request an extension of Policy exception from the Risk Portal.
        -   When creating a Control from Control Objective form, Control is created without Entity.
        -   When the policy exception requester and the impacted control owner are the same, then don't send approval to the control owner but send approvals only to the requester's manager.
        -   On Service Portal, the Policy Acknowledgement widget displays the date in the incorrect format.
        -   Access controls for viewing reports.
-   **Version 15.0.3 - December 2022**
    -   Fixed:
        -   Migrating the policy exception table causes the application installation to take a long time. Added a column to store Impacted controls during migration instead of changing existing column type.
        -   Reduction in installation size of the application.
-   **Version 15.0.1 - August 2022**
    -   New:
        -   Perform Advanced Risk Assessments on Policy Exceptions.
        -   Categorize Compliance Objects like Policies, Authority Documents, Control Objectives, Citations, Controls etc.. based on Functional Domain like IT Compliance and Risk, Privacy etc..
        -   Compliance Manager/Compliance Analyst should be able to reuse existing Evidences collected on other GRC objects.
    -   Changed:
        -   Role hierarchy changes : GRC Reader role will not be part of Business User role. Changed all the ACL's, Modules etc.. accordingly.
        -   Added Expired substate for Closed Policy Exceptions to indicate Policy Exceotion is Approved and Valid to date is crossed.
        -   Reason code can be modified after Policy Exception is Approved.
        -   Policy Exceptions submitted from Service Portal or Employee Service Center should go through Verification Approvals when Verification Rule is configured.
        -   Requester should be able to extend Policy Exception more than once based on a configuration property.
    -   Fixed:
        -   Localization issues
        -   Incorrect due date on Policy Acknowledgements
        -   Manually Retired controls are moved to Draft state when Policy is published.
        -   States in which Controls is considered to be Active.
        -   On Impacted Controls for Policy Exceptions : Add/Add all buttons are not coming up
        -   On Controls, Open Issues is not updated when a new issue is created.
        -   Policy Exception is created even though Valid from and Valid to dates are same.
        -   GRC Business user is able to move the policy exception to analyze state even though verification approvals are configured.
        -   Description of auto created Policy exception created from PACE exception is truncated
        -   Retire button should not be present on the KB article related to Policy.
-   **Version 14.2.0 - May 2022**

    Fixed: The issue in the Policy Exception form where "Add all" button sometimes adds duplicate controls.

-   **Version 14.1.3 - March 2022**
    -   New:
        -   Generic Integration Framework to map any objects to control objectives and generate controls based on the configuration.
        -   Security changes
        -   Users will be able to create Issues, Exceptions, Acknowledge Policies, etc. from Employee Service Center.
    -   Changed:
        -   Allow multiple controls for the same combination of Entity and Control Objective.
        -   Policy Exception changes: Add impacted controls from different control objectives.
        -   Scripted APIs to create/update Policy Exceptions.
        -   Security changes
    -   Fixed:
        -   Policy Exception substate becomes invalid on ""Request Extension"".
        -   Activating a Policy creates controls for control objectives which have the ""Create Controls automatically"" flag set to false.
        -   Policy Exception Add Impacted Controls breaks with Request too large.
        -   Date format issues when creating policy acknowledgments.
        -   When attestations are grouped, the field 'Taken on' is not populated on child attestations.
-   **Version 13.1.1 - November 2021**
    -   New:
        -   Added field to capture Supplemental Guidance on Citations.
        -   Users should not edit the Citations imported from GRI/SASB content packs. Added logic to make all fields on Citation form read only when source is GRI or SASB.
-   **Version 13.0.3 - September 2021**
    -   New:
        -   Added support for Workspaces
        -   Added a new feature where you cannot reactivate controls if the controls were retired manually. This feature is applicable even if the related entity, entity type or control objective is reactivated.
    -   Changed: Control generation end to end flow
    -   Fixed:
        -   Attestation shows an entity name but does not change after entity name is changed
        -   On Issues, Planned end date is not correctly populated when planned start date is changed
        -   Policy exception is not approved when Policy is not associated
        -   Policy Review workflow updates the Policy back to the Review/Draft state before the 'Valid to' date
        -   When a Retired control is moved 'Back to Draft' and saved, it is getting Retired again
        -   Control owner field not dependent on owning group field
        -   Policy Acknowledgement exceptions - date fields issues on Safari browser
        -   Policy Acknowledgement performance issues
-   **Version 12.0.4 - June 2021**
    -   Changed:
        -   Modified Policy Acknowledgement Submit/Cancel transactions to background jobs to handle performance issues.
        -   Modified the flow to add users to Policy Acknowledgement Audience.
    -   Fixed: Security issues
-   **Version 12.0.1 - March 2021**
    -   New: Support for GRC Workspaces
    -   Changed: Updates to Policy Acknowledgements
    -   Fixed: Policy exception Upgrade script issues, Item Generation issues.
-   **Version 11.1.0 - November 2020**

    Fixed: Policy Exceptions upgrade scenarios

-   **Version 11.0.2 - October 2020**

    New: Knowledge Base \(KB\) article versioning \(requires Quebec platform\)

-   **Version 10.1.2 - June 2020**

    New: Improved policy exception workflow with tight integration to Vulnerability Response to seamlessly execute an exception within that application.

-   **Version 10.0.0 - March 2020**
    -   New: Additional Automated Test Framework quick start tests were added
    -   Fixed: Minor bugs
-   **Version 9.0.4 - November 2019**

    This application was updated in New York. See the section Supporting Links &amp; Docs for release notes and product documentation.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

