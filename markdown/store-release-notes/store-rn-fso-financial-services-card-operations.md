---
title: Financial Services Operations release notes
description: Version history for the Financial Services Operations Financial Services Card Operations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-financial-services-card-operations.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 12
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Financial Services Operations release notes

Version history for the Financial Services Operations Financial Services Card Operations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 12.0.5 - June 2026 \(Zurich\)**
    -   Changed:
        -   Updated the label for the dispute reason option from "Failed travel merchant-intra-eea and domestic european transactions only" to "Failed travel merchant specific european transactions only" in the Dispute Intake form to improve clarity for users selecting dispute types.
        -   Enhanced the Dispute Intake Questionnaire form by reorganizing UI sections and updating field visibility rules to streamline the dispute intake process.
        -   Modified client scripts for Credit Voucher Transaction Receipt handling to improve form behavior and validation.
        -   Updated UI policies controlling when fields are shown or hidden on the Dispute Intake form to ensure appropriate fields are displayed based on user selections.
-   **Version 13.2.0 - June 2026**

    Changed: Updated Dispute Intake Questionnaire

-   **Version 13.1.0 - May 2026**
    -   Changed:
        -   Updated internal policy rules to evaluate dispute amount directly from the card dispute transaction instead of from the financial transaction, improving accuracy in policy decisions
        -   Added new questions for Visa-specific dispute scenarios to capture additional information during dispute intake.
    -   Fixed: Resolved intermittent issue where card dispute fields were not properly disabling when users clicked Continue button in the Verifi integration workflow
-   **Version 12.0.4 - May 2026 \(Zurich\)**

    New: Added new questions for Visa-specific dispute scenarios in the to capture additional information during dispute intake

-   **Version 13.0.2 - April 2026**
    -   New:
        -   Added new decision questions, scripts, and macro components to support advanced workflows.
        -   Added new UI policies, questions and scripts to align with the latest. visa rev\(26.1\) changes.
        -   Added new activity type templates and mappings to support customer history tracking and management.
    -   Updated:
        -   Updated few UI policies to align with the latest visa revision\(26.1\) changes
        -   Moved AI engagement event logic to the fso ai scope for better maintainability and separation of concerns.
        -   FSO now uses the native CSM Case Type Selector with Agent and User Criteria support, replacing custom extension logic and legacy components to reduce maintenance overhead and standardize case type handling across all user types.
        -   Enhanced Verifi integration, including updates to UI policies and supporting files for dispute management.
    -   Fixed:
        -   Resolved issues with the getMessage function to ensure accurate messaging in the app.
        -   Fixed minor issues in the MC for smoother user experience.
-   **Version 12.0.3 - April 2026**
    -   Changed
        -   Enhanced user interface policies to dynamically show and hide relevant fields based on dispute type and context.
        -   Updated fraud section user interface policies to improve form usability and data collection accuracy.
        -   Added translations for multiple languages to support global users.
-   **Version 12.2.0 - March 2026**
    -   New:
        -   Added relationship script to get the sn\_bom\_transaction for specific consumer and all financial account this consumer holds.
        -   Added ACL roles for payment card databroker execute ACLs.
        -   Added business rule "Sync case acknowledgment by transactions" to automatically sync case acknowledgment status when all dispute transactions are acknowledged.
        -   Added action to zip uploaded documents using Integration Hub zip plugin
        -   Added external document IDs field in if folder for Card Data Security. Will be used to store merchant document IDs.
        -   Added reusable subflow to attach documents to either skyflow or sys\_attachment
        -   Added client- and server-side validation to prevent future dates for Dispute Reported Date.
        -   Added missing Mastercard reason code mappings to the "Derive Intake Answers from Chargeback Reason Code and Messages" decision table for automatic intake form pre-population for RC 4808, RC 4834
    -   Changed:
        -   Updated the existing recommendation loader and recommendation component, enhanced the UI actions within the recommendation component
        -   Updated default Dispute reported date to the dispute transaction created date \(Card dispute transaction table\)
        -   Updated the read-only option to 'Strict Read Only' for read-only fields
        -   Replaced direct references to the admin role with feature-specific granular admin roles to align with least-privilege access principles.
-   **Version 12.0.1 - February 2026**

    Changed: Fixed the accessibility issue on transaction components in the BLSP portal.

