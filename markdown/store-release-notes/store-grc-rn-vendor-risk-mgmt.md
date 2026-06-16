---
title: GRC: Third-party Risk Management release notes
description: Version history for the GRC: Third-party Risk Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-vendor-risk-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 11
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Third-party Risk Management release notes

Version history for the GRC: Third-party Risk Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 22.3.3 - June 2026 \(Australia\)**
    -   New:
        -   Added Software Bill of Materials \(SBOM\) Smart Assessment template and automation rules.
        -   Added Now Assist response generation for Smart Assessment questionnaires.
        -   Added comment and work notes read access for vendor assessment reviewer role on Smart Assessment template categories.
    -   Changed:
        -   Enhanced role-based access controls by replacing GRC uber roles with feature-specific roles.
        -   Updated Smart Assessment template versioning to support template evolution and migration.
        -   Improved vendor risk scoring calculation to include assessment-level normalization for Smart Assessments.
    -   Fixed:
        -   Resolved usage analytics duplicate record creation \(PRB1967479\).
        -   Fixed reassignment filter issues for internal and external assessments \(PRB2020935\).
        -   Added table allowlist validation to prevent unauthorized access \(PRB1997560\).
        -   Fixed Smart Assessment template migration when TPRM Due Diligence not installed \(PRB2013668\).
        -   Corrected risk rating scale deletion during migration \(PRB2016123\).
        -   Fixed email notification trigger for internal assessment state changes \(PRB2016087\).
        -   Resolved SAE questionnaire setup errors with async business rules \(PRB2014774\).
        -   Corrected external assessment questionnaire due date calculation \(PRB2011825\).
        -   Fixed Smart Assessment count display in SVDP homepage for engagements \(PRB2008813\).
        -   Corrected assessment level normalization in risk rating calculations \(PRB1990558\).
        -   Fixed IRQ/tiering template scale reversal from classic to SAE \(PRB1998195\).
        -   Prevented editing of "Include previous responses" after draft state \(PRB2007197\).
        -   Filtered inactive metrics when copying assessment responses \(PRB2004261\).
        -   Fixed SAE assessment instance state when templates removed \(PRB2004521\).
        -   Corrected IRQ questionnaire validation for non-English customers \(PRB2000693\).
        -   Updated "Responses expected by" field on external assessments \(PRB1999504\).
        -   Enabled "Supports smart assessment" field for issue generation rules \(PRB1996346\).
        -   Updated ACL roles for issue-to-SAE questions \(PRB1996731\).
        -   Resolved duplicate audit creation in scoring rule updates \(PRB1992222\).
        -   Fixed missing audit entries for state changes in SAEUtilsBase \(PRB1994299\).
-   **Version 22.0.2 - March 2026**
    -   New:
        -   Assessments are now supported on TPRM element records.
        -   Assessments can be prefilled leveraging AI using the uploaded documents \(Innovation lab feature\).
        -   Sample assessment templates are made available through Unified Content Accelerator plugin.
    -   Fixed:
        -   SAE tiering emails have been corrected to include valid URLs.
        -   Inactive downstream suppliers not being removed when the SAE fourth‑party template is deleted has been resolved.
        -   Engagement level risk area widget not populating for Workspace has been resolved.
        -   Internal assessment's "Questionnaire due reminder" email being sent out with an empty Subject and empty Body has been resolved.
    -   Removed: Assessments using entities is no longer supported.
-   **Version 21.1.6 - December 2025**
    -   New:
        -   Risk area support for internal assessments.
        -   Document Management System integration to manage all vendor documents in one place with the ability to reference them across engagements as needed.
    -   Changes: Applicable table fields marked as read-only where updates from client scripts must not occur.
    -   Fixed:
        -   Issue generation rule was restricting the creation of more than one rule on the same questionnaire template even though different questions were being selected.
        -   SAE Template Copy Functionality was creating a record in TPRM Table instead of sn\_smart\_asmt\_template.
        -   Card borders were missing on Overview pages in Coral Dark theme.
        -   Assessor was not being notified after vendor submits an assessment.
        -   An issue with not being able to submit SIG detail assessment on the Smart assessment engine.
