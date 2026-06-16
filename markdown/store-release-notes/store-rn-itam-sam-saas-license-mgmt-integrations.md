---
title: Software Asset Management - SaaS License Management release notes
description: Version history for the IT Asset Management Software Asset Management - SaaS License Management on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itam-sam-saas-license-mgmt-integrations.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 14
breadcrumb: [ServiceNow Store - IT Asset Management release notes, ServiceNow Store release notes]
---

# Software Asset Management - SaaS License Management release notes

Version history for the IT Asset Management Software Asset Management - SaaS License Management on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 17.4.0 - June 2026 \(Australia\)**
    -   In this version, the following enhancements have been made:
        -   Enhanced ACC-V capabilities
        -   Improved attachment handling in DocuSign consumption job
        -   Expanded Calendly integration with additional scope support
        -   Look Up Ideas Stream action in GraphQL schema
        -   Enhanced reference picker stability for samp\_sw\_subscription\_profile
        -   Improved reliability of SAM - SSO Okta update connected applications scheduled job
        -   Enhanced data validation with null checks for Azure integration approleassignment custom property
        -   Improved product data accuracy from Adobe APIs for samp\_sw\_subscription table imports
-   **Version 16.7.0 - June 2026 \(Zurich\)**
    -   In this version, the following enhancements have been made:
        -   Enhanced ACC-V capabilities
        -   Improved attachment handling in DocuSign consumption job
        -   Expanded Calendly integration with additional scope support
        -   Ensured user field population for old records with SSO resolution rules
        -   Optimized Look Up Ideas Stream action in GraphQL schema
        -   Enhanced reference picker stability for samp\_sw\_subscription\_profile
        -   Improved reliability of SAM - SSO Okta update connected applications scheduled job
-   **Version 15.4.1 - June 2026 \(Yokohama\)**
    -   In this version, the following enhancements have been made:
        -   Enhanced attachment handling in DocuSign consumption job
        -   Expanded Calendly integration capabilities with additional scope support
        -   Improved user field population for old records with SSO resolution rules
        -   Look Up Ideas Stream action in GraphQL schema
        -   Improved reference picker performance for samp\_sw\_subscription\_profile
        -   Enhanced reliability of SAM - SSO Okta update connected applications scheduled job
-   **Version 15.4.0 - May 2026 \(Yokohama\)**

    In this version, SAM admins can troubleshoot SaaS integration job failures more efficiently with guided error resolution. When a job fails at runtime, admins can select the Troubleshoot button to generate error details and access step-by-step resolution guidance — making it easier to identify and fix common configuration issues, reducing downtime and minimizing the need for escalation.

-   **Version 17.2.0 - April 2026 \(Australia\)**

    Requires Software Asset Management \(SAM Pro or SAM Enterprise\).

-   **Version 16.5.0 - April 2026 \(Zurich\)**

    Requires Software Asset Management \(SAM Pro or SAM Enterprise\).

-   **Version 17.0.5 - March 2026 \(Australia\)**

    In this version, several issues have been fixed across various SaaS and SSO integrations.

-   **Version 16.3.0 - March 2026 \(Zurich\)**
    -   Enhancements:
        -   Introduced improvements to the CrowdStrike integration to enhance overall functionality and reliability.
        -   Added support for configuring multiple data extensions for the Salesforce Marketing Cloud integration.
    -   Fixes:
        -   Resolved a performance issue in the Download Subscription job for the Workday integration.
        -   Fixed errors in the Download Subscription job for the Roadmunk integration.
        -   Addressed form-related issues in the Workday integration profile form.
-   **Version 15.1.1 - March 2026 \(Yokohama\)**

    In this version, enhancements for CrowdStrike integration have been introduced.

-   **Version 16.1.0 - February 2026 \(Zurich\)**
    -   Salesforce CRM integration: The integration profile now supports both Authorization Code and Client Credentials grant types.
    -   Adobe Cloud integration: The issue causing the Import Subscription job to fail after an upgrade, due to missing Organization ID values in existing profiles, has been fixed.
    -   DocuSign integration: Consumption job performance has been enhanced, and organization-level integration profiles now have stronger required-field validations.
-   **Version 15.1.0 - February 2026 \(Yokohama\)**
    -   Salesforce CRM integration: The integration profile now supports both Authorization Code and Client Credentials grant types.
    -   Adobe Cloud integration: The issue causing the Import Subscription job to fail after an upgrade, due to missing Organization ID values in existing profiles, has been fixed.
    -   DocuSign integration: Consumption job performance has been enhanced, and organization-level integration profiles now have stronger required-field validations.
