---
title: Combined Healthcare and Life Sciences Service Management Core release notes for upgrades from Washington DC to Australia
description: Consolidated page of all release notes for Healthcare and Life Sciences Service Management Core from Washington DC to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-washingtondc-australia/australia-washingtondc-healthcareandlifesciencesservicemanagementcore-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined Healthcare and Life Sciences Service Management Core release notes for upgrades from Washington DC to Australia

Consolidated page of all release notes for Healthcare and Life Sciences Service Management Core from Washington DC to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Healthcare and Life Sciences Service Management Core release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Healthcare and Life Sciences Service Management Core to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

During the upgrade to Washington DC, the Healthcare sold product \[sn\_hcls\_sold\_product\] parent table changes to Install base item \[sn\_install\_base\_item\] for the following tables:

-   Member Plan \[sn\_hcls\_member\_plan\]
-   Medication \[sn\_hcls\_medication\]
-   Immunization \[sn\_hcls\_immunization\]
-   Enrolled Program \[sn\_hcls\_enrolled\_program\]
-   Enrolled Program Service \[sn\_hcls\_enrolled\_program\_service\]

 In addition, the following tables have had their parent tables removed and are standalone tables:

-   Healthcare Organization\[sn\_hcls\_organization\]
-   Healthcare Location\[sn\_hcls\_location\]
-   Practitioner Location\[sn\_hcls\_practitioner\_facility\]

This reparenting enables customers to use the organizations and location tables for a broader set of use cases.

 Existing data is migrated in the following manner so that existing functionality isn’t impacted:

1.  Reference of location field in sn\_hcls\_immunization updated to use cmn\_location.
2.  All data is moved from Healthcare Sold Product to Install Base Item tables.
3.  Rows in the affected Install Base Item are populated based on the source\_task value from the Healthcare Sold Product.
4.  The state of sn\_hcls\_enrolled\_program and sn\_hcls\_enrolled\_program\_service are copied from hcls\_state.
5.  All data moves to the standalone tables of Healthcare Organization, Healthcare Location, and Practitioner Location.
    1.  The script creates records in the Business Location table for existing records in the Healthcare Organization table to form a 1:1 reference.
    2.  Records that refer to a service organization are updated with a reference to the appropriate business location.
    3.  Any practitioner who has a record in the practitioner location will have a record created in the Service Organization Member table with the appropriate business location.
    4.  Records that contain healthcare location data will contain the parent service organization of that healthcare location.

