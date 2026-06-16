---
title: Commercial Lines Claims release notes
description: Version history for the Commercial Lines Claims application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-fso-commercial-lines-claims.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Financial Services release notes, ServiceNow Store release notes]
---

# Commercial Lines Claims release notes

Version history for the Commercial Lines Claims application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.6.0 - June 2026**

    New: Added child tables for indexing for Financial Case indexed source

-   **Version 4.5.0 - April 2026**

    Updated: FSO now uses the native CSM Case Type Selector with Agent and User Criteria support, replacing custom extension logic and legacy components to reduce maintenance overhead and standardize case type handling across all user types.

-   **Version 4.4.0 - March 2026**

    Updated: Updated the read-only option to 'Strict Read Only' for read-only fields

-   **Version 4.2.2 - December 2025**

    Fixed: Playbook Engine Configuration: Disabled Process Automation Designer \(PAD\) engine for the Commercial Auto Claim playbook to resolve processing issues and improve playbook execution reliability.

-   **Version 4.2.1 - August 2025**

    Changed: Included additional translations to support localization for Q4.

-   **Version 4.1.3 - February 2025**
    -   Removed:
        -   Removed 'Insured Property' from the Property Incident table.
        -   Removed 'Claim fraud decision', 'Claim validation decision', and 'SIU review' from the Commercial Claim Base table.
-   **Version 3.4.1 - November 2024**
    -   New:
        -   Added "sn\_ins\_claim\_cml.flow\_executor"\(Flow Executor role\) which is going to be used to run all flows/subflows. It contains the "sn\_bom.flow\_executor" and "sn\_ins\_claim\_cml.manager" roles.
        -   New script include "FinancialSandboxUtil" which is sandbox enabled has been added.
        -   UX page properties have been added to the claim summary page.
        -   Added UX client scripts\(property\_description/text\) On Claim Summary Page.
        -   Added UX client scripts\(property\_description/text\) on Claim Commercial Property Incident Workspace.
    -   Changed:
        -   Flows and subflows have been updated to run as Flow executor instead of System user:
            -   Commercial Adjuster Task Form With Wait Condition.
            -   Commercial Claim Services Document Decision.
            -   Update claim case on SIU task updates.
            -   Claim work notes - updates for settlement.
            -   Claims Instruction list.
            -   Generate Policy Snapshot for Commercial Auto.
            -   Claim policy case - PB activity.
            -   Claim triage decision.
            -   Update commercial auto claim case.
            -   Claim fraud decision.
            -   Claim validation decision.
        -   CommercialAutoClaimAdjusterTaskAjax, AutoIncident, AutoIncidentDAO, AutoClaimTaskDAO, ClaimProfileExtensionPointImpl has been made as Sandbox enabled as false.
    -   Removed:
        -   Removed UX client scripts \(property\_description/label\) on Claim Commercial Property Incident Summary Page.
        -   Removed UX client script \(heading\_1/label\) on Claim Commercial Property Incident Workspace.
        -   Removed contributor viewer role from processor and adjuster.
-   **Version 3.3.0 - August 2024**
    -   New: Added extension point so that we can use the new fields under claim profile
    -   Removed: Removed header component from existing landing pages
-   **Version 3.2.0 - May 2024**
    -   New: Migrated data from FSO service category \(sn\_bom\_service\_definition\_category\) table to CSM service category\(sn\_csm\_case\_types\_service\_category\) and relationship tables
    -   Changed: Modified configuration for localization support
-   **Version 3.1.0 - February 2024**
    -   Changed:
        -   Upgraded snc-app-parent version to 5.1.0.16
        -   Modified configuration for localization support
-   **Version 2.0.1 - December 2023 \(Vancouver\)**
    -   New:
        -   Added sn\_ins\_claim\_cml.manager role to sn\_ins\_claim\_cml.admin
        -   Added FRISSObjectExtensionPoint extension to get claim objects
    -   Removed: Removed the sn\_ins\_claim\_cml.auto\_property\_user role
-   **Version 2.0.0 - November 2023**
    -   New:
        -   Added new table Property Incident
        -   Added new activity claim Injury in Commercial auto claim case playbook
        -   Added new action and subflow to trigger adapter flow via spoke selector.
        -   Added new flow to create policy snapshot when case is created
        -   Added archive rule for Commercial auto claim case table
    -   Changed:
        -   Moved the Insurance policy and Incident date field to the details section from the incident details section
        -   Moved product model demo data from 'sn\_bom\_b2b\_ins\_policy\_model' table to 'sn\_ent\_b2b\_ins\_policy\_model' table
-   **Version 1.4.0 - August 2023**
    -   Business features addressed as part of this release:

        -   Introduced new UX experience for claims adjusters using Claims Workspace view
        -   Introduced new claim summary page for claims users
        -   Updated fraud score view experience by introducing a new Fraud score page for claims users
        Specific modifications to the application are as follows:

        -   New
            -   Added 'Settle claim' UI action on adjuster task
            -   Added UX page properties for claim summary &amp; adjuster task record page
            -   Added 'summary\_page\_read' role to auto processor role
        -   Changed
            -   Deactivated personal auto adjuster playbook
            -   Updated claim case &amp; adjuster task form views
        -   Removed
            -   Removed 'sn\_bom.service\_viewer' role from FNOL &amp; adjuster roles
            -   Removed 'sn\_ins\_claim\_pers.auto\_viewer' role from write ACL on adjuster task
-   **Version 1.3.0 - May 2023**

    New:

    -   Added UX page properties for the Agent Assist on Voltron record page.
    -   Added role fraud\_score\_reader to processor and adjuster.
    -   Added UI action to generate fraud score if friss application is installed.
    -   Added localization changes.
-   **Version 1.2.1 - March 2023**

    Fixed: Fixed processor's permission to be able to add or edit claim coverages/claim properties/claim participants.

-   **Version 1.2.0 - February 2023**
    -   New:
        -   Added Agent Assist feature for commercial lines claim
        -   Added commercial claim processor role to the commercial lines claim adjuster
        -   Added "Add Task" button to create ad hoc tasks
        -   Added Ribbon and Header component for claim task
        -   Added Dynamic Related Record task component in the right contextual panel commercial case and adjuster task
        -   Added new state for adjuster task
        -   Added access to Processor persona on claim case, during claim validation stage
        -   Added automatic posting of work notes on case at different points of the claim case resolution process like approval of reserves/payments and claim settlement
    -   Changed:
        -   Made the Short Description field for claim task as mandatory
        -   Made the priority field editable for claim case
        -   Modified landing page for adjuster, processor,manager
        -   Modified ordering of UI actions
-   **Version 1.1.0 - November 2022**
    -   New:
        -   Added validation for commercial lines claims
        -   Added claim manager group
        -   Added adjuster role to claim manager
        -   Added new landing page for claim manager
        -   Added approval module for manager
        -   Added claim reserve and payment approval process
        -   Added mapping for activity definition on update action
    -   Fixed:
        -   Fixed dark theme issues
        -   Fixed claim closure issues for SIU review
    -   Changed:
        -   Renamed table lable from Commercial Auto Claim Service to Commercial Auto Claim Case
        -   Modified the content and layout for the Adjuster landing page
-   **Version 1.0.0 - August 2022**
    -   Commercial Lines Claims empowers carriers to digitize any commercial claims process end-to-end. Eliminate paper files and update claims in real-time, with the ability to work from anywhere.
    -   Automate the transfer of documents, data, payment, and approval requests with seamless work orchestration. Increase efficiencies and improve customer satisfaction with frictionless experiences.