-   **Version 21.0.3 - August 2025**
    -   New: Third-party Risk Management has been updated to work with Smart Assessment Engine.
    -   Fixed:
        -   An issue where the TPRM code would always create an assessable record for core\_company when creating the assessment instances has been addressed.
        -   The incorrect logic for the computing rating in the case a user responded to all scoring questions as not applicable.
        -   Unwanted updates caused by the business rule: Display applicable risk scoring rule.
        -   An info message that was misleading when submitting a risk assessment to a third-party contact.
        -   An issue with multiple vendor portal widgets bypassing security ACLs has been addressed.
-   **Version 20.2.4 - August 2025**

    Fixed: Changes required to address several widgets on Vendor portal bypassing security ACL have been made.

-   **Version 20.2.2 - July 2025**

    Fixed: Added/updated ACLs to prevent query range access to unauthenticated users.

-   **Version 20.2.1 - June 2025**

    Fixed: Added/updated ACLs to prevent query range access to unauthenticated users.

-   **Version 20.1.1 - May 2025**
    -   Updates: Security updates have been made.
    -   Fixed:
        -   Accessibility issues have been addressed.
        -   i18n translation issues have been addressed.
        -   Vendor risk admin does not see questionnaire designer UI action.
        -   Import Questionnaire by Excel and get generated Questionnaire template should have Category name as case sensitive.
        -   Conflicting column name 'industry' on core\_company when customer\_account is installed has been handled.
-   **Version 20.0.1 - February 2025 \(Yokohama\)**
    -   New: Ability to copy the responses from a previously answered questionnaire \(within the same third-party\) to a new questionnaire of the same questionnaire template.
    -   Fixed:
    -   -   Incorrect translations for Simplified Chinese have been addressed.
-   Duplicate theme files getting created when Vendor Portal plugin repaired with customization in place have been addressed.
-   Issue generation failure for choice questions when dependent on multi-selection question has been addressed.
-   **Version 19.1.4 - February 2025 \(Xanadu\)**

    Fixed: After TPRM workflows have been migrated to flow designer, there was an issue with these workflows not being compatible on the Washington platform version. This issue has been addressed.

-   **Version 19.1.2 - November 2024**
    -   New: The Digital resilience third-party registers application now integrates with TPRM.
    -   Changed:
        -   Addressed accessibility gaps in TPRM workspace.
        -   Migrated the legacy tiering questionnaire reminder and external questionnaire reminder workflows to flow designer.
    -   Fixed:
        -   Corrected property access role requirement in the documentation.
        -   The scoring\_rule and scoring\_rule\_ref fields were being updated by a BR every time an engagement record was viewed.
        -   N/A should not be included automatically as a value when multi-select question responses are exported to excel.
        -   Fixed authorization issue in GlideRecord/GlideAggregate query string which provided excess access to low privilege.
        -   Fixed UX Screen Condition ACL to include script-level authorization.
        -   Fixed misconfiguration of ACLs that have no roles, no conditions, no script and no security attributes.
        -   Renamed the Privacy manager group to 'TPRM Privacy manager' to prevent conflict with the Privacy Management application group.
-   **Version 19.0.1 - August 2024**
    -   Fixed:
        -   Radio button selections not visible in Dark mode when viewing responses to a questionnaire.
        -   Controls were being prevented from becoming compliant after assessment instances got automatically cancelled when the assessment template changed.
        -   The SIG lite questionnaires were not available for selection when creating a new issue generation rule.
        -   The "Set default third-party tiering score" business rule was not performing as expected because its filter conditions was missing 'IRQ template' as a classification type.
        -   Third-party risk assessment work queue should not include 'Recalled' state.
        -   Cross Site Scripting \(XSS\) inside vendor portal excel import.
    -   New: Docs for visual data model of all tables that are core TPRM tables and how they are connected.
