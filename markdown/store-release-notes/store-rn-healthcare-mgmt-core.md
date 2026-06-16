---
title: Healthcare and Life Sciences Service Management Core release notes
description: Version history for the Healthcare and Life Sciences Service Management Core application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-healthcare-mgmt-core.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - Healthcare and Life Sciences release notes, ServiceNow Store release notes]
---

# Healthcare and Life Sciences Service Management Core release notes

Version history for the Healthcare and Life Sciences Service Management Core application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.5.0 - June 2026**
    -   This release delivers platform-wide accessibility \(WCAG 2.2 AA, 400% zoom/reflow\) and security and subscription-alignment hardening for HCLS Service Management Core.
        -   Security and Compliance
            -   WCAG 2.2 AA accessibility checkers: Added to HCLS Service Management Core to support automated accessibility validation.
            -   Automated WCAG 2.2 AA accessibility testing: Enabled across all Industry Verticals applications in this bundle.
            -   WCAG 2.2 AA compliance and 400% zoom/reflow support: Delivered across HCLS Service Management Core forms, lists, and workspaces.
            -   Access control hardening: Reviewed and corrected ACL role assignments to ensure every ACL retains at least one HCLS role, preserving access control after upstream scope changes.
            -   Non-Glide access control hardening: Audited and merged non-Glide ACL changes across HCLS application repositories.
            -   Subscription alignment — ACL gap fix: Corrected an access control gap so read access to dosage definition data is scoped to the dosage definition table rather than its parent request definition.
-   **Version 11.3.0 - March 2026**
    -   Fixed:
        -   The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. If you have custom client scripts that modify ServiceNow‑owned read‑only fields using g\_form.setValue\(\) or g\_form.clearValue\(\), refer toFor more information about granular read-only security options, see
        -   If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.
-   **Version 11.1.0 - December 2025**

    Fixed Installation errors

-   **Version 11.0.0 - August 2025**
    -   Changed: Moved CSM playbooks from HCLS Core to Pre-Visit Management.
    -   Fixed:
        -   Removed duplicate conditions/scripts from the field level ACLs.
        -   Corrected table access for HCLS admin, HCLS Manager, and HCLS Agent roles.
        -   Corrected HCLS Agent access to HCLS Cases and Patient Identifiers.
        -   Corrected role access on Service Model Foundation tables.
-   **Version 10.1.0 - May 2025**

    Changed: Added new OAuth Util Script to support retrieving Epic launch tokens from the user launch context when utilizing SMART on FHIR to authenticate with Epic's Hyperspace.

-   **Version 10.0.3 - February 2025**
    -   Improved Healthcare Organization creation process to simplify linking with associated Business Location.
        -   Previously admins would have to manually create a Business Location and associate it to the Healthcare Organization. Now when a Healthcare Organization is created the Business Location is automatically created and linked to the Healthcare Organization.
    -   Improved Healthcare Location to allow for a single Healthcare Location to be associated to multiple Healthcare Organizations.
        -   Previously a Healthcare Location could only be associated to one Healthcare Organization.
-   **Version 8.0.3 - February 2025**
    -   Updates made to give sn\_hcls\_patient for appropriate role access
    -   CSM query rules and Scripted ACLs added to the following tables.
        -   sn\_hcls\_patient\_identifier
        -   sn\_hcls\_pre\_auth\_header
        -   sn\_hcls\_pre\_auth\_diagnosis
        -   sn\_hcls\_pre\_auth\_item
        -   sn\_hcls\_claim\_diagnosis
        -   sn\_hcls\_pract\_location\_specialty
        -   sn\_hcls\_practitioner
        -   sn\_hcls\_practitioner\_facility
        -   sn\_hcls\_practitioner\_specialty
        -   sn\_hcls\_immunization
        -   sn\_hcls\_enrolled\_program
-   **Version 9.0.0 - August 2024**
    -   New: Use the new Patient identifier table to maintain and manage multiple identifiers such as patient MRN, social security number, and more.
    -   Changed: The Healthcare Workspace has received performance improvements to optimize loading times.