-   **Version 12.0.0 - December 2025**
    -   New:
        -   Initiation Process:
            -   Common:
                -   Introduced unified intake process for card and non-card \(ACH\) transactions
                -   Enhanced views in Initiation/Review flow to also support ACH transactions in workspace, portal, and VA
                -   Added new playbook and decision tables to determine dispute category and reason codes
                -   Duplicate check logic and messaging when financial transactions have existing dispute cases
                -   Case triaging framework for automating dispute case prioritization
            -   Non-cards:
                -   ACH Email Communication: Pre-defined email templates with e-signature support for customer communication via Written Statement of Unauthorized Debit \(WSUD\) forms
                -   Document Management: Added support for WSUD document definitions with attachment components
                -   New activity for collecting and signing documents in Initiate and Review
                -   Added questionnaires for ACH dispute handling
        -   Processing:
            -   Non-cards:
                -   Introduced end-to-end dispute processing from investigation to closure for ACH transactions
                -   Defined service level agreements \(SLAs\) for ACH dispute processes
                -   New workspace for handling ACH transactions dispute lifecycle
                -   New Email Templates for communication tasks email
            -   Cards:
                -   Defined service level agreements \(SLAs\) for Mastercard dispute processes
                -   Changes supporting end-to-end Mastercard integration
                -   Capability to add documents to a dispute task on workspace
    -   Fixed: Fixed the transaction closure flow at investigation stage when the decision taken is to write off the dispute amount
-   **Version 11.1.0 - October 2025**
    -   New
        -   Enhanced Error Handling
            -   Added better error handling when authorization code is not available
            -   Implemented fallback logic for missing authorization codes
    -   Changed
        -   Visa 25.2 VROL Compliance Updates
            -   Updated questionnaire with revised terminology for Visa 25.2 VROL compliance
            -   Changed transaction-related questions to use ""payment credential"" instead of ""card"" terminology
            -   Updated merchant status question to ""Is the merchant insolvent or bankrupt?"" for clarity and compliance
        -   Transaction Handling Improvements
            -   Made fields conditionally mandatory based on transaction type
            -   Enhanced the logic to populate same authorization transactions automatically
            -   Improved reference qualifier functionality for same authorization transactions
        -   Code Quality Enhancements
            -   Enhanced code readability with better variable naming and formatting
            -   Optimized query performance for transaction lookups
    -   Fixed
        -   Reference Qualifier Issues
            -   Fixed reference qualifier query by properly using authorization code variable
            -   Fixed potential null reference issues in dispute transaction handling
-   **Version 10.2.2 - October 2025**
    -   New:
        -   Enhanced Error Handling
        -   Added fallback logic for missing authorization codes
        -   Implemented proper error handling when authorization code is not available
    -   Changed:
        -   Visa Questionnaire Updates
            -   Updated questionnaire with revised terminology for Visa compliance
            -   Changed transaction-related questions to use "payment credential" instead of "card" terminology
            -   Updated merchant status question to ""Is the merchant insolvent or bankrupt?"" for clarity
            -   Transaction Handling Improvements
                -   Made fields conditionally mandatory based on transaction type
                -   Enhanced the logic to populate same authorization transactions automatically
                -   Improved reference qualifier functionality for authorization transactions
                -   Updated variable names for better code readability
            -   Code Quality Enhancements
                -   Enhanced code formatting and structure
                -   Optimized query performance for transaction lookups
    -   Fixed:
        -   Reference Qualifier Issues
            -   Fixed reference qualifier query by properly using authorization code variable
            -   Fixed potential null reference issues in dispute transaction handling
            -   Added proper fallback query \('sys\_id=-1'\) when authorization code is missing
-   **Version 11.0.0 - August 2025**
    -   New:
        -   Added a new page "Dispute Workspace" for Dispute transaction records
        -   Added E2E flow for managing disputes lifecycle under Mastercard's network
    -   Changed:
        -   Updated trigger condition for common Dispute Transaction playbook to not run for Mastercard transactions
        -   Added support for B2B2C/B2B2E usecase.
        -   Moved next activity status determination logic for Dispute case to decision table
-   **Version 10.2.0 - May 2025**

    New: Added a step to the card dispute application to identify and take action for friendly fraud cases.

-   **Version 10.1.0 - April 2025**
    -   Added a new client script to a field in the Dispute Intake table.
    -   Removed data column 'is\_parcelado' from Dispute Intake table.
    -   Modified some UI policies, forms, and sections.
    -   Updated an error message in the client script.
