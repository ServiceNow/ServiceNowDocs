---
title: Tag Governance release notes
description: Version history for the Tag Governance application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-tag-governance.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - ITOM Visibility release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Tag Governance release notes

Version history for the Tag Governance application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.10.0 - June 2026**
    -   Removed: Removed the itil role from the tag\_admin role.
    -   Fixed: Improved the performance of the Tag Governance Insights dashboard.
-   **Version 1.9.0 - March 2026**
    -   New: A new filter type called policy type has been added to the 'Overall compliance status across CIs' widget on the Tag Governance Insights dashboard.
    -   Changed: The Tag Governance dashboard has been redesigned to display all data on the Tag Governance Insights dashboard, replacing the previous three-tab \(Overview, Policy View, and Efficacy\) structure. The new design provides improved visualization and navigation.
    -   Removed: The three-tab—Overview, Policy View, and Efficacy—structure of the Tag Governance dashboard has been removed.
    -   Known Issue:When users select the 'Tag Governance Insight' card on the Insights page of the Discovery Admin Workspace, the tag governance store app upgrade link does not redirect as expected.Refer to KB0561766 for the workaround.
-   **Version 1.8.0 - December 2025**

    Changed: Added granularity to the roles. No changes to the admin role.

-   **Version 1.7.0 - August 2025**
    -   New: New policy type-- "Tag Category--introduced to group similar tag keys using Regex.
    -   Fixed:
        -   The following issues were fixed for tag policy audits on GCP: Duplicate findings and incorrectly missing tag key.
        -   Tag Dashboard: Data is now populated for ratings and CI coverage trends widgets.
-   **Version 1.5.0 - November 2024**
    -   New: A dark theme for UI is now supported.
    -   Changed: Migrated the tag governance dashboard to a new and improved UIB interface.
    -   Fixed:
        -   Improved tag filter to handle cases where an item has more than one key.
        -   Implemented a cascade rule to delete all related records when a CI is deleted.
-   **Version 1.1.7 - August 2024**
    -   New: A dark theme for UI is now supported.
    -   Changed: Migrated the tag governance dashboard to a new and improved UIB interface.
    -   Fixed: Improved tag filter to handle cases where an item has more than one key.
    -   Implemented a cascade rule to delete all related records when a CI is deleted.
-   **Version 1.1.6 - February 2024**
    -   New:
        -   Enhanced Task Management: Introduced a new system property, allow\_new\_cert\_follow\_on\_task, allowing customization of task creation during policy runs for non-compliant CIs, reducing task redundancy.
        -   Tag Governance Admin Options: Added options during policy setup and in system properties for admins to control Tag policy compliance visibility in the overall CI compliance status and manage new task creation for non-compliant CIs.
        -   Table Cleaner for Run History: Implemented a table cleaner for sn\_itom\_tag\_policy\_run to periodically remove old runs, optimizing data management in Tag Governance.
    -   Changed:
        -   Tag Compliance Status Handling: Modified behavior to avoid unnecessary records in cert\_audit\_result table, improving system stability. The 'Save cert audit results' checkbox is clear, as the default setting for creating new Tag policies. Existing policies prior to upgrade are unaffected by this change, but they can be modified by the tag policy administrator as needed.
        -   Improved Popular Tags Logic: Enhanced popular tags calculation logic for quicker processing and reduced queries, contributing to improved system performance.
        -   Audit Optimization: Disabled audits for deletes in sn\_itom\_tag\_policy\_compliance\_listing and sn\_itom\_tag\_policy\_run\_listing tables to optimize system performance.
        -   CMDB classes support: Now the OS templates \(vm images, the cmdb\_ci\_os\_template class\) is also supported in tag policy evaluation
    -   Fixed:
        -   Data Pile-up Prevention: Addressed issues related to potential data pile-up and system stability by ensuring unnecessary records are not inserted into the cert\_audit\_result table.
        -   Event driven updates for AWS LB: Events from AWS Load Balancers \(ALB, NLB\) processed for tag changes correctly now
        -   Quality improvements: many minor product issues
    -   Removed: Audit Record Visibility: Hidden the link to Tag Gov policy results under Related Links when the 'Save cert audit results' checkbox is clear, signifying the exclusion from overall compliance status.
-   **Version 1.1.5 - May 2023**
    -   New:
        -   Dark theme support when Next Experience mode is enabled
        -   Event driven tag audit supported with Azure Resource Changes processing
    -   Fixed: Tag remediation supported with AWS Assume role to update tags of resources in member accounts in AWS cloud
-   **Version 1.1.3 - February 2023**
    -   Changed:
        -   Added a tool tip in the Remediation form to inform the users that the update tags to cloud feature is only available in the with ITOM Governance license.
        -   Access the configuration item \(CI\) properties in the key-value policy type script.
        -   For example, use ci.name.toString\(\) in the script to access the name of the CI.
        -   Performance improvements to the Update Compliance Listing status business rule
    -   Fixed:
        -   Issues that led to failed processing of the Azure tag removal events.
        -   Issues that led to failed processing of the Azure tag change events.
        -   Issues that prevented purging of the non-operational or retired CIs from the Tag dashboard causing performance issues.
        -   Issues in the Tag Governance Policies that prevented the audit tasks from getting the correct User or User Group assignments on policy audit failure.
        -   Issues that caused the Remediate Tags action to delete additional tags that aren't part of the failed audit.
-   **Version 1.1.0 - July 2021**

    New: Use the Tag Governance app to establish your tagging policies for all your IT Resources. Tags are the key-value pairs associated to your on-premises and cloud resources. Most companies have cloud tagging policies, this app helps to setup tagging policies consistently for all clouds and non-cloud resources too.