-   **Version 14.1.0 - February 2026 \(Xanadu\)**

    In this version, the UI issues affecting the Publish button on the integration profile page have been resolved, and enhancements have been added to the Salesforce CRM integration playbook.

-   **Version 16.0.8 - December 2025 \(Zurich\)**
    -   Automate user resolution with AI for SaaS license management to increase efficiency and accuracy in subscription management.
    -   Implemented DataFeed API for accurate, reliable Docusign consumption tracking with improved scheduling and authentication.
    -   Enhancements have been made to ensure SSO scheduled jobs run efficiently and in parallel.
    -   Fixed UI breakage issues in the Action Payload Field form view and Permission type fields.
    -   Enhancements in Office 365 jobs to improve reliability and error handling.
    -   Connection validation issues resolved for Zoom and Smartsheet integrations.
    -   Resolved Refresh Looker subscription job issues.
-   **Version 15.0.19 - December 2025 \(Yokohama\)**
    -   Automate user resolution with AI for SaaS license management to increase efficiency and accuracy in subscription management.
    -   Implemented DataFeed API for accurate, reliable Docusign consumption tracking with improved scheduling and authentication.
    -   Enhancements have been made to ensure SSO scheduled jobs run efficiently and in parallel.
    -   Fixed UI breakage issues in the Action Payload Field form view and Permission type fields.
    -   Enhancements in Office 365 and Adobe scheduled jobs to improve reliability and error handling.
    -   Fixed issues in SAP Ariba integration for subscription creation and resolution.
    -   Connection validation issues resolved for Zoom and Smartsheet integrations.
    -   Resolved Refresh Looker subscription job issues.
-   **Version 14.0.12 - December 2025 \(Xanadu\)**
    -   Enhancements in Last Activity for Visio Online users.
    -   Resolved date-related error in Salesforce CRM profile publishing.
    -   Improved Adobe Cloud subscription processing.
    -   Fixed UI breakage issues in Action Payload Field view after plugin installation.
-   **Version 16.0.6 - August 2025 \(Zurich\)**
    -   This version includes several improvements and bug fixes:
        -   Support for the Microsoft 365 Dynamics profile type is added.
        -   License assignment and dual use handling for M365 is improved.
        -   Permission levels for Entra ID, Microsoft Dynamics 365, and other services are updated.
        -   Scheduled jobs for Office 365 and Adobe are improved.
        -   The UI issue with duplicate Publish buttons is fixed.
-   **Version 15.0.17 - August 2025 \(Yokohama\)**
    -   This version includes several key improvements and bug fixes:
        -   The SSO Application form has been updated with new improvements.
        -   Issues with page breaks on the integration page have been resolved.
        -   The duplicate Publish button on the integration profile page has been removed.
        -   Scheduled job issues related to Microsoft 365 and Adobe subscriptions following an upgrade have been fixed.
        -   The Salesforce download consumption subflow issue has been successfully resolved.
-   **Version 14.0.11 - August 2025 \(Xanadu\)**

    In this version:

    -   Enhancements are added in SSO Application Form.
    -   Integration page break issues are fixed.
    -   Duplicate publish button in profile page is resolved.
    -   Okta scheduled job issue related to scopes is fixed.
-   **Version 15.0.15 - May 2025 \(Yokohama\)**
    -   New:
        -   Gain complete visibility into the usage of all SaaS applications
        -   Discover and manage all paid or free SaaS applications, which are accessed via a browser and configured within the ServiceNow Agent Client Collector \(ACC-V\) product. Manage your shadow IT spend more effectively by viewing all the users who access these applications in the SaaS detection report. This report also shows the usage of these applications and how long each application has been used.
-   **Version 14.0.9 - May 2025 \(Xanadu\)**
    -   New:
        -   Gain complete visibility into the usage of all SaaS applications
        -   Discover and manage all paid or free SaaS applications, which are accessed via a browser and configured within the ServiceNow
        -   Agent Client Collector \(ACC-V\) product. Manage your shadow IT spend more effectively by viewing all the users who access these applications in the SaaS detection report. This report also shows the usage of these applications and how long each application has been used.
-   **Version 13.1.12 - May 2025 \(Washington DC\)**
    -   New:
    -   Gain complete visibility into the usage of all SaaS applications
    -   Discover and manage all paid or free SaaS applications, which are accessed via a browser and configured within the ServiceNow
    -   Agent Client Collector \(ACC-V\) product. Manage your shadow IT spend more effectively by viewing all the users who access these applications in the SaaS detection report. This report also shows the usage of these applications and how long each application has been used.
