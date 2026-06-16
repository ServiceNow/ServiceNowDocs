---
title: Financial Services Operations release notes
description: Version history for the Financial Services Operations Financial Services Operations Core on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-financial-services-operations-core.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 12
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Financial Services Operations release notes

Version history for the Financial Services Operations Financial Services Operations Core on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 12.2.0 - June 2026**
    -   New:
        -   Added relationships for Insurance policies
        -   Added child tables for indexing for Financial Case indexed source
    -   Changed: Updated CSR query rule
-   **Version 12.1.1 - May 2026**

    New: Added new fields in Financial transaction authorization and Financial transaction table as part of 26.1 content pack changes for visa and mastercard.

-   **Version 11.0.4 - May 2026 \(Zurich\)**

    New: Added new fields in Financial transaction authorization and Financial transaction table as part of 26.1 content pack changes for visa and mastercard.

-   **Version 12.0.0 - April 2026**
    -   New:
        -   Added action layout items for CSR, enhancing the available options for customer service representatives.
        -   Introduced new security ACLs and role mappings, strengthening access control and ensuring only authorized users can access sensitive features.
    -   Updated: FSO now uses the native CSM Case Type Selector with Agent and User Criteria support, replacing custom extension logic and legacy components to reduce maintenance overhead and standardize case type handling across all user types.
    -   Fixed: Provided a glidefix script for Case type selector upgrade scenarios, ensuring a smooth upgrade process.
    -   Removed: Removed script includes that are no longer needed, as part of case type selector updates.
-   **Version 11.0.3 - April 2026 \(Zurich\)**
    -   Changed:
        -   Enhanced authorization-related transaction retrieval logic to improve transaction data accuracy and completeness.
        -   Added translations for multiple languages to support global users.
-   **Version 11.2.0 - March 2026**
    -   Updated:
        -   Updated the read-only option to 'Strict Read Only' for read-only fields
        -   Replaced direct references to the admin role with feature-specific granular admin roles to align with least-privilege access principles.
-   **Version 11.0.2 - February 2026**
    -   New:
        -   Orchestration flow that automatically triggers AI-powered document validation, classification, and extraction when Document Verification tasks are submitted
        -   Flow coordinates document processing by calling Document Processor subflows
    -   Changed: Updated task list layout in dispute workspace for better responsive display
-   **Version 11.0.0 - December 2025**
    -   New:
        -   Financial Transaction Enhancements: Added new fields and additional configurations for financial transactions and authorization, supporting richer data capture and improved financial operations.
        -   ACH Payment Network Support: Added support for ACH payment network, including model changes, data broker, and ACL updates for ACH common intake.
    -   Changed:
        -   Role and ACL Updates: Added sn\_doc\_processor roles to consumer/customer and updated payment network read ACLs to include consumer and customer roles, enhancing security and access control.
        -   Decision Table and ACL Enhancements: Added query range ACL for transaction date fields and updated methods to support transactions by multiple networks.
    -   Fixed:
        -   Contact Role Assignment: Added business rules and made subflows/action updates to ensure correct contact role assignment, improving data integrity.
        -   Choice and Value Corrections: Fixed issues with select choices and value checks, including empty value checks and case mismatches in labels.
        -   Inactive Transaction Display: Refactored code to prevent non-active transactions from being displayed in core documents.
-   **Version 10.0.1 - October 2025**
    -   New
        -   Enhanced Transaction Matching
            -   Added new method getMatchingAuthTransactions to identify and retrieve transactions with the same authorization code
            -   Implemented support for filtering transactions by network transaction ID
            -   Added date range filtering capabilities to narrow down transaction matches
            -   Improved transaction search by financial account to support dispute resolution workflows
-   **Version 9.1.3 - October 2025**
    -   New:
        -   Enhanced Transaction Matching
            -   Added new method getMatchingAuthTransactions to identify and retrieve transactions with the same authorization code
            -   Implemented date range filtering for transaction searches to improve accuracy and relevance of results
            -   Added support for filtering by network transaction ID to better identify related transactions
            -   Enabled exclusion of the current transaction from search results to focus on other matching transactions
    -   Changed:
        -   Improved Localization Support
            -   Enhanced client-side scripts with proper message handling for internationalization
            -   Updated validation messages to use the getMessage\(\) function for proper translation support
            -   Improved user experience for non-English users with properly localized error messages
