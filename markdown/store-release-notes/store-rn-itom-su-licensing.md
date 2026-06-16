---
title: ServiceNow ITOM/OT SU Licensing release notes
description: Version history for the ServiceNow ITOM SU Licensing content on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-su-licensing.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# ServiceNow ITOM/OT SU Licensing release notes

Version history for the ServiceNow ITOM SU Licensing content on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.13.0 - June 2026**
    -   New:
        -   Provides estimation for customers to plan migration to new 2026 ITOM SKUs viaReport Estimate ITOM Licensable CIs.
        -   Added new Non\_human\_identity category in license metadata to support upcoming new functionality.
        -   Added support for new ITOM Prime + Tanium Endpoint Management by adding SG-TaniumSN and SG-TaniumEndpoint under Licensable discovery sources for that specific new SKU.
    -   Fixed:
        -   Corrected regression caused by new SKUs shifting counts from containers to container images, so that old SKUs remain unaffected
        -   Corrected edge case involving a counted CI being reclassified from one category to another so that there remains only one historical list entry for such a CI
-   **Version 3.12.0 - March 2026**
    -   New:
        -   Added API Insight category usage under Visibility, enhancing visibility metrics for better analysis
        -   Added new bundle for ITOM Observability, providing comprehensive monitoring and management capabilities for ITOM solutions
        -   New chart for store App version monitoring, enabling tracking of application version updates.
    -   Changed: Added new countable discovery source KubernetesVisibilityAgent for Container and Container Images
    -   Fixed:
        -   Updated service mapping job exclusion condition when CI has invalid discovery source, ensuring accurate service mapping count
        -   Improved Exclusion job performance, reducing processing time and resource consumption
        -   Clean up of Unresolved Monitored Object in Historical CIs., resolving inconsistencies in historical configuration data
-   **Version 3.11.0 - December 2025**
    -   New: ITOM subscriptions are now linked from  Subscription Management to the ITOM Licensing Dashboard, to simplify the process of drilling down into the details of ITOM subscription consumption
    -   Fixed: End User Devices are now only counted in ITOM Health when a ServiceNow component \(currently, our Agent Client Collector\) is installed, aligning to the definition of this licensable resource category in the ServiceNow ITOM Subscription Unit Overview
-   **Version 3.10.2 - July 2025**

    Fixed:

    -   Use the new, improved Coral UI theme for the Licensing Dashboard.
    -   Optimized memory handling for large svc\_model\_assoc\_ci datasets prevents Out of Memory errors and ensures stable CI processing in ITOM Licensing.
-   **Version 3.10.0 - May 2025**
    -   New: ITOM Observability has been added to the ITOM Licensing Dashboard, enabling admins to visualize daily raw resource counts and the moving 90-day average SU consumption \(similar to other ITOM applications in the dashboard\).
    -   Changed: Simplified and improved the association of End User Customer Prem devices to parent classesThe association of CMDB classes to a licensable resource category has been improved so that, if a licensable resource category \(such as End Customer Prem Devices\) is associated with a CMDB class that is also a further descendent of a class that is associated with another licensable resource category \(such as Networking Devices\), the effective association of a CMDB class is via the closer CMDB parent class relationship or the direct association \(such as Media Gateway to End Customer Prem Devices instead of Networking Devices\).
    -   Fixed: Corrected order of applying the Discovery feature use across bundles for example, Pro/Enterprise, the Visibility and Discovery SKUs when present.
-   **Version 3.8.0 - February 2025**
    -   New: Added support for Observability Value Stream via Counting and Listing Job.
    -   Changed: Added support for counting Service Graph Connector usage without discovery installed.
    -   Fixed: Performance fix: Enabled visibility to historical CIs for customers with 1 million or more CIs.
-   **Version 3.7.0 - November 2024**
    -   Fixed:
        -   Improved Visibility Performance when Service Mapping is enabled.
        -   Common category count correction when OT License is present.
        -   Removed join dependency from the Exclusion List table to improve job performance.
        -   Exclude Server from DR site from the license count.
        -   Azure virtual desktop exclusion rule updated.
-   **Version 3.6.0 - August 2024**
    -   New: Exclusion for Windows 11 and Windows 12 VMs. All existing license usage definitions are now part of the app available on ServiceNow store.
    -   Changed: Updated the OT Count Conditions removing explicit dependency on OT Entity Column.
    -   Fixed: Attribute-based exclusion rule. New License Summary Defect. Improved Memory performance.
-   **Version 3.5.0 - May 2024**
    -   The Cloud Functions class \(cmdb\_ci\_cloud\_function\) has been moved from the PaaS category into a new category named FaaS \(Functions as a Service\) to allow for a different SU ratio than the rest of the CMDB CI classes in the PaaS category.
    -   When SU-based ITOM Discovery and ITOM Visibility subscriptions are present, usage will be applied to ITOM Visibility \(or a bundle that includes it\) first, to align with applying usage to bundle subscriptions first.
    -   Default SU ratios for instances without SU-based ITOM subscriptions have been updated.
    -   ServiceWatch has been removed as a licensable CMDB source.
    -   Consideration of CSDM Lifecycle Attributes instead of the Status \(install\_status\) attribute is now dependent on the csdm.lifecycle.migration.activated system property.
    -   New exclusion rules for Nutanix controllers, VxRails controllers, vSphere Clustered Services controllers, and Hyper-V storage.
