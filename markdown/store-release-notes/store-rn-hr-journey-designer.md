---
title: Journey designer release notes
description: Version history for the Journey designer application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-journey-designer.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Journey designer release notes

Version history for the Journey designer application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 7.4.0 - June 2026**
    -   New:
        -   AI model updates — Knowledge Transfer document grouper and Journey Summarization for Manager have been upgraded to the latest third-party models with improved defaults.
        -   Security &amp; access controls — Application administration documentation updated with new security directives; ACL and scoping analysis completed for Journey Designer, Journey Accelerator, and related apps.
    -   Customer-impacted fixes:
        -   NOW Mobile task visibility — Journey tasks are now fully accessible within the mobile app regardless of which navigation path is used.
        -   Task due date persistence — Due dates are now reliably stored and reflected on the task record immediately after creation.
        -   Record Producer error handling — Aborting a record producer submission no longer surfaces a misleading error from the Journey bulk request banner.
    -   Other fixes:
        -   Knowledge Transfer — Post-completion sharing now works as expected; access controls prevent unauthorized admin visibility into restricted transfers; manager notifications after KT initiation have been made more informative; the KT flow is now resilient when certain lifecycle stage settings are turned off.
        -   Accessibility \(WCAG 2.2\) — High-zoom usability has been improved across several Journey Designer surfaces, including button visibility, header behavior, and form control rendering. Journey details page and configuration form screen reader issues have also been addressed.
        -   RCA &amp; COE — Journey configuration now correctly propagates RCA records; a privilege status mismatch in a scheduled script has been corrected; HR Lifecycle COE deactivation no longer fails due to scope restrictions.
        -   Pre-hire Banner — An underlying configuration issue that prevented the banner from rendering has been resolved.
        -   Localization — Template title strings are now constructed in a translation-friendly way; several UI labels that remained in English regardless of locale have been corrected.
        -   Performance — Opening a New Hire Onboarding journey is now noticeably faster, consistently falling within acceptable load time thresholds.
-   **Version 7.3.3 - April 2026**
    -   Fixed:
        -   Journey Summary accuracy dropped
        -   Manager draft view missing empty state
        -   Task template for type "Add a catalog request", "Request a knowledge transfer" and "Add an order guide"
-   **Version 7.3.2 - March 2026**
    -   New:
        -   Added journey knowledge transfers for offboarding scenarios
        -   With Now Assist for HRSD, an agentic workflow template is available that can summarize documents from Sharepoint and automatically create knowledge transfers
    -   Notable fixes:
        -   Fixed error message displayed when sending a personalized message
        -   Fixed issue where requests can't be opened
        -   Fixed URL for journeys
        -   Fixed "Due soon or Overdue" incorrectly appearing on Completed Approval tasks
        -   Fixed to support Closed incomplete and Cancelled closure states for tasks in the Journey
        -   Resolving errors when pre-hire opens a task
        -   Various security, cosmetic, and accessibility improvements
-   **Version 7.2.5 - January 2026**
    -   Fixed:
        -   Fixed issue where bulk task completion was not working due to misconfigured ACL
        -   Fixed issue where tasks would not display in mobile
        -   Fixed issue where managers do not have access to single score reports on journey home page
        -   Fixed issue where stages are not displayed for employees on JA-only journeys
-   **Version 7.2.2 - December 2025**
    -   New:
        -   Increased flexibility for managers to personalize journeys
            -   Manager \(Journey accelerator\) tasks can now be slotted into Lifecycle Event activity sets on Journey Details Page
            -   Manager \(Journey accelerator\) stages can now be re-ordered among Lifecycle Event activity sets on Journey Details Page
        -   Draft/publish capabilities for manager tasks when in Journey edit mode
        -   New Journey Accelerator task types \(Catalog Item, Automated Order Guide\) allow managers to add service requests to journeys
    -   Fixed:
        -   Fixed issue with breadcrumb widget breaking on sn\_doc\_task records
        -   Fixed issue where Journey page was not reflecting correct progress after upgrades to Y release
        -   Fixed issue with decorative icons missing aria-hidden attribute
        -   Fixed issue with translations not showing properly on My Journeys page sort-by filter
        -   Fixed issue with text overflow in Journey creation flow when translated to Swedish
        -   Fixed issue with "Update journey progress with count for overdue tasks" schedule job creating additional flow contexts
        -   Fixed issue with uploading large attachments in Journey accelerator tasks