-   **Version 10.0.0 - August 2025**
    -   New:
        -   Added new attachments screen to show attachments as the first tab in the side panel
        -   Added read ACLs for customers to access B2B accounts \(Savings, Checking and Credit card\) to support B2B2C/B2B2E
        -   Added fields for Issuer BIN, Acquirer BIN, Issuer ICA, and Acquirer ICA to financial transaction table
        -   As part of this release, Deny ACLs were introduced on the existing tables. These Deny ACLs will restrict access for unauthenticated users on CRUD Operations
    -   Fixed: Fixed query to get numeric currency code
    -   Changed:
        -   Updated B2B account form views to add consumer
        -   Increased length of Network transaction ID to 255
-   **Version 9.1.0 - May 2025**
    -   New: Added fields for storing shipping addresses and validating similar transaction logic for friendly fraud in the script include.
    -   Fixed: Minor accessibility issues
-   **Version 9.0.0 - March 2025**
    -   New: Added new columns to sn\_bom\_transaction table
    -   Changed: Updated cancel playbooks for task function to cancel task playbooks forcefully
-   **Version 8.0.6 - February 2025**
    -   Added: Added 'Claim fraud decision', 'Claim validation decision', and 'SIU review' to the Claim Base table
    -   Fixed:
        -   Added reject rule to fix KMF policy of FSO core
        -   Glide script to promote columns
    -   Changed: Updated the translation changes for Q1
-   **Version 7.0.3 - November 2024**
    -   New:
        -   Added Network ID field for Chargeback Reason Codes.
        -   Added sn\_bom.flow\_executor role to the claim core's flow\_executor.
        -   Updated "Create Document Verification Task for Consumer or Contact" to handle account as well.
        -   Added new roles to sn\_bom.adjuster and sn\_bom.fnol\_representative.
        -   Added ACLs for Travel Policy tables.
        -   Added script include: CommercialTravelPolicyDAO, PersonalTravelPolicy, PersonalTravelPolicyDAO, CommercialTravelPolicy, IncidentTypeDAO, IncidentType.
        -   Add tables Personal/Commercial Travel Policy.
        -   Added table Incident Type.
        -   Added ACLs for Incident Type table.
    -   Changed:
        -   ClaimAjax and BankingAjax have been made as Sandbox enabled as false.
        -   Added new script include BankingQueryAjax with Sandbox enabled as true.
        -   Updated UIBDataBrokerUtil to handle coverages for task table as well.
        -   Styling changes done for Claim Workspace.
        -   Bring back details tab on Claim adjuster record page.
        -   Refactored PolicySnapshotGenerator.
        -   Refactor Claim Details on Claim Summary.
    -   Fixed:
        -   Related list for policy snapshot will now show Claim participant instead of policy participant\(When claims app is install\).
        -   Insurance Customer Info page - Added null check in the UX client script to fix the console error.
    -   Removed: Removed Card provider field from Chargeback Reason Codes.
-   **Version 6.0.10 - October 2024**

    New: Added liquid assets choice to Business App ID field on Financial transaction table.

-   **Version 6.0.6 - September 2024**

    Fixed: Rendering of add participant button on insurance claim participants widget on core adjuster workspace.

-   **Version 6.0.2 - August 2024**
    -   New:
        -   Added Insurance policies and Policy Snapshots to the Claim base table.
        -   Added Relationship to insured to the Policy participant table.
        -   Added Beneficiary type, Allocation percentage, Irrevocable to the Policy participant role table.
        -   Added the Beneficiary sub page.
        -   Added claim summarization component to the adjuster record page.
        -   Added read ACL for sn\_bom\_case.comments\_and\_work\_notes.
        -   Added new common landing page, which enables user to switch between dashboard pages based on access.
        -   Added read access for transactions to cardholders.
    -   Changed:
        -   Modified the adjuster workspace to show/hide playbook based on role and stage.
        -   Modified condition to hide the Fraud score tab, Customer Information tab, Claim summary tab for individual life claims app.
        -   Modified related lists for individual life policies.
    -   Fixed:
        -   Fixed Customer central page to show all claims when there is no insurance policy
        -   Fixed auto refresh of widgets on the Claim workspace page
    -   Removed: Removed header component from all existing landing pages
-   **Version 5.0.3 - June 2024**
    -   Fixed:
        -   Fixed i18n issue for case type selector
        -   Removed invalid query on insurance\_policy field in Policy participant table
-   **Version 5.0.0 - May 2024**
    -   New:
        -   Added extension point implementation to show required service definitions in case type selector model screen
        -   Added fix script to migrate data from FSO service definition category \(sn\_bom\_service\_definition\_category\) table to CSM service category\(sn\_csm\_case\_types\_service\_category\) and relationship tables
        -   Added Currency ISO Code Association table
        -   Added the following fields to the Financial Transaction table
    -   1.  Product description