-   **Version 3.4.0 - February 2024**
    -   New: OT Foundation app usage
    -   Changed:
        -   Counting of ACC-V and Event Management usage on DEX-managed EUDs is not applied to ITOM apps when DEX v2 subscription is present.
        -   Daily counts of CIs managed by SG-OT Excel Import are no longer filtered by last discovered/last scan date.
        -   Deduplication between KVM VM CIs and Server CIs factors in the reverse relationship direction set by KVM Discovery.
-   **Version 3.3.0 - November 2023**
    -   New:
        -   Support for new bundle Cloud Accelerate
        -   Added exclusion rule forGoogle Cloud Platform BigQuery Dataset Replicas
        -   Component Accessibility WCAG 2.1
    -   Changed: Plugin name changed to Servicenow ITOM/OT SU Licensing.
    -   Fixed:
        -   Performance Issue of Visibility Job.
        -   Removed Incorrect filter from ITOM License Summary Page
        -   Exclusion relationship between VM Server record and Virtualization Instance is reversed as per Discovery
-   **Version 3.1.0 - August 2023**
    -   New
        -   Auto-generation of Licensed CI listing for historical review
        -   Polaris-based dashboard with drill down into CI listings
        -   Support for CSDM Lifecycle Attributes
    -   Fixed
        -   Discovery source mapping issues for SG Connector sources
        -   Corrected deduplication logic that validates the related CI as countable, using sys\_object\_source rather than CI discovery\_source attribute
        -   DEX Plugin name update
        -   UCS Rack Mount Unit Exclusion
-   **Version 3.0.1 - May 2023**
    -   New: Support for ITOM SDX License
    -   Changed: Added standard SU filtering to Service Mapping portion of Visibility counts
    -   Fixed:
        -   Multiple bug fixes.
        -   Improved Exclusion Job Performance.
        -   DEX and HLA License added in exclusion table.
    -   Removed: Removed Discovery from Dummy License.
-   **Version 2.4.0 - February 2023**
    -   New:
        -   Added UCS Blade deduplication: UCS Blade CIs excluded from Server count based on Runs On::Runs relationship with a counted cmdb\_ci\_server \(or child\) CI
        -   Randomized daily usage count execution time, based on system property \(default off\)
    -   Fixed: Bug fixes
-   **Version 2.3.1 - December 2022**

    Minor fixes.

-   **Version 2.2.0 - September 2022**
    -   New: Support mixture of HLA and ITOM Health, as part of this feature we added a new value stream for HLA, we support HLA as an add on license to ITOM Health. Listing jobs and CI exclusion feature are being supported for HLA.
    -   Fixed:
        -   Improving performance of populating exclusion table.
        -   Azure Databricks exclusion rule has been modified to use object ID rather than name.
        -   Correcting the exclusion criteria for VM-server relationship, when one of them was not discovered in last 90 days
        -   Minor product fixes.
-   **Version 2.1.0 - August 2022**
    -   New:
        -   Support for license counts without subscription records. This feature provides ability for on-premises customers, non-production instances to track their ITOM license consumption.
        -   Dashboard for resource consumption and status against their purchased subscriptions, both latest daily counts and current 90-day average trends simultaneously.
    -   Fixed:
        -   Performance improvements in listing jobs.
        -   Removed non-existent roles.
        -   Minor product fixes.
    -   Known issues: If using the Store app on Rome, disable old scheduled jobs manually
-   **Version 2.0.0 - May 2022**
    -   New:
        -   Support for ITOM Governance based on a new value stream, providiing the ability to list the resources licensed within the ITOM Governance package, providing the exclusion/de-duplication logic similar to other value streams like visibility or health.
        -   A new IoT resource category has been added with cmdb\_ci\_iot, cmdb\_ci\_converged\_infra.
        -   Added new exclusion criteria for Hyper-V desktop VMs, in addition to ability to exclude Windows desktop VMs on vCenter and desktop VMs on Microsoft Azure Platform.
    -   Fixed:
        -   Old Licensing Jobs are not getting removed from the scheduler after installing the store application.
        -   License report is not proper when all CIs migrated from one domain to another in last 90 days.
-   **Version 1.1.0 - March 2022**
    -   New:
        -   Supports separate license counting for ITOM Discovery and ITOM Visibility when both licenses are present.
        -   Added new record category for Networking Devices Advanced.
    -   Fixed:
        -   Fixed bugs in ""Report ITOM Licensable CIs"".
        -   All the a la carte subcriptions \(even 0 usage\) are listed in usage account table.
-   **Version 1.0.6 - February 2022**
    -   New:
        -   Performs daily counts of ITOM-managed resources, recomputes averages over the last 90 daily counts, presents these counts, and offers listing of countable resources on-demand.
        -   ITOM licensing functionality has previously been part of family release, but now is delivered via this store app, so any new licensing requirements can be released more frequently.
        -   Application Menus \(ITOM License, OTM License\) and all their modules have been moved to store app. All script includes and scheduled jobs have been moved to the store app and their names are suffixed with “Store”.
        -   All existing licensing tables will stay in family release and are not moved to store app, so there are no data migration issues.
        -   Once the app is installed, all the old licensing scheduled jobs will be disabled via fix script and the new ones from the store app will be activated.

**Parent Topic:**[ServiceNow Store - IT Operations Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom.md)