**Note:** You may experience a longer time for the upgrade to complete if your upgraded instance has a large number of records.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).

 If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Healthcare and Life Sciences Service Management Core.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Case summarization using Now Assist](https://www.servicenow.com/docs/access?context=hcls-now-assist&family=washingtondc&ft:locale=en-US)**

Generate a summary from the fields that you select on a case record to quickly understand the case context by using case summarization within Workspace.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Patient identifier table](https://www.servicenow.com/docs/access?context=hcls-patient-identifier-table&family=xanadu&ft:locale=en-US)**

Use the new Patient identifier table to maintain and manage multiple identifiers such as patient MRN, social security number, and more.

For instructions on migrating data from the patient table to the patient identifier table, please reach out to [Now Support](https://support.servicenow.com/now) for the fix script.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Healthcare and Life Sciences Service Management Core features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[EMR Help enhanced for HCLS case creation](https://www.servicenow.com/docs/access?context=submitting-cases-from-emr-systems&family=washingtondc&ft:locale=en-US)**

The EMR Help application has been enhanced to provide requesters with the capability to create additional HCLS cases. For more information on the EMR Help application, see [Exploring EMR Help](https://www.servicenow.com/docs/access?context=emr-help&family=washingtondc&ft:locale=en-US).

-   **[Data model further aligned with Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=hcls-serv-mgmt-core&family=washingtondc&ft:locale=en-US)**

The following updates have been made to the data model to take advantage of the core CSM install base item capabilities to track internal and external items:

    -   The following tables now extend Install Base Item instead of Healthcare sold product:
        -   Member Plan \[sn\_hcls\_member\_plan\]
        -   Medication \[sn\_hcls\_medication\]
        -   Immunization \[sn\_hcls\_immunization\]
        -   Enrolled Program \[sn\_hcls\_enrolled\_program\]
        -   Enrolled Program Service \[sn\_hcls\_enrolled\_program\_service\]
    -   This update impacts the following columns:
        -   The hcls\_state field under table Enrolled Program and Enrolled Program Service tables has been deprecated and the state field from the Install Base table is used going forward. Data is moved from hcls\_state field to state field.
        -   The parent column now refers to the parent install base item to ensure that proper parent-child relation is maintained.
        -   The source\_task column under the Enrolled Program and Enrolled Program Service tables is now tracked using the affected install base item m:m table.
-   **[Healthcare locations and organizations realigned for multi-industry cases](https://www.servicenow.com/docs/access?context=hcls-serv-mgmt-core&family=washingtondc&ft:locale=en-US)**
    -   The Healthcare Organization \[sn\_hcls\_organization\] table is now a standalone table and no longer extends Service Organization.
        -   In some cases, custom tables might have a reference to a Company/Service Organization that can contain the value of a healthcare organization. In scenarios where custom columns refer to Service Organization and have Healthcare Organization data, reach out to [Now Support](https://support.servicenow.com/now) for the migration script.
        -   Parent field now refers to Healthcare organization.
    -   Healthcare Location \[sn\_hcls\_location\] table is now a standalone table and no longer extends Service Organization.
        -   Healthcare Cases, Install Base records, and Sold Product records can no longer be created for Healthcare Locations. For existing records of these types, the Healthcare Location value is replaced by the service organization value of the associated Healthcare Organization as a Healthcare location is always associated with a Healthcare Organization.
        -   Service\_organization\_parent field data has been cloned to the parent location field. Parent location is used going forward.
        -   Parent field data has been cloned to the organization field. Organization is used going forward.
    -   Practitioner Location \[sn\_hcls\_practitioner\_facility\] table is a standalone table and no longer extends Service Organization Member.
        -   In instances where a mapping exists between a healthcare location and a practitioner, the mapping is updated to be between the healthcare organization \(of the associated healthcare location\) and that practitioner because Healthcare Location is now a standalone table and no longer extends the Business Location table.
        -   Service\_organization field data has been cloned to location field. Location is used going forward.

</td></tr><tr><td>

Xanadu

</td><td>

-   **[Workspace performance enhancements](https://www.servicenow.com/docs/access?context=hcls-using-workspace&family=xanadu&ft:locale=en-US)**

The Healthcare Workspace has received performance enhancements to optimize loading times.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Healthcare and Life Sciences Service Management Core features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   The Consumable Model \[cmdb\_consumable\_product\_model\] table has been removed from the data model.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Healthcare and Life Sciences Service Management Core features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   The Healthcare Sold Product \[sn\_hcls\_sold\_product\] table has been deprecated.

-   The Payer Plan \[sn\_hcls\_payer\_plan\] table has been deprecated. Where this table was previously used, the Medical Insurance Model table \[sn\_ent\_medical\_insurance\_model\] is used going forward.

-   The Medication Product Model \[sn\_hcls\_medication\_product\] table has been deprecated. Where this table was previously used, the Medication Model \[sn\_ent\_medication\_model\] table is used going forward.
-   The Vaccine Product \[sn\_hcls\_vaccine\_product\] table has been deprecated. Where this table was previously used, the Vaccination Model \[sn\_ent\_vaccination\_model\] table is used going forward.

For all deprecated tables, existing customer data is moved to the new tables when the upgrade occurs. Codeset records of type **Medication code** and **Form code** will be copied from the HCLS codeset to ENT model classification. Records in the new tables refer to codeset type records in the ENT model classification table.


</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Healthcare and Life Sciences Service Management Core.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Install Healthcare and Life Sciences Service Management Core by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

Install Healthcare and Life Sciences Service Management Core by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

Install Healthcare and Life Sciences Service Management Core by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Healthcare and Life Sciences Service Management Core we have noted them here.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Healthcare and Life Sciences Service Management Core we have noted them here.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Healthcare and Life Sciences Service Management Core, such as specific requirements or compliance levels.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Healthcare and Life Sciences Service Management Core we have noted them here.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Healthcare and Life Sciences Service Management Core we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Utilize the enhanced EMR Help application capabilities for requesters to create HCLS \(Healthcare and Life Sciences\) cases.
-   Use improved data alignment within the Healthcare and Life Sciences data model.
-   Leverage automated case summarization using the generative AI capabilities of Now Assist.

 See [Exploring Healthcare and Life Sciences Service Management Core](https://www.servicenow.com/docs/access?context=hcls-explore-core&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Promote accurate and comprehensive patient data management by leveraging multiple patient identifiers within the enhanced Healthcare and Life Sciences Service Management data model.
-   Utilize the performance updates within the healthcare workspace to optimize loading times.

 See [Exploring Healthcare and Life Sciences Service Management Core](https://www.servicenow.com/docs/access?context=hcls-explore-core&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

Healthcare and Life Sciences Service Management Core has received security enhancements in the Australia release.

 See [Healthcare and Life Sciences Service Management](https://www.servicenow.com/docs/access?context=hcls-service-mgmt-overview&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-washingtondc-australia/rn-combined-intro.md)