-   **Version 15.0.12 - March 2025 \(Yokohama\)**
    -   The Confluence Cloud connection template to support site-specific API calls for multi-site use cases is fixed.
    -   The alias update issue for Confluence Cloud integration is fixed.
    -   The issue of setting up of dynamic connection even when the Download activity is unchecked is fixed.
    -   The minimum permissions required for Microsoft Entra ID integration are updated.
    -   The issue where the Count on Cal record was not being added for entries that had the same software model and license metric but different workloads is fixed.
-   **Version 14.0.8 - March 2025 \(Xanadu\)**
    -   The need for additional Client ID and Client Secret while setting up Dropbox integration is removed.
    -   The Confluence Cloud connection template to support site-specific API calls for multi-site use cases is fixed.
    -   The minimum permissions required for Microsoft Azure AD integration are updated.
-   **Version 13.1.11 - March 2025 \(Washington DC\)**
    -   The need for additional Client ID and Client Secret while setting up Dropbox integration is removed.
    -   The Confluence Cloud connection template to support site-specific API calls for multi-site use cases is fixed.
    -   The minimum permissions required for Microsoft Azure AD integration are updated.
-   **Version 15.0.8 - February 2025 \(Yokohama\)**
    -   In this release, we're introducing:
        -   Simplified SaaS activation which allows to manage selected applications seamlessly with App v2.
        -   Security Permissions which allows to grant minimum required permissions for key SaaS use cases like subscription downloads, activity calculations, and reclamations.
        -   Enhanced Microsoft Licensing support for Microsoft 365 and Dynamics.
        -   Added license metrics for Sensor Subscription and Reserved Hourly Average Sensor for CrowdStrike.
-   **Version 14.0.7 - February 2025 \(Xanadu\)**
    -   Issue with download subscriptions job for multiple adobe integration profiles with Oauth connection type is fixed.
    -   Issue with confluence cloud Oauth token is fixed.
    -   Enhancements made to Crowdstrike integration to fetch product level usage information and to support recon against multiple license metrics.
-   **Version 13.1.10 - February 2025 \(Washington DC\)**
    -   Issue with download subscriptions job for multiple adobe integration profiles with oauth connection type is fixed.
    -   Issue with confluence cloud oauth token is fixed.
    -   Enhancements made to crowdstrike integration to fetch product level usage information and to support recon against multiple license metrics.
-   **Version 14.0.5 - November 2024 \(Xanadu\)**
    -   Fixed:
        -   Zendesk download subscription issue.
        -   Removed dependency on write scopes while pulling Box subscriptions.
        -   Zoom API rate limit issue.
        -   Software Subscriptions related list tab in integration profile page.
-   **Version 13.1.8 - November 2024 \(Washington DC\)**
    -   Fixed:
        -   Removed dependency on write scopes while pulling Box subscriptions.
        -   Zoom API rate limit issue.
        -   Software Subscriptions related list tab in integration profile page.
-   **Version 12.0.16 - November 2024 \(Vancouver\)**
    -   Fixed:
        -   The dependency on write scopes while pulling Box subscriptions is removed.
        -   Zoom API rate limit issue.
-   **Version 14.0.4 - August 2024 \(Xanadu\)**
    -   New Tableau integration is added.
    -   The Webex Activity Job issue is fixed.
    -   The SurveyMonkey integration is improved to support all types of user plans.
    -   The Microsoft 365 Update User Activity to account GCC/GOV subscription identifier is fixed.
    -   The Zendesk Download Subscription sub-flow issue is fixed.
    -   The empty user principal name issue for Facebook Integration is fixed.
    -   Security defects are fixed.
-   **Version 13.1.7 - August 2024 \(Washington DC\)**
    -   Fixed Webex Activity Job issue.
    -   Enhanced SurveyMonkey integration to support all type of user plans.
    -   Fixed Microsoft 365 Update User Activity to account GCC/GOV subscription identifier.
    -   Fixed Zendesk Download Subscription sub-flow issue.
-   **Version 12.0.15 - August 2024 \(Vancouver\)**
    -   Fixed Webex Activity Job issue.
    -   Enhanced SurveyMonkey integration to support all type of user plans.
    -   Fixed Microsoft 365 Update User Activity to account GCC/GOV subscription identifier.
    -   Fixed Zendesk Download Subscription sub-flow issue.