-   **Version 8.0.0 - May 2024**
    -   New:
        -   CSDM life cycle stage and status model have been adopted. The following tables now have the option to activate these mappings in the life cycle mapping table:
            -   sn\_hcls\_immunization
            -   sn\_hcls\_medication
            -   sn\_hcls\_enrolled\_program\_service
            -   sn\_hcls\_enrolled\_program
            -   sn\_hcls\_medical\_device\_install\_base\_item
        -   Clicking on the 'Activate' button in the life\_cycle\_mapping table will activate the CSDM fields population based on the mapping set in this table for all the tables in the instance. Legacy state fields can still be used.
        -   Model category and product instance identifier have been adopted from CSM.
-   **Version 7.1.0 - February 2024**
    -   New: Generate a summary from fields that you selected on a case record and quickly understand the case context by using the Now Assist case summarization within Workspace.
    -   Changed:
        -   The EMR Help application has been enhanced to provide requestors with the capability to create additional HCLS cases.
        -   The following updates have been made to the data model to take advantage of the core CSM install base item capabilities to track internal and external items:
            -   The following tables now extend Install Base Item instead of Healthcare sold product:
                -   Member plan\[sn\_hcls\_member\_plan\]&gt;
                -   Medication\[sn\_hcls\_medication\]&gt;
                -   Immunization\[sn\_hcls\_immunization\]&gt;
                -   Enrolled program\[sn\_hcls\_enrolled\_program\]&gt;
                -   Enrolled program service\[sn\_hcls\_enrolled\_program\_service\]
            -   This will have impact on the following columns:
                -   The hcls\_state field under table Enrolled program and Enrolled program service tables has been deprecated and the state field from the Install base table will be used going forward. Data has been moved from hcls\_state field to state field.&gt;
                -   The parent column now refers to the parent install base item to ensure that proper parent-child relation is maintained.&gt;
                -   The source\_task column under the Enrolled program and Enrolled program service tables is now tracked using the affected install base item m:m table.
        -   Healthcare locations and organizations realigned for multi-industry cases:
            -   Healthcare Organization \[sn\_hcls\_organization\] table is now a standalone table and no longer extends Service Organization.
                -   In some cases, custom tables might have a reference to Company/Service Organization which can contain the value of a healthcare organization. In scenarios where custom columns refer to Service Organization and have Healthcare Organization data, please reach out to Now Support for the migration script.
                -   Parent field now refers to Healthcare organization.
            -   Healthcare Location \[sn\_hcls\_location\] table is now a standalone table and no longer extends Service Organization.
                -   Healthcare Cases, Install Base records, and Sold Product records can no longer be created for Healthcare Locations. For existing records of these types, the Healthcare Location value will be replaced by the service organization value of the associated Healthcare Organization as a Healthcare location is always associated with a Healthcare Organization.&gt;
                -   Service\_organization\_parent field data has been cloned to parent location field. Parent location will be used going forward.&gt;
                -   Parent field data has been cloned to the organization field. Organization will be used going forward.&gt;
            -   Practitioner Location \[sn\_hcls\_practitioner\_facility\] table is now a standalone table and no longer extends Service Organization Member.&gt;
                -   In instances where a mapping exists between Healthcare Location and a Practitioner, the updated mapping will be between Healthcare Organization \(of the associated Healthcare Location\) and that Practitioner as Healthcare Location is now a standalone table and no longer extends the Business Location table.&gt;
                -   Service\_organization field data has been cloned to location field. Location will be used going forward.&gt;
    -   Removed:
        -   Consumable model \[cmdb\_consumable\_product\_model\] table has been removed from the data model.
        -   Healthcare sold product\[sn\_hcls\_sold\_product\] has been deprecated&gt;
        -   Payer plan table has been deprecated. Where this was previously used, medical insurance model is now used going forward.&gt;
        -   Medication product model \[sn\_hcls\_medication\_product\] table has been deprecated. Where this was previously used, Medication Model \[sn\_ent\_medication\_model\] table is now used going forward.&gt;
        -   Vaccine product \[sn\_hcls\_vaccine\_product\] table has been deprecated. Where this was previously used, Vaccination model \[sn\_ent\_vaccination\_model\] table is now used going forward.
-   **Version 5.0.2 - January 2024 \(Vancouver\)**

    Security fix.