-   **Version 10.0.0 - March 2025**
    -   New:
        -   Added new data fields to Dispute Intake, Card Disputes Task, and Card disputes transaction tables to capture more information
        -   Added fix script to enable audit for Card Disputes Transaction
        -   Introduced dedicated playbooks for Card Dispute Transaction - one for Visa and other card networks
        -   Integrated Visa API touchpoints into the Case and Transaction playbooks for Visa disputes \(requires Visa integration installation\)
        -   Added "Select associated transactions" activity in playbook to select associations when Visa integration is enabled
        -   Included a "Fill additional transaction questions" activity for handling disputes involving multiple transactions
        -   Added activities to manage pre-arbitration and arbitration process for Visa disputes
    -   Changed:
        -   The Card Disputes Service Case playbook now includes a processing lane, and Investigation and Chargeback actions have been shifted to the Transaction level playbook to facilitate independent movement and processing of each transaction
        -   A new report has been added to the dispute agent's landing page to highlight instances where acquirers have missed the response deadline
-   **Version 9.1.0 - February 2025**
    -   New:
        -   Added a new custom activity to resume dispute cases initiated by VA.
        -   Provided financial account write access to consumers and customers, allowing them to select a financial account after case creation, for example, in the 'Resume dispute case' activity.
        -   Created access for card disputes transactions for agents, agent connectors, and contributors.
        -   Added a form view to collect financial account and financial transaction details for VA, and implemented UI policies.
        -   Added business rules to copy VA financial transactions and additional transactions \(only in the fraud category\) to the existing financial transactions field.
    -   Changed:
        -   Updated the case playbook to handle VA-initiated cases by moving intake creation and reason code update logic to the flow.
        -   Updated the scope name in the reference qualifier for the Financial transactions field.
        -   Updated translation changes for Q1.
-   **Version 8.0.1 - November 2024**
    -   New:
        -   Added generic intake table for cardholder and agent.
        -   Added UI policies, business rules, views, client scripts for new intake tables.
        -   Added Reason code message field to Card disputes transaction.
    -   Changed:
        -   Updated references of card provider to use transaction Network ID to support multi-network.
        -   Updated the reason code calculation logic to be at each transaction level, instead of case level.
        -   Updated disclaimer message on Submit activity.
        -   Updated view on completion of record generator activity.
        -   Setting display property false for Associated transaction field and added fix script for that.
        -   CardDisputesTaskAjax has been made as Sandbox enabled as false.
    -   Removed: Removed Account status as of transaction date, Dispute amount modification reason, Reason code, Reason code message and Suggested reason code from Card disputes transaction table.
-   **Version 7.0.5 - October 2024**

    Removed Late Presentment from processing Error decision question.

-   **Version 7.0.3 - September 2024**

    Fixed: Updated record generator activity to show only form view on activity completion, without any clickable cards.

-   **Version 7.0.1 - August 2024**

    New

    -   New:
        -   Added configurations to integrate the dispute flow with Mastercard questionnaire and chargeback eligibility rules
        -   Added summarization feature for dispute case
        -   Added technical dashboard landing pages for dispute manager, card agent and dispute agent
        -   Introduced a user-friendly portal interface that enables customers to easily start and manage disputes.
        -   Added new fields for deriving category:
        -   What issue are you experiencing with the transaction?
        -   Did you authorize the transaction?
        -   What is the issue that you are experiencing?
        -   Do you recognize the merchant and the purchase?
    -   Changed:
        -   Existing landing page view changed to a new dashboard view
        -   Modified playbook flow to support both cardholder and agent flow
    -   Fixed: Fixed security defect with adding of report\_view ACL for tables sn\_bom\_credit\_card\_disputes\_transaction
    -   Removed:
        -   Removed existing landing pages and respective accessibility records
        -   Deactivated subflow, action and activity definition for creating questionnaire
-   **Version 5.0.0 - May 2024**
    -   New:
        -   Migrated data from FSO service category \(sn\_bom\_service\_definition\_category\) table to CSM service category\(sn\_csm\_case\_types\_service\_category\) and relationship tables
        -   Added Event Inquiry app as a dependency
        -   Added the following field to Card Disputes Service Case
            -   TI event ID
        -   Added a decision table to configure Visa dispute questionnaire
        -   Added new menus for Next experience dashboard menu
    -   Changed:
        -   Modified configuration for localization support
        -   Modified playbook to
            -   Spawn applicable tasks dynamically
            -   Add new lane and fields for closure of case
    -   Removed:
        -   Deprecated sn\_bom\_credit\_card.requestor role and related UI actions
        -   Removed the dependency to Guided Decisions Experience
        -   Removed the following fields from Card Disputes Transaction
            -   1.  Card network