2.  Merchant floor limit
3.  Message reason code
4.  Authorization date
5.  Acquirer country code
6.  Total settled amount currency desc
7.  Avs response code
8.  Cavv authentication results code
9.  CAVV result
10. Cryptogram
11. Merchant category code \(MCC\)
12. Central processing date
13. Jurisdiction
14. Cash back amount
15. Merchant address
16. Merchant city
17. Merchant country
18. Merchant name
19. Merchant state
20. Merchant phone number
21. Merchant URL
22. Merchant email
23. Merchant postal code
24. Merchant country code
25. Token
26. Processing code
27. POS condition code
28. Pos terminal capability code
29. Entry mode
30. Lodging no-show indicator
31. CAVV type
32. Purchase inquiry ID
33. Visa transaction type
34. Purchase info available indicator
35. Visa merchant ID
36. CVV result
37. Chip condition code
38. Market-Specific Data Identifier
39. ECMOTO
40. Pos Environment
41. Proof full chip
42. Card authentication reliability indicator
43. Chip transaction indicator
44. Authorization source code
45. PIN-Preferred chip code
46. PIN entry capability
47. CVV2 result
48. CVV2 present indicator
49. Ind for3D secure
50. Token verification results code
51. Auth not available in ATR indicator
52. Reimbursement attribute
53. Issuer region
54. Acquirer region
55. Transaction status
56. Business application ID
57. Fee program indicator
58. RDR eligibility indicator
59. Purchase inquiry eligible indicator
60. Visa transaction type short description
    -   Changed:
        -   Updated case creation model screen from FSO interceptor to CSM case type selector. More details are available in this KB article KB1638995.
        -   Modified the type of the following fields from integer to string:-
            -   Acquirer Reference Number- Authorization code
            -   Modified configuration for localization support
    -   Removed:
        -   Deprecated FSO service definition category \(sn\_bom\_service\_definition\_category\) table
        -   Deprecated category field from Service definition \(sn\_bom\_service\_definition\) table
        -   Deprecated sn\_bom.requestor, sn\_bom.b2b\_requestor, sn\_bom.b2c\_requestor, sn\_bom.fs\_requestor roles and related UI actions
-   **Version 4.2.0 - February 2024**
    -   New:
        -   Added a new activity layout and activity definition for editing list items within playbook activity
        -   Added new field Active in the Chargeback reason codes table
        -   Added read ACL for Currency table for agent
        -   Added new table Merchant Category Code
        -   Added new table Payment Network
        -   Added new fields Issuer BIN, Product ID, Authorization date time, Network ID, Merchant Name, Network transaction ID, MoTo, Transaction response code, Authorization response code, Transaction categorization, Acquirer reference number, Authorization code, Authorization date time to the Financial Transaction table
        -   Added data to the Chargeback reason codes table for card provider VISA
    -   Changed:
        -   Migrated landing pages, interceptor page and customer informartion pages to UIB layout 3.0
        -   Renamed Dispute category choice, Consumer dispute to Customer dispute
        -   Upgraded snc-app-parent version to 5.1.0.16
    -   Fixed:
        -   Fixed the display of the claims details section in the claim workspace
        -   Fixed alignment in the policy section in the Customer Information page
        -   Fixed the contact policy relationship
    -   Removed: Removed Cardholder dispute choice from the Category field in the Chargeback reason codes tables
-   **Version 3.0.1 - December 2023 \(Vancouver\)**
    -   Removed:
        -   Removed the 'Generate insured property for policy snapshot" subflow, which was in draft state
        -   Removed the 'Generate policy snapshot" subflow, which was in draft state
        -   Removed the 'Generate participant for policy snapshot' subflow, which was in draft state
-   **Version 3.0.0 - November 2023**
    -   New:
        -   Added new string fields Coverage Type and Coverage Value to the Policy Coverage table to support external system integration
        -   Added Sold Product column to the Financial Services Base table
        -   Added External ID field to the below tables
            -   Customer Property
            -   Insured property
            -   Policy Coverage
            -   Policy Participant
    -   Changed:
        -   Moved card model, personal insurance model, commercial insurance model, group life insurance model, individual life insurance model, financial services model, deposit model, loan model, investment model, loan model and lines of credit model tables to Expanded Model and Asset Classes application.
        -   Added Fix script to move the data from existing model tables to new model tables.
        -   Data from product code &amp; product type fields in model tables will be moved to model number &amp; service type field
        -   Data from start date &amp; end date fields in model tables will be moved to service model lifecycle records
        -   Added required sn\_ent model viewer roles to existing financial account viewer roles
        -   Renamed Policy Participant Insured Property to Policy Participant Role
        -   Renamed External System ID to External ID in the Financial Account and Insurance Policy table