-   **Version 7.1.8 - November 2025**
    -   Fixed:
        -   Issue causing security access issues with various fields in the Requested items list \[sc\_req\_item\] list
        -   Issue where journey configurations may not be displayed on journey creation page when they are Lifecycle Events only \(and do not include a Journey Accelerator plan\).
-   **Version 7.1.6 - October 2025**
    -   Fixed:
        -   GenAI Security Fixes
        -   Improved performance for the "Journey Generation\_Amazon Bedrock" Gen AI skill
-   **Version 7.1.3 - September 2025**
    -   New: Support for the "Generate onboarding ramp-up plan" Agentic workflow available with Now Assist for HRSD.
    -   Fixed: Fixed issue where Journey Bulk Tasks \(Catalog item and order guide\) were intermittently not getting completed.
-   **Version 7.0.2 - August 2025**
    -   New:
        -   Introduces a new "Pre-hire" role when Explicit Roles is installed. The role can be optionally assigned during onboarding. This will designate onboarding users as "external" users while giving them access to the Journey Details page and an Employee Center home page that's tailored for onboarding.
        -   Journey owners can cancel JA-only Journeys \(Journeys with no HR component\)
        -   Journey admins can configure whether to show the "Task Templates" and "Create a Journey for Your Team" widgets
    -   Changed: The "Show case to subject person" and "'Hide Activity Sets" flags on the HR Service are now honored for journeys
-   **Version 5.3.6 - May 2025**
    -   New:
        -   With the installation of Now Assist for HR Service Delivery \(HRSD\), an AI-generated summary appears on the Journey details page.
        -   With the installation of HR Service Delivery AI agent collection, rampup plans can be automatically generated using AI Agents. Managers can interact with Virtual Agent in portal to make changes to the plan and publish AI-generated stages once ready
    -   Changed: Improved user experience when viewing the journey details page.
    -   Fixed: Various usability and security improvements
-   **Version 5.2.0 - February 2025**
    -   New: Journey Generation \(enabled with Now Assist for HR\): Managers can leverage GenAI to create Journey Accelerator plans via text input from portal.
    -   Fixed: Various accessibility and usability bugs.
-   **Version 5.1.1 - November 2024**
    -   Changed: Improved script include and scope security
    -   Fixed: Various usability and accessibility issues
-   **Version 5.0.2 - September 2024**

    Added support for Vancouver.

-   **Version 5.0.1 - August 2024**
    -   New:
        -   Journey designer to support change of manager.
        -   OOB demo data of JD to support multiple journeys.
        -   Managers to share Journey task templates with other managers.
    -   Changed:
        -   Improved employee experience for Parental leave guide.
        -   Ability to trigger JA task due dates based on employee start date.
-   **Version 4.1.1 - May 2024**
    -   New:
        -   Journey Overview and Executive Journey View Next experience dashboards.
        -   LLM based VA Topic for creating Journey Accelerator task through task templates.
        -   LLM based VA topic to apply for Parental Leave of Absence
    -   Changed:
        -   Redirecting Journey Overview module to Next experience Journey Overview dashboard.
        -   Renamed Journey Usage module to Executive Journey View and redirecting it to Executive Journey View Next experience dashboard.
    -   Fixed: Minor updates
    -   Removed:
        -   Reports module under Journey Designer navigation is removed.
        -   Old Journey Overview and Journey Usage dashboards are removed.
