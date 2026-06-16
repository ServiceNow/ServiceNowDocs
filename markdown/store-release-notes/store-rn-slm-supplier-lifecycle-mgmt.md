---
title: Supplier Lifecycle Operations release notes
description: Version history for the Supplier Lifecycle Operations application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-slm-supplier-lifecycle-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 16
breadcrumb: [ServiceNow Store - Supplier Lifecycle Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Supplier Lifecycle Operations release notes

Version history for the Supplier Lifecycle Operations application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.0.0 - June 2026 \(Australia\)**
    -   Fixed:
        -   Improved access controls for better security.
        -   Fixed translation of user interface text to ensure accurate display of product capabilities across multiple languages, resolving issues reported.
-   **Version 8.0.0 - June 2026 \(Zurich\)**
    -   Fixed:
        -   Improved access controls for better security.
        -   Fixed translation of user interface text to ensure accurate display of product capabilities across multiple languages, resolving issues reported.
-   **Version 5.9.0 - June 2026**
    -   Fixed:
        -   Improved access controls for better security.
        -   Fixed translation of user interface text to ensure accurate display of product capabilities across multiple languages, resolving issues reported.
-   **Version 7.0.0 - March 2026**
    -   New:
        -   -   Monitor and enforce time-bound documents from suppliers.
    -   -   Provides escalation pathways if document upload tasks are not completed.
-   Enables admins to configure document lead time, grace period, and reminder frequency.
-   Ensures seamless management of documents with expiration dates and reduces manual oversight on renewals.
-   Supplier managers or contacts can fill the expiry date while uploading documents. Based on this, automated upload document tasks are created \(Supported only in the Australia release\).
-   Assess supplier performance at scale powered by the Smart Assessment Engine application.
    -   Bulk distribution via segmentation rules: Associate assessment templates with supplier segments to survey hundreds of suppliers at once, replacing manual one-off outreach.
    -   Internal stakeholder completion: Sourcing and procurement teams complete assessments in the Source-to-Pay Workspace, keeping evaluations centralized and auditable.
    -   Supplier self-service completion: Supplier contacts complete their assessments through the Supplier Collaboration Portal.
-   Email-driven capabilities to simplify supplier interactions and centralize communication.
    -   Email-based task completion: Suppliers can directly complete tasks via email, such as marking tasks complete, playing videos, and accessing shared links.
    -   Centralized email tab: Email tab at supplier, case, and task levels to view all communications in one place.
    -   Email summarization: Summarization within emails provides quick and clear context for users \(for tasks and cases\).
-   **Version 5.6.0 - March 2026 \(Yokohama\)**
    -   New:
        -   Monitor and enforce time-bound documents from suppliers.
            -   The workflow enhances supplier document capabilities by:
                -   Providing users with escalation pathways if document upload tasks are not completed.
                -   Enabling admins to configure document lead time, grace period, and reminder frequency.
            -   Ensures seamless management of documents with expiration dates and reduces manual oversight and follow-ups on renewals.
        -   Assess supplier performance at scale powered by the Smart Assessment Engine application.
            -   Bulk distribution via segmentation rules: Associate assessment templates with supplier segments to survey hundreds of suppliers at once, replacing manual one-off outreach.
            -   Internal stakeholder completion: Sourcing and procurement teams complete assessments in the Source-to-Pay Workspace, keeping evaluations centralized and auditable.
            -   Supplier self-service completion: Supplier contacts complete their assessments through the Supplier Collaboration Portal.
        -   Email-driven capabilities to simplify supplier interactions and centralize communication.
            -   Email-based task completion: Suppliers can directly complete tasks via email, such as marking tasks complete, playing videos, and accessing shared links.
            -   Centralized email communication tab: Email tab at supplier, case, and task levels to view all communications in one place.
            -   Email summarization: Summarization feature within emails for supplier cases and tasks provides quick and clear context for users.
-   **Version 4.1.1 - October 2025**

    Fixed:

    -   Caller access for supplier onboarding email event
    -   Other minor fixes
-   **Version 1.0.2 - August 2025**

    New: Added Relish validations for existing suppliers, including Address, Banking, and Sanctions checks.

-   **Version 4.1.0 - May 2025**

    Minor fixes.

-   **Version 4.0.0 - February 2025**

    Minor fixes.

-   **Version 3.0.0 - December 2024**
    -   Enables effortless access to supplier contact information across multiple suppliers with a single set of login credentials.
    -   Centralises case and task tracking from various suppliers, enhancing efficiency within a single platform.
-   **Version 2.9.0 - November 2024**

    New: Added feature to support Supplier performance framework.

-   **Version 2.6.13 - September 2024 \(Washington DC\)**
    -   Fixed:
        -   The issue where the supplier contact could read the payment information of other suppliers has been fixed.
        -   The activity definition missing error seen in the Supplier onboarding playbook has been resolved.
        -   The issue causing the "Mark complete" button to show in the Review case lane of the Case playbook has been fixed.
-   **Version 2.8.0 - August 2024**
    -   New:
        -   Exchange supplier data with any third-party ERP system using improved transform maps, flows, inbound and outbound integration tables.
        -   Identify the supplier payment record in an ERP system using the Bank Identification Number \(BIN\) field in the Supplier Payment Information \[sn\_fin\_supplier\_payment\] primary table.
        -   View information related to suppliers in the Source-to-Pay Workspace:
            -   View contracts and supplier products in the Related Links section on the About tab of the Supplier page
            -   View purchase orders and invoices on the Related work tab of the Supplier page
            -           -   Create a knowledge base articles from the Source-to-Pay Workspace.
        -   Configure knowledge bases to enable publishing of knowledge base articles from Source-to-Pay Workspace.
-   **Version 2.6.8 - July 2024**
    -   Fixed:
        -   The Close notes field and Reject Supplier button are now displayed properly in the Supplier onboarding playbook.
        -   The Close notes field is now rendered properly in the Case playbook for all case types.
        -   Fixed issue related to the Skip button being unresponsive or not visible in playbooks.
-   **Version 2.6.0 - May 2024**
    -   New:
        -   Supplier Offboarding Playbook: The supplier offboarding playbook has been introduced that enables you to do the following:
            -   Create a supplier offboarding case to offboard a supplier
            -   Create a Due Diligence request if the GRC: Third-party Risk Due Diligence \[sn\_tprm\_dd\] plugin is installed
            -   View a list of pending supplier cases and tasks
            -   View existing contracts and invoices
            -   Maintain communication with the internal stakeholders and the supplier throughout the offboarding process
        -   Organization Tax Details table: A new table, Organization Tax Details \(sn\_fin\_org\_tax\_detail\) has been added that stores multiple tax registration details for each individual supplier. This table has been added in the Finance Common Architecture \(com.sn\_fin\) plugin.
        -   Assign task to internal users: Previously, tasks were only assigned to external users \(supplier contacts\). You can now assign tasks also to internal users. A new field Task audience has been added on the Details tab of the task to identify tasks that are internal or external.
        -   Risk tab in Source-to-Pay Workspace: A new Risk tab has been added on the Supplier record page in the Source-to-Pay Workspace. The Risk tab displays supplier risk assessment details, such as third-party name and process information, summary reports, risk intelligence scores, and tracking data for issues and tasks. The Risk tab is displayed only if you have installed the Third-party Risk Management \[com.sn\_vdr\_risk\_asmt\] and GRC:Advanced Vendor Risk Management \[com.sn\_vdr\_risk\_asmt\_workspace\] plugins.
        -   Supplier task changes: The supplier task of action type Sign document uses the document template \(PDF or HTML\). The E-signature template is used only for KB articles.
        -   Supplier case changes: The "Conduct a risk assessment" and "Conduct a tiering risk assessment" case types have been deprecated. A new case type Due diligence has been added that provides the functionality for conducting risk assessments.
        -   SLO integration framework: An integration framework is provided for inbound and outbound integrations. Customers intending to import supplier data \(such as supplier location, payment information, and supplier contact\) from third-party ERP systems can populate the SLO inbound staging tables, which will automatically populate the data into the SLO primary tables by using the default transform maps shipped with this feature. Customers intending to push supplier data into third-party ERP systems can refer to the SLO outbound tables from where they can pick and push the data into the ERP systems. The outbound tables are automatically updated when the SLO primary tables are updated.
            -   All the inbound tables and their associated transform maps are part of the ERP Integration Framework \(com.sn\_fcms\_integrations\) plugin.
            -   All the outbound tables and their associated flows are part of the Source-to-Pay Integration Framework \(com.sn\_spend\_intg\) plugin.
    -   Changed: Made updates to form views and labels.
    -   Upgrading to the May Store 2024 release \(Washington DC\):
        -   In the May Store 2024 release, the Action type column in the Supplier Task \(sn\_slm\_task\) table has been deprecated.
        -   In the May Store 2024 release, the Supplier Task \(sn\_slm\_task\) table uses the Action type for task column from its parent Service Task \[sn\_spend\_sdc\_service\_task\] table. After you upgrade to the May Store 2024 release, ensure that you run the fix script to migrate existing data from the deprecated Action type column to the newly added Action type for task column in the Supplier Task table.
        -   Important: Before you run the fix script, ensure that you restructure the Supplier Task table to extend the Service Task table.
        -   1.  Navigate to All &gt; System Definition &gt; Fix Scripts.
2.  Search for the SLO - upgrade scripts for may 2024 script.
3.  Open the fix script record.
4.  In the Script field, set the batch size variable to a number equal to the number of supplier task records in your instance. For example, if your instance has 10000 supplier task records, set the batch size variable as follows: var batchSize = 10000;
5.  Select Update.
6.  Select Run Fix Script.
-   **Version 2.5.0 - February 2024**
    -   New:
        -   A new plugin, Risk Assessments for Supplier Lifecycle Operations \(sn\_supplier\_tprm\) has been added that provides an integration with Third-party Risk Management \(TPRM\) application to conduct risk assessments when onboarding new suppliers using the Supplier onboarding playbook. In addition, the Supplier onboarding playbook now includes a new Perform risk assessment playbook that triggers two different flows to conduct supplier risk assessments, depending on the plugins that you have installed:
            -   If you have installed only the Risk Assessments Integration for Supplier Lifecycle Operations \[sn\_supplier\_tprm\] plugin, the Perform risk assessment playbook triggers the flow that includes activities to verify the eligibility of the supplier by creating risk assessments.
            -   If you have installed both the Risk Assessments for Supplier Lifecycle Operations \[sn\_supplier\_tprm\] and GRC: Third-party Risk Due Diligence \[sn\_tprm\_dd\] plugins, the Perform risk assessment playbook triggers the flow that includes activities to create a due diligence request, complete Inherent Risk Questionnaire \(IRQ\) assessments, and conduct risk assessments for a third-party or an engagement.
        -   The supplier manager can now create cases on behalf of suppliers in the Source-to-Pay Workspace
    -   Changed:
        -   Starting with the Washington D.C. release, Supplier Manager Workspace is being prepared for future deprecation. It will be hidden and no longer be activated on new instances but will continue to be supported. Source-to-Pay Workspace provides the latest experience for this functionality.
        -   The Case playbook has been updated to no longer include approval activities for completing the following supplier case types:
            -   Supplier support request
            -   General inquiry
        -   The Review supplier primary data playbook has been updated to no longer include approval activities for completing the following supplier case types:
            -   Banking information change request
            -   Supplier information change request
            -   Supplier location change request
    -   Upgrading to the Washington DC release
        -   After upgrading to the Washington DC release, you will see only the Source-to-Pay Workspace on the All navigation tab. You don't have to do anything if you choose to continue to use the Source-to-Pay Workspace.
        -   However, you will see both the Source-to-Pay Workspace and Supplier Manager Workspace on the Worksapces tab. If you want to use the Supplier Manager Workspace instead of the default Source-to-Pay Workspace, ensure that you run the following fix script after upgrading to the Washington DC release:
            -   fixscript\_migrate\_workspace\_to\_smw.xml
        -   If you want to revert to using the Source-to-Pay Workspace, run the following fix script:
            -   fixscript\_migrate\_workspace\_to\_s2p.xml
        -   Do these steps to download and run a fix script:
        -   1.  Download the required fix script XML file from the Supporting Links and Docs section.
2.  Navigate to All &gt; System Definition &gt; Fix Scripts.
3.  Right-click the Name column and choose Import XML.
4.  Select Choose file and then select the fix script XML file that you downloaded.
5.  Select Upload.
6.  Search for and select the fix script record to open it.
7.  Select Run Fix Script.
-   **Version 2.4.2 - November 2023**
    -   New:
        -   A new role, Supplier Agent \[sn\_slm.agent\] has been added. The supplier agent can do everything the supplier fulfiller can do, plus users with this role can:
            -   Create cases and tasks
            -   View all the suppliers, cases, and tasks
            -   Update all the tasks and assigned cases
        -   You can now configure due dates for different case types so that the Due date field is auto-populated when you create supplier cases.
        -   You can now specify a category while adding a supplier location. The choices are:
            -   Contracting address
            -   Delivery address
            -   Facility \(default\)
            -   Headquarters
            -   Invoice address
            -   Service center
        -   The generic case playbook is now displayed only for these case types:
            -   Supplier support request
            -   General inquiry
        -   A new playbook "Review supplier primary data request" has been introduced. This playbook is displayed when updating supplier primary data for the following case types:
            -   Banking information change request
            -   Supplier information change request
            -   Supplier location change request
        -   Introduced a new sidebar for supplier cases in the Supplier Manager Workspace. Sidebar enables stakeholders to collaborate with others by getting into discussions when working on supplier cases. You can start a Sidebar discussion by selecting Discuss on a supplier case in the Supplier Manager Workspace.
        -   You can now directly remove a supplier contact from the Supplier Manager Workspace by selecting the cross icon \(X\) next to the supplier contact name in the Supplier contacts widget.
        -   You can now add a subsidiary for a supplier from the Subsidiaries tab on the Supplier page.
        -   You can now add related cases for a supplier case from the Related Cases tab on the Supplier case page.
        -   You can now submit a supplier case in Draft state to indicate that it is ready to be worked on. A new UI action "Submit" has been added for a supplier case.
        -   You can now complete a supplier case when all the activities related to that case are completed. A new UI action "Complete" has been added for a supplier case.
        -   You can now reopen supplier cases that are in Closed completed, Closed rejected, and Closed canceled states. Note that the Re-open option is not available for the auto-closing supplier cases.
        -   Supplier Lifecycle Operations no longer uses Map UI Component for threat and alert data feeds \(com.sn\_fam\_map\) for supplier location maps. Instead the application now uses the Geo Map component \(sn\_geo\_map\) for displaying supplier location maps in the Supplier Manager Workspace. There is no impact to the existing map functionality due to this change.
    -   Changed:
        -   The following supplier cases types have been renamed:
            -   "Supplier onboarding" renamed to "Onboard new supplier".
            -   "Request or issue" renamed to "Supplier support request".
            -   "Other" renamed to "General inquiry".
            -   "Update banking details" renamed to "Banking information change request".
            -   "Update supplier profile" renamed to "Supplier information change request".
            -   "Elevate or restrict access" renamed to "Account access request".
            -   "Risk assessment" renamed to "Conduct a risk assessment".
            -   "Tiering assessment" renamed to "Conduct a tiering risk assessment".
        -   The following new supplier cases type has been introduced:
            -   Enroll a new supplier user
-   **Version 2.3.4 - August 2023**
    -   New: The new landing page for the Supplier Manager Workspace provides a more efficient way for you to view and work on your supplier cases and tasks, see your work summary at a glance, and easily manage your suppliers.
    -   Fixed:
        -   Supplier case records and forms: Minor fixes and UX improvements.
        -   Supplier task records and forms: Minor fixes and UX improvements.
        -   Supplier onboarding playbook: Minor fixes for UI issues and usability-related improvements.
-   **Version 2.2.0 - May 2023**
    -   New: The Advanced Work Assignment \(AWA\) for Supplier Lifecycle Operations feature enables you to automatically assign work items to agents based on availability and capacity. Using this feature, a supplier fulfiller can accept an incoming chat request from the Supplier Manager Workspace Inbox to start a chat session and directly interact with a supplier contact.
    -   Changed:
        -   Renamed this application to Supplier Lifecycle Operations. This application was formerly named Supplier Lifecycle Management.
        -   Renamed the Supplier Management Workspace to Supplier Manager Workspace.
        -   Onboarding playbook.
-   **Version 2.0.0 - February 2023**
    -   New
        -   Email composer with quick messages and response templates to better facilitate conversations between supplier managers and suppliers. Supplier managers can now directly send emails using predefined templates from a supplier case or task in the Supplier Management Workspace.
        -   The Supplier Lifecyle Management application \(com.snc.sn\_supplier\_mgmt\) now has a dependency on the Supplier Common \(com.snc.sn\_slm\) application, which is automatically installed when you install the Supplier Lifecycle Management application.
    -   Changed
        -   The following roles, which were earlier a part of the Supplier Lifecycle Management application, have been renamed and moved to the new Supplier Common application:
            -   Supplier Administrator \(sn\_slm.admin\)
            -   Supplier Contact \(sn\_slm.contact\)
            -   Supplier Fulfiller \(sn\_slm.fulfiller\)
            -   Supplier Manager \(sn\_slm.manager\)
            -   Supplier Owner \(sn\_slm.owner\)
        -   The following tables, which were earlier a part of the Supplier Lifecycle Management application, have been renamed and moved to the new Supplier Common \(com.snc.sn\_slm\) application plugin so that they can be commonly used and extended by other products.
            -   Supplier Product Code \(sn\_slm\_code\_m2m\_supplier\)
            -   Supplier Document Type \(sn\_slm\_document\_type\)
            -   Supplier Document References \(sn\_slm\_document\_references\)
            -   Product Code \(sn\_slm\_product\_code\)
            -   Supplier Case \(sn\_slm\_case\)
            -   Supplier Email Domain \(sn\_slm\_email\_domain\)
            -   Supplier Task \(sn\_slm\_task \)
            -   Supplier Location \(sn\_slm\_m2m\_location\)
            -   Supplier Document Configuration \(sn\_slm\_document\_config\)
        -   The Supplier Payment Information \[sn\_supplier\_payment\] table, which stores the bank account records of the suppliers, has been moved to Finance Common Architecture \(com.sn\_fin\) application and has been renamed as sn\_fin\_supplier\_payment.
-   **Version 1.5.1 - December 2022**

    Minor fixes.

-   **Version 1.5.0 - November 2022**
    -   New:
        -   Supplier owners can do the following:
            -   Remove supplier contacts and delegate their tasks before removing the contacts.
            -   Elevate or restrict access to supplier contacts.
        -   In the Supplier Management Workspace, added the Supplier Information tab that shows a 360-degree view of suppliers and contacts for a supplier case record. The Supplier Information tab shows details about the supplier and the supplier contact, a summary of all the open and overdue cases, and a list of all the cases by their priority.
        -   Supplier overview and Supplier contacts contextual side panels that display information about suppliers and supplier contacts, respectively, in the supplier case details and supplier case record pages. This allows you to quickly view supplier information without navigating away from these pages.
        -   Supplier administrators can create supplier document configurations to create automated tasks that enable suppliers to upload prerequisite documents.
    -   Changed: In the Supplier Management Workspace, if a supplier has more than 5 contacts, the Supplier Contacts widget displays links that show a list of contacts that have been registered and a list of supplier cases for contacts that are pending registration. This widget also shows an Admin label next to the contact's name, which indicates that the contact is a primary contact.
-   **Version 1.4.1 - September 2022**
    -   Fixed:
        -   Minor fixes and changes
-   **Version 1.4.0 - August 2022**
    -   New
        -   Improve supplier data quality by allowing suppliers to manage their own information
        -   Speed up issue resolution by allowing suppliers to collaborate directly with the business
        -   Vastly improve supplier onboarding time with structured playbooks
        -   Centralize supplier information and provide powerful tools for managing the entire lifecycle of suppliers
        -   Manage supplier networks to address issues at scale
        -   Orchestrate complex, cross-functional workflows to increase productivity
        -   Integrate with external data sources and aggregators for a 360-degree view of suppliers that facilitates data-driven decision-making
        -   Evaluate supplier performance and mitigate risk
-   **Version 1.3.0 - May 2022**

    With ServiceNow Supplier Lifecycle Management, you can effectively collaborate with suppliers, manage supplier relationships, monitor risk, compliance, and performance across the supplier life cycle.

    -   Supplier Data Management: Manage supplier data, contacts, performance, and plans to boost productivity of teams who engage with suppliers.
    -   Supplier Collaboration Portal: Resolve supplier inquiries and requests using services that orchestrate complex, cross-functional workflows, thus increasing team productivity and mitigating business risk.
    -   Supplier Management Workspace
        -   Detect issues quickly and take action to resolve conflicts before they impact the business.
        -   Compare suppliers and establish corrective action plans for poor performers.
    -   Supplier Onboarding
        -   Standard way to orchestrate onboarding activities across procurement, finance, legal, IT and more.
        -   Automate supplier activation across disparate systems.
        -   Consolidate documentation with process to drive ongoing updates and compliance across your supplier network.

**Parent Topic:**[ServiceNow Store - Supplier Lifecycle Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-slm-highlights.md)