-   **Version 18.1.3 - June 2024**
    -   Fixed:
        -   Classification for SIG Core did not appear in TPRA Questionnaires.
        -   Fixed ACLs that did not require a role on tables:
            -   sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment
            -   sn\_vdr\_risk\_asmt\_ua\_activity
        -   Domain separation to work as expected for scheduled jobs relating to event-driven management.
        -   Domain separation to work as expected for scheduled jobs relating to repeating assessments.
    -   Deprecated legacy "Vendor Risk Dashboard".
        -   Dashboard will remain for existing customers.
        -   It will not be installed for new customers.
-   **Version 18.0.2 - February 2024**
    -   Changed:
        -   Starting in version 17.0.2, a new system property was added, sn\_svdp.allow\_assessor\_edit. The default setting for this property enables Third-party Risk Assessors \[sn\_vdr\_risk asmt.vendor\_assessor\] to answer questions or modify responses in third-party questionnaires. If you do not wish to use this functionality, please turn this property off.
        -   Starting in version 17.0.4, a new role was added \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\]. The new \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] role can create and edit questionnaire templates and contains all the permissions of the \[vendor\_risk \_manager\] and \[assessment\_admin\] roles. The permissions for creating and editing questionnaire templates have been removed from the \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\].
        -   Updated some usage of "vendor" to "third-party".
        -   Updated OOB views in Vendor Management Workspace to match corresponding pages in Classic View.
    -   Fixed:
        -   All Vendors list in Vendor Management workspace was not working if the Third-party Risk Management application was not installed.
        -   Scoring rule was not visible when viewing records on tables extended from Company table.
        -   Third-party Risk Assessments could move to state Generate Observations without all questionnaires being completed.
        -   Work Queue page was disabled if Third-party Risk Due Diligence application was not installed.
-   **Version 17.0.7 - January 2024**
    -   Corrected Vendor Portal dependency version to version 17.0.5.
    -   Starting in version 17.0.4, a new role was added \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\]. The new \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] role can create and edit questionnaire templates and contains all the permissions of the \[vendor\_risk \_manager\] and \[assessment\_admin\] roles. The permissions for creating and editing questionnaire templates have been removed from the \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\].
-   **Version 17.0.6 - November 2023**
    -   Fixed:
        -   Security update
        -   Removed unneeded ACLs on sys\_choice table
        -   View responses link showing up even if responses have not been returned by the third-party
        -   Removed warnings in logs when scores are overridden on assessments
    -   Changed:
        -   Starting in version 17.0.4, a new system property was added, sn\_svdp.allow\_assessor\_edit. The default setting for this property enables Third-party risk assessors \[sn\_vdr\_risk asmt.vendor\_assessor\] to answer questions or modify responses in third-party questionnaires. If you do not wish to use this functionality, please turn this property off.
        -   Starting in version 17.0.4, a new role was added \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\]. The new \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] role can create and edit questionnaire templates and contains all the permissions of the \[vendor\_risk \_manager\] and \[assessment\_admin\] roles. The permissions for creating and editing questionnaire templates have been removed from the \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\].