2.  Card type
3.  Merchant address
4.  Merchant city
5.  Merchant country
6.  Merchant name
7.  Merchant state
8.  Merchant phone number
9.  Merchant URL
10. Merchant email
11. Merchant postal code
12. Merchant country code
13. Merchant category code \(MCC\)
14. Central processing date
15. Jurisdiction
16. Product description
17. Transaction amount
18. Transaction date
19. POS condition code
20. Entry mode
21. Fraud report ID
22. Chargeback rights indicator
23. Reimbursement attribute
24. Business application ID
25. CAVV type
26. Processing code
        -   Removed the following field from Card Disputes Service Case: Are supporting documents available?
-   **Version 4.0.0 - February 2024**
    -   New:
        -   Added the Guided Decision Experience app as a dependency
        -   Added configuration for questionnaire and chargeback eligibility rules for VISA
        -   Added the below fields to the Card Disputes Service Case table:
            -   Category
            -   Reason code
            -   Cardholder permission
            -   Account status as of transaction date
            -   Are supporting documents available?
        -   Added the below fields to the Card Disputes Transaction table:
            -   Reason code
            -   Chargeback eligibility
            -   Chargeback eligibility reason
            -   Processing code
            -   CAVV Type
            -   Business Application ID
            -   POS condition code
            -   Entry mode
            -   Exception type
            -   ROL transaction ID
            -   Visa case number
            -   Visa dispute ID
            -   Fraud report ID
            -   Merchant address
            -   Merchant phone number
            -   Merchant URL
            -   Merchant email
            -   Merchant postal code
            -   Merchant country code
            -   Merchant category code
        -   Horizontal process layout for disputes. Added 'Case information' and 'State of transaction' widgets for the disputes record page.
    -   Changed:
        -   All list activities to open form on same playbook activity
        -   Migrated the agent assist pages to UIB layout 3.0
    -   Removed:
        -   Removed Dispute Reason and Fraud alert fields in the Card Dispute Service Case table
        -   Removed Dispute Reason field in the Card Dispute Transaction table
        -   Removed field Do you suspect fraud? from the Card Dispute Task table
-   **Version 2.5.0 - November 2023**
    -   New:
        -   Added email notifications for card dispute cases &amp; transactions.
        -   Added list edit ACL on dispute transaction table for users with roles sn\_bom\_credit\_card.dispute\_agent\_connector, sn\_bom\_credit\_card.contributor, sn\_bom\_credit\_card.dispute\_agent.
    -   Changed:
        -   Updated label for the 'Did merchant respond?' field to 'Merchant response' and updated the choice values.
        -   Moved product model demo data from the 'sn\_bom\_card\_model' table to 'sn\_ent\_card\_service\_model' table.
        -   Updated dispute card transactions playbook name to Card Disputes.
        -   Updated 'Submission comment' field label to 'Comment' in 'sn\_bom\_credit\_card\_disputes\_service' table
        -   Updated 'Chargeback details' field label to 'Chargeback reason code and description' in 'sn\_bom\_credit\_card\_disputes\_task' table
        -   Updated 'Transaction verified' field label to 'Customer response' in 'sn\_bom\_credit\_card\_disputes\_transaction' table
-   **Version 2.4.0 - August 2023**
    -   New
        -   Added approval process for card dispute playbook flow
        -   Added landing page for card dispute manager
        -   Added email template for card dispute flow
-   **Version 2.3.0 - May 2023**
    -   New:
        -   Added UX page properties for the Agent Assist on Voltron record page.
        -   Added localization changes.
    -   Changed: Updated Dispute Card transactions playbook activity name from Alert merchant to Alert participating merchant.
-   **Version 2.2.0 - February 2023**
    -   Changed:
        -   Updated contributor roles
        -   Updated UI actions for case
-   **Version 2.1.0 - November 2022**
    -   New: Added business location functionality
    -   Fixed: Fixed dark theme issues
-   **Version 2.0.0 - August 2022**
    -   New:
        -   Added configuration for document signing with integration to Document Template
        -   Added Document processor features
    -   Changed: Updated existing flows to support new document functionalities
    -   Removed: Financial document services application dependencies
-   **Version 1.0.6 - May 2021**

    Changed: Financial Services Core application dependency version has been updated

-   **Version 1.0.5 - March 2021**
    -   New: Added support of Serivce Definitions
    -   Changed: Moved plugin dependencies to Financial Services Operations Core
-   **Version 1.0.4 - September 2020**

    Provides capabilities to consolidate requests for a Card Operations team and route them through workflows to the appropriate middle and back office teams.