-   **Version 13.1.4 - May 2024 \(Washington DC\)**
    -   Fixes for the Event horizon field issue for Zoom integration.
    -   Replaced deprecated actions with V2 actions for all the integrations.
    -   Fixed Adobe/M365 import scheduled jobs inactive issue after installing SaaS plugins.
    -   Fixed Workfront Update User Activity scheduled job draft state issue.
-   **Version 12.0.13 - May 2024 \(Vancouver\)**
    -   Fixed multiple profile creation issues for Crowdstrike Integration.
    -   Fixed Zoom Webinar to pull only licensed users as subscriptions.
    -   Enhanced Github Update User Activity subflow to use the org event action to fetch activity details.
-   **Version 11.1.9 - May 2024 \(Utah\)**
    -   Enhanced Github Update User Activity subflow to use the Org Event action to fetch activity details.
    -   Fixed empty ACLs issue.
-   **Version 13.1.2 - March 2024**

    Shawdow SaaS Analytics dashboard issues are fixed.

-   **Version 13.1.0 - February 2024 \(Washington DC\)**
    -   Added Shadow SaaS analytics from browser activity report to discover and manage all SaaS applications accessed via a browser and configured within the ServiceNow Digital End-User Experience \(DEX\) product.
    -   Implementednew reports API GetM365AppUserDetail for desktop products to get weekly usage for Microsoft 365 subscriptions.
    -   Problem fixes.
-   **Version 12.0.10 - February 2024 \(Vancouver\)**

    In this release, a few issues are fixed.

-   **Version 11.1.6 - February 2024 \(Utah\)**

    In this release, a few issues are fixed.

-   **Version 12.0.7 - December 2023 \(Vancouver\)**

    With this release, the SSO Integrations scheduled jobs are running as expected after upgrading to Vancouver.

-   **Version 12.0.5 - October 2023**

    In the 12.0.5 version, UI issues on the chart layout for the Overlapping Usage Dashboard in the Software Management Workspace are fixed.

-   **Version 12.0.4 - August 2023**
    -   Fixed look up host details action for crowdstrike integration.
    -   Fixed security issues.
    -   Verified calendly integration without lastpass account.
    -   Updated Microsoft Dynamic 365 subflows to pull power apps subscriptions.
-   **Version 11.1.0 - May 2023 \(compatible with Utah\)**
    -   Fixes for Trello and Looker integrations
    -   Added Zoom webinar subscription management
    -   Added Reclamation flow for Roadmunk
-   **Version 10.0.8 - May 2023 \(compatible with Tokyo\)**

    Fixes for Smartsheet, monday.com, Microsoft Dynamics 365, Trello, and Zoom.

-   **Version 9.0.11 - May 2023 \(compatible with San Diego\)**

    Fixes on Zoom, Microsoft Dynamics 365, Trello, and Smartsheet spokes.

-   **Version 11.0.6 - March 2023**
    -   Retrieving the user subscriptions of all License Types supported by Miro.
    -   Fixed download subscriptions for monday.com integration.
    -   Fixed Subscription assigned field issue with Zoom integration.
    -   Updated Microsoft Dynamic 365 subflows to filter out unsupported identifiers.
-   **Version 11.0.4 - February 2023**

    Removed: In this release, the script files are deprecated from SaaS License Management Foundation, SaaS License Management Connection, and moved to SaaS License Management.

-   **Version 10.0.6 - January 2023 \(compatible with Tokyo\)**
    -   Fix for populating Publisher, Product, and Software model fields in subscription records.
    -   Removed the 'sn\_pad\_demo' plugin dependency.
-   **Version 9.0.10 - January 2023 \(compatible with San Diego\)**
    -   Fix for populating Publisher, Product, and Software model fields in the subscription records.
    -   Removed the 'sn\_pad\_demo' plugin dependency.
-   **Version 8.0.9 - January 2023 \(compatible with Rome\)**
    -   Fix for populating Publisher, Product, and Software model fields in the subscription records.
    -   Removed the 'sn\_pad\_demo' plugin dependency.
-   **Version 10.0.5 - September 2022 \(compatible with Tokyo\)**
    -   Fix in Crowdstrike for accurate CAL records calculation.
    -   Fix in Jira, Confluence Cloud for fecthing the groups for different connection alias.
    -   Fix in Sam workspace to populate Subflows in Survey Monkey, Confluence Cloud Integrations.
-   **Version 9.0.9 - September 2022 \(compatible with San Diego\)**

    Fix in Jira, Confluence Cloud for fecthing the groups of different connection alias.