-   **Version 17.0.4 - August 2023**
    -   New:
        -   In version 17.x, Vendor Risk Management is renamed to Third-party Risk Management
        -   Support for Third-party Risk Due Diligence \(if applicable\)
        -   Added the ability to risk assess any record that extends core\_company table \(if the user has access to view that record\)
        -   A new role has been added. The new \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] role can create and edit questionnaire templates and contains all the permissions of the \[vendor\_risk \_manager\] and \[assessment\_admin\] roles. The permissions for creating and editing questionnaire templates have been removed from the \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\].
    -   Fixed:
        -   Updates to Choices in GRC Choice table getting overridden on upgrade
        -   Incorrect dates auto-populating the Vendor Risk Assessment schedule fields
        -   Incorrect calculation of category results with multiple selection questions
        -   Incorrect generation of Vendor Risk Assessment when no tier-based submission rules are defined
        -   Improved translations
    -   Changed: A new system property was added, sn\_svdp.allow\_assessor\_edit. The default setting for this property enables Third-party risk assessors \[sn\_vdr\_risk asmt.vendor\_assessor\] to answer questions or modify responses in third-party questionnaires. If you do not wish to use this functionality, please turn this property off.
    -   Removed: "Email" field for respondents to tiering assessments -- this was never meant to be on the form
-   **Version 16.0.3 - May 2023**

    Fixed: Issue where internal comments may get removed if a vendor contact changes their answer on multiple selection question types.

-   **Version 16.0.1 - February 2023**

    Fixed: Added report view ACLs to increase security on VRM tables

-   **Version 15.0.7 - August 2022**
    -   New: Added support for Third Party Scores to roll up in risk rating calculation
    -   Fixed:
        -   Inaccurate message sometimes seen on Vendor Risk Assessment page due to missing advanced risk plugin
        -   Missing translations in Risk Assessment Designer
        -   Improved translation support throughout application
        -   Risk area field and mapping fields could not be changed for single domain third-party provider services after it has been created
        -   Improved performance of saving Fourth-Party Questionnaires in Vendor Portal
        -   When vendor risk assessment is deleted, its issues and tasks are now moved to closed cancelled state
        -   Removed the incorrect role condition on Business Rule ""Copy vendor tiering to engagement"" as it was too restrictive
-   **Version 14.1.3 - March 2022**
    -   New: 4th-Party Management feature
    -   Fixed:
        -   An issue where some names caused ESignatures to fail was fixed
        -   Minor WCAG 2.1 fixes
-   **Version 13.0.1 - September 2021**
    -   Fixed:
        -   Prevent inactive questionnaires from sending email notifications when adding to an assessment
        -   Corrected issue where some questions in vendor portal show incorrectly as not answered
        -   Fixed broken ATF step
        -   Added Accessibility features
        -   Improved support for different translations
        -   Improved security of application packages and demo data
-   **Version 12.0.2 - June 2021**
    -   New:
        -   VRM assessment engine changes:
            -   Updated multiple selection score calculation and option values
            -   Added support for a reference list in multiple selection data types
            -   Added display info for category and question
            -   Added support for dependent questions across categories
    -   Fixed:
        -   Security and product issues
        -   Issue generation was choosing the wrong scope
-   **Version 11.0.2 - October 2020**
    -   New:
        -   VRM - Issue Creation Changes
        -   VRM - Engagement Changes
        -   VRM - External Monitoring Common Data Model
        -   VRM - Issue Creation Changes
        -   VRM - Issue Risk Factoring
        -   VRM - Portal Navigation Guidance
    -   Fixed: Enable report acl
-   **Version 10.1.3 - June 2020**
    -   New:
        -   New support for vendor engagements
        -   New support for vendor hierarchies and roll up risk scoring
-   **Version 10.0.2 - March 2020**
    -   New:
        -   Import an assessment questionnaire from an Excel spreadsheet
        -   Export questions and answers to an Excel spreadsheet
        -   Add e-signatures to assessments on the Vendor Portal
        -   Add e-signatures to the assessment approval process
-   **Version 9.0.1 - November 2019**

    This feature was updated for Madrid and is still compatible with New York.

-   **Version 7.0.9 - March 2020**

    Fixed: Problem saving vendor responses to SIG 2018 questionnaires

-   **Version 7.0.8 - December 2019**

    Fixed: Support additional information on vendor portal questionnaire. Madrid instances on Patch 9 or later are able to receive this bug fix.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