-   **Version 2.5.6 - January 2024 \(Utah\)**

    Security fix for Service Portal.

-   **Version 2.3.4 - January 2024 \(Tokyo\)**

    Security fix for Service Portal.

-   **Version 5.0.0 - November 2023**
    -   Changed:
        -   Care specialities have been introduced and aligned to practitioners. A form view has been provided in Workspace and navigation is available from the List Menu.
        -   Observations and conditions have been linked to appointments.
        -   Practitioner locations and care specialities have been aligned.
-   **Version 2.5.4 - September 2023 \(Utah\)**

    Fixed: Issue causing slow ACL and response time.

-   **Version 2.3.2 - September 2023 \(Tokyo\)**

    Fixed: Issue causing slow ACL and response time.

-   **Version 4.0.2 - August 2023**

    New: Updated Patient details view now displays Patient 360 as an overview tab.

-   **Version 2.5.1 - May 2023**
    -   New:
        -   Healthcare location table updated to support optimized clinical resources and personnel across locations by configuring the new Codeset Locations \[sn\_hcls\_codeset\_location\]table
        -   Contacts of accounts can now be configured to open healthcare cases on the CSM portal for HCLS-B2B2C cases
    -   Changed: Serial number field added to the Medical device install base item \[sn\_hcls\_medical\_device\_install\_base\_item\] table
-   **Version 2.4.0 - February 2023**
    -   New:
        -   The following tables were added to the Healthcare and Life Sciences data model for updated claims management:
            -   Pre-authorization item \[sn\_hcls\_pre\_auth\_item\] table
            -   Pre-authorization diagnosis \[sn\_hcls\_pre\_auth\_diagnosis\] table
            -   Claim diagnosis \[sn\_hcls\_claim\_diagnosis\] table
    -   Changed:
        -   Updated the Patient \[sn\_hcls\_patient\] table for storing additional patient information
        -   Updated the Claim header \[sn\_hcls\_claim\_header\] and Pre-authorization request \[sn\_hcls\_pre\_auth\_header\] tables to further improve claims management
-   **Version 2.3.1 - December 2022**

    Changed: Upgraded to the updated ServiceNow AI Platform capabilities enabling reduction in the package size of the ServiceNow Store applications with the removal of the redundant folders and their contents.

-   **Version 2.3.0 - November 2022**
    -   New:
        -   Enabled accounts and contacts for use within the Healthcare and Life Sciences Service Management Core application
        -   Added sn\_hcls.customerservice\_agent role and expanded sn\_hcls.manager role to enable customer service agents and managers to create and manage healthcare cases for accounts and contacts
        -   Support for clinical devices in the Healthcare and Life Sciences data model
-   **Version 2.2.0 - August 2022**
    -   New:
        -   Improvements in role-based access to healthcare cases, tasks, and data
        -   Domain separation support in Healthcare and Life Sciences Service Management Core
-   **Version 2.1.0 - May 2022**
    -   New:
        -   Added new tables Dosage specification \[sn\_hcls\_dosage\_specification\], Dosage variable \[sn\_hcls\_dosage\_variable\], and Dosage definition \[sn\_hcls\_dosage\_definition\] for specifying medication dosage within a program
        -   Added new table Appointment participant \[sn\_hcls\_appointment\_participant\] for managing multiple participants within an appointment
        -   Added new table Source system \[sn\_hcls\_source\_system\] for storing source system and destination information to support external integrations
    -   Changed:
        -   Updated the Healthcare and Life Sciences data model and business logic around consent management
        -   Updated the Healthcare code set \[sn\_hcls\_code\_set\] table for storing code set system information
        -   Healthcare cases now have the Patient field listed as optional
-   **Version 2.0.0 - February 2022**
    -   New: Configurable Patient Portal that will allow patients to manage or request healthcare services, schedule immunizations, manage upcoming appointments, view household member information, and interact with care teams
    -   Changed: Consolidated Workspace landing page for agents to provide cohesive view and manage all types of patient requests
-   **Version 1.4.0 - October 2021**

    Changed: Updated the Healthcare and Life Sciences data model to support the Patient Support Services application.