-   **Version 4.0.3 - February 2024**
    -   New: Bulk management of Catalog items, Order guides, Approvals, Mark as complete type tasks. Update similar tasks in similar journeys in a single action.
    -   Changed: Learning Experience dashboard is migrated to the Next Experience.
-   **Version 3.0.8 - January 2024**
    -   Security updates, re-enforcing ACLs with a better security attributes/roles
    -   Bug fixes in journey configuration tabs
    -   Minor updates in the Journey designer admin console to correct possible issues when displaying some pages.
    -   Localization and accessibility improvements in journey pages.
-   **Version 3.0.3 - August 2023**
    -   New Journey Designer Admin Console - Access all the features that you need to configure and maintain journeys in a single intuitive experience. By using the admin console, you can consolidate;Lifecycle Events,;Journey Accelerator, and;Journey designer features for seamless configuration and management. The admin console also provides in-app enablement resources, help, and recommendations for delivering journeys.; ; ;
    -   Fixed:
        -   My Journeys - Next tasks will always redirect to the /esc portal
        -   Journey details page unable to handle date formats;
-   **Version 2.1.0 - May 2023**
    -   New: Migration script for migrating from Journey Accelerator v4.0 plans to Journey designer journeys \(applicable to customers using Journey Accelerator pre-Journey designer\).
    -   Fixed:
        -   Issue: Journey Accelerator-only journeys to not auto-assign mentor task templates.
        -   Issue: Hyperlinks not working in Journey Accelerator task templates.
        -   Performance improvements on the Journey designer pages.
        -   Resolved issues with translation of short descriptions on the tasks \(web and Now Mobile\).
        -   Usability issues and dark theme support.
        -   RCA updates.
    -   Changed:
        -   Journey Accelerator task description will appear in Completed version of the task.
        -   When duplicated stage name created, show error message to owner.
    -   Removed:
        -   Dependency on the Retry Handler Framework. If you are using Microsoft Exchange Online spoke for scheduling within Journey designer/Journey Accelerator, you will need to separately install.
        -   HR Taxonomy removed as a dependency.
-   **Version 2.0.5 - February 2023**
    -   New: Decentralized creation of journey templates allows admins to assign owners and approvers to plan configurations who can manage the journey templates in Employee Center.
    -   Changed: Celebratory messages for key moments like successfully completing or creating a journey
    -   Fixed: Performance improvements on how we track journey progress
-   **Version 1.0.9 - January 2023**
    -   Fixed
        -   Issues related to personalized message features
            -   When the journey header is modified, the personalized message will not pull the employee into the 'to:' field
            -   When a journey owner is also a mentor, the personalized message widget doesn't disappear after sending the email
        -   Security issues for report ACLs fixed
        -   Issues related to scope issues creating HR Services of fulfilment type 'Journey'
            -   HR services of the fulfilment type 'Journey' are created in the lifecycle events scope and therefore cannot be saved
            -   Other cross-scope issues related to HR services
-   **Version 1.0.5 - September 2022**

    Changed: With this patch release, Lifecycle Events for Enterprise is dependent on Journey designer v5.0.5 so if not already installed, the plugin will automatically install

-   **Version 1.0.3 - August 2022**

    Journey designer brings together the power of Lifecycle Events and the flexibility of Journey Accelerator, so that employees and managers have one unified experience for both curating and navigating a journey. Admins build journey configurations for employee transitions such as onboarding, offboarding, leaves of absence, career growth, and more. Managers create and modify their own journeys for team members. They can also add recommended learning \(powered by machine learning\) and send personalized emails to their employees from the journey. Customers using Lifecycle Events and/or Journey Accelerator can utilize their existing configurations to create journeys. New customers will need Lifecycle Events for Enterprise and Journey Accelerator \(will be automatically installed with Journey designer\) before building journey configurations.


**Parent Topic:**[ServiceNow Store - HR Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-hr.md)