-   **Version 8.0.8 - September 2022 \(compatible with Rome\)**

    Fix in Jira, Confluence Cloud for fecthing the groups of different connection alias.

-   **Version 10.0.2 - August 2022 \(compatible with Tokyo\)**

    New: In this version 10.0.2, Workday integration and fixes were added.

-   **Version 9.0.8 - August 2022 \(compatible with San Diego\)**

    Fixes

-   **Version 8.0.7 - August 2022 \(compatible with Rome\)**

    Fixes

-   **Version 5.0.10 - August 2022 \(compatible with Quebec\)**

    Removed: SAP SuccessFactors dependency from the SaaS Licence Management application is removed.

-   **Version 9.0.7 - July 2022 \(compatible with San Diego\)**

    Removed: SAP SuccessFactors dependency from the SaaS Licence Management application is removed.

-   **Version 8.0.6 - July 2022 \(compatible with Rome\)**

    Removed: SAP SuccessFactors dependency from the SaaS Licence Management application is removed.

-   **Version 5.0.9 - June 2022 \(compatible with Quebec\)**

    New: Added dependency of updated Software Asset Management integration with Salesforce CRM \(1.0.6\)

-   **Version 9.0.3 - April 2022 \(compatible with San Diego\)**

    New: In the Software Asset Management - SaaS License Management Integrations 9.0.3 version, new SaaS dependency is included.

-   **Version 8.0.3 - April 2022 \(compatible with Rome\)**

    New: In the Software Asset Management - SaaS License Management Integrations 8.0.3 version, new SaaS dependency is included.

-   **Version 5.0.2 \(compatible with Quebec\) - March 2022**

    New: Includes new SaaS dependency.

-   **Version 9.0.2 - February 2022**
    -   New: Added Crowdstrike integration spoke
    -   Changed: Updated version of Trello integration spoke
    -   Fixes
-   **Version 8.0.2 - January 2022**

    Fixed: Version 8.0.2 includes fixes for the GoTo spoke.

-   **Version 8.0.1 - December 2021**

    Fixed: Version 8.0.1 includes fixes for the Salesforce, Workplace from Facebook integrations.

-   **Version 8.0.0 - November 2021**
    -   New: In version 8.0.0, Rally, Looker, Workplace from Facebook, and SmartRecruiters integrations are added.
    -   Fixed: Some fixes are made in the Jira spoke.
-   **Version 7.0.1 - October 2021**

    Fixed: Fixes for the Confluence Cloud and Cisco Webex Meeting integration spokes

-   **Version 7.0.0 - August 2021**
    -   Use the ServiceNow SaaS License Management application to leverage the new improved user interface for existing integrations:
        -   GoTo
        -   Trello
        -   Confluence
        -   Monday.com
        -   Miro
        -   Cisco Webex Meetings
    -   Use the ServiceNow SaaS License Management application to integrate with the following applications:
        -   Cisco Webex
        -   Roadmunk
        -   Adobe Workfront
        -   Zendesk
        -   Microsoft Dynamics 365
-   **Version 6.0.3 - July 2021**
    -   Consumption-based reconciliation
    -   New improved user interface
    -   Subscriptions go through a reconciliation framework
    -   Office and adobe dashboards are now part of SaaS overview dashboard.
-   **Version 5.0.1 - May 2021**
    -   New: Integrate with Miro, Aha, Trello, Calendly, and monday.com
    -   Changed: Integrate with SurveyMonkey to track software subscriptions and reclaim unused licenses.
-   **Version 4.0.0 - March 2021**
    -   New: Integrate with Confluence Cloud, Salesforce Marketing Cloud, and SAP SuccessFactors.
    -   Changed: Integrate with Salesforce CRM to track software subscriptions and reclaim unused licenses for products such as Sales Cloud, Service Cloud, Platform, and Capability.
-   **Version 3.0.1 - February 2021**

    New: Integrate with GoToMeeting and GitHub applications. Retrieve and calculate user activity for Smartsheet applications.

-   **Version 2.0.0 - January 2021**
    -   The SaaS License Management feature of Software Asset Management provides visibility into SaaS and SSO usage data so you can immediately reclaim unused subscriptions. Reduce and optimize your SaaS spend.

        With this feature, you can:

        -   Create and manage direct integrations with SaaS applications.
        -   Create integrations with SSO providers to view subscription usage for all connected applications.
        -   View SaaS and SSO subscription usage and cost information on the SaaS License Management Overview dashboard.
        -   Reclaim user subscriptions that have limited to no activity.