-   **Version 2.2.0 - August 2023**
    -   New
        -   Added Claim workspace for the adjuster to view the claim details, fraud score, and claim summary
        -   Added FSO default record page for adjuster workspace
        -   Added a new summary page for claim case
        -   Added a new page for claim fraud score
        -   Added ""Incident Location"" field on the Claim base table
-   **Version 2.1.0 - May 2023**

    New:

    -   Added UX page properties for the Agent Assist on Voltron record page.
    -   Added screen collection entries for the 'Customer Information' \(Customer 360\) on Voltron page.
    -   Added Fault rating field to Claim Base table.
    -   Added spoke selector subflow to lookup claim fraud score data.
    -   Added Fraud score reference to Claim Base table.
    -   Added role fraud\_score\_reader to processor and adjuster.
    -   Added decision table to specify line of business.
    -   Added UI component to display claim fraud score in the contextual side bar.
-   **Version 2.0.2 - March 2023**

    Fixed: Fixed insurance policy viewer role hierarchy to read policy data.

-   **Version 2.0.1 - February 2023**
    -   New:
        -   Added a new role "sn\_bom.relationship\_contributor"
        -   Added report date to customer information list view
        -   Added new column 'Category' to the transaction table
    -   Changed:
        -   Renamed role "sn\_bom.b2c\_contributor" to "sn\_bom.consumer\_contributor"
        -   Renamed role "sn\_bom.b2b\_contributor" to "sn\_bom.account\_contributor"
        -   Renamed claim base State field to Status
        -   Updated contributor roles
        -   Updated UI actions for case
-   **Version 1.9.0 - November 2022**
    -   New:
        -   Added the business location functionality
        -   Added the claim information to the customer information page
        -   Added claim payment approval process
        -   Added FNOL representative landing page
        -   Added role sn\_bom.location\_manager\_contributor
        -   Added landing page for Location manager
        -   Added spoke selector configuration for JHA
    -   Changed: Updated label for the table 'Claim Policy Base' to 'Claim Base'
    -   Fixed: Fixed labels for lines of credit tables
-   **Version 1.8.0 - August 2022**

    New: Added new tables to support Individual and Group life insurance use cases

-   **Version 1.7.0 - May 2022**
    -   New:
        -   Added dependency to new Document Processor application to collect and verify customer documents
        -   Agent and contributor inherit document collector role from Document Processor
-   **Version 1.6.2 - March 2022**

    New: Ability to model coverages and coverage options for all types of insurance policies

-   **Version 1.5.1 - October 2021**
    -   New:
        -   Added table for Investment Product Model extending Product Model
        -   Added table for Investment Account extending Sold Product
        -   Added table for Investment Transaction extending Financial Transaction
        -   Added the following tables for Securities Holdings:
            -   Holding
            -   Holding Lot
        -   Added the following tables for Securities:
            -   Security
            -   Stock
            -   Option
            -   Bond
            -   ETF
        -   Added the following roles to view Investment products, Investment accounts, Transactions, Holdings, and Securities:
            -   Investment account viewer
            -   Security viewer
        -   Added menu modules for Investment account and Securities
    -   Changed: Restructured Financial Services Operations menu modules
-   **Version 1.4.0 - July 2021**
    -   New:
        -   Added table for Financial Services Model extending Product Model
        -   Added tables for Financial Services: Wire Service and RDC Service
        -   Added roles for each type of Financial Services and Financial Services Models
-   **Version 1.3.1 - May 2021**
    -   Changed:
        -   Industry core application dependency version has been updated
        -   Re-parenting of task, sold product and transaction tables
-   **Version 1.3.0 - April 2021**
    -   New:
        -   Extended product model table to create Auto Insurance Product and Homeowner Insurance Product tables Extended financial account table to create Auto Insurance Policy and Homeowner Insurance Policy tables
        -   Extended financial transaction table to create Insurance Policy Transaction tables
        -   Added the following roles to view insurance product, insurance policies, and transactions:
            -   Insurance policy viewer
            -   Auto policy viewer
            -   Homeowner policy viewer
-   **Version 1.2.0 - March 2021**
    -   New:
        -   Added new case type: Financial Services Case
        -   Added new roles: Financial Services Agent, Financial Services Requestor
-   **Version 1.1.0 - December 2020**
    -   New:
        -   Personal Banking - Data model extended to support financial accounts, associated financial transactions, and the corresponding product model for Student Loans for Personal Banking
        -   Business Banking - Data model extended to support financial accounts, associated financial transactions, and the corresponding product models for:
            -   Business checking/savings account
            -   Business loans like term loans and equipment loans
            -   Business line of credit
-   **Version 1.0.4 - September 2020**

    Provides a Financial Services data model that is used in Financial Services Operations workflows. This includes Financial Accounts, Financial Product Models, and Financial Transactions.


