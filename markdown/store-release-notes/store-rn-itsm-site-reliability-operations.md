---
title: Site Reliability Operations release notes
description: Version history for the Site Reliability Operations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-site-reliability-operations.html
release: store
topic_type: reference
last_updated: "2024-01-04"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# Site Reliability Operations release notes

Version history for the Site Reliability Operations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 14.2.2 - January 2024**
    -   Changed: Changed access to become approval only to discourage further downloads and encourage downloads of the new Service Reliability Management app store app.
    -   Fixes related to UI.
-   **Version 14.2.1 - August 2023**
    -   Fixed:
        -   Issues related to condition builder in alert rule condition creation flow.
        -   Issue related to service selection on the Service Relationships page.
        -   Other minor fixes.
-   **Version 14.2.0 - November 2022**
    -   New:
        -   Added support to show dedicated business and technical services in Site Reliability Operations.
        -   Added localization support.
    -   Fixed:
        -   Refresh the Service Dependency page when a service is deleted.
        -   Update an On-call escalation tracking table as Accepted with Voice when a user accepts an assignment via voice call.
        -   Capture the Accepted state in an On-call escalation tracking table when a user accepts an assignment via Notification Device for voice.
        -   Stop further reminders when record assignment is rejected by a Notification device for primary email.
-   **Version 14.1.1 - May 2022**
    -   Fixed: Multiple bugs, including the following:
        -   Fixed an issue where user-created application services from Site Reliability Operations \(SRO\) were automatically set to Non-Operational after creation.
        -   Fixed an issue where the SRO administrator or manager could not view the On-Call calendar on SRO.
-   **Version 14.0.2 - December 2021**

    Fixed: Fixed the compatibility issues with On-Call Scheduling.

-   **Version 14.0.0 - July 2021**
    -   New:
        -   In addition to allowing teams to manage application services, Site Reliability Operations \(SR Ops\) now allows teams to manage technical services created from Dynamic CI groups in IT Operations Management. This allows teams to manage a group of CIs that do not map to an application service as if it were a service. These technical services are created by Central IT on behalf of the SRE team. The technical services can’t be created or deleted directly in SR Ops.
        -   Integration Actions are now Alert Rules. Alert Rules is a more comprehensive system allowing new types of rules to be created on services as well as configuration items \(CIs\) that impact services. Note: For Service + CI and CI options, the alert rule will only trigger if the CI is a direct child of the service or technical service \(anything more than one level deep will not trigger the rule\). For example, Dynamic Groups with nested Dynamic Groups will not trigger the rule.
    -   Changed:
        -   SR Ops has been steadily moving to a Workspace-only experience. This release finished that effort with only a few exceptions. Classic UI modules for managing Conditions, Actions, and Configurations for Alert Rules have been kept since these forms have fields that are not fully compatible with Workspace. All other classic UI modules have been removed and certain actions are no longer supported in classic UI. For example, creating new business and application services can no longer be done in classic UI.
        -   In an Alert Rule chain, the first alert rule condition is evaluated on every change to the alert so it may run later when that condition matches.
    -   Fixed:
        -   "Internal server error" is displayed when a user removes application services from the Relationships map
        -   "Internal server error" is displayed if a user adds a service relationship to an existing service with a duplicate name impacted CI "Service not available" error is returned on the home page if a team has thousands of members
        -   A support group is removed from the child service if a user creates a relationship between two existing services Not able to remove a service from the Service Relationships map after deletion of a service Service level Alert Rule records are not deleted from Alert Management Rule tables when service is deleted
        -   Remove from map functionality is not working properly between business and app services
        -   Service level Alert Rules are not deleted automatically when service is deleted SRO manager is not able to see the shifts from all the groups Various refresh issues
    -   Upgrade: Condition field is now mandatory on Alert Rules. If you have old Alert Rules that don't have conditions, they will still work.
    -   Uninstalling: Alert Rules: Uninstalling Site Reliability Operations will not remove alert rules that have been created in the system.
    -   Known Issues: EM Connectors: Issue when customers run on-premises using Oracle DB. Customers running on-prem with Oracle DB should not use this version of SR Ops. Workaround: None \(as of now\). If Notify is not set up properly, in Quebec the work notes on an alert can erroneously report that notifications have been sent when they have failed.
-   **Version 13.0.0 - April 2021**
    -   New:
        -   NewNew Integration Actions user experience.
        -   New action to send alerts notifications to an existing Slack channel.
        -   New EM Connector for Grafana.
        -   My on-call schedules added to workspace lists.
    -   Fixed:
        -   CI field of alert will now be populated when using Azure Monitor Push Connector.
        -   Users will now be warned when requesting a duplicate team.
        -   Fixed a looping issue when no on-call is setup and user rejects alert/incident.
        -   Fixed problems fully deleting Integration Actions.
    -   Known issues:
        -   EM Connectors: Issue when customers run on-premises using Oracle DB.
        -   Customers running on-prem with Oracle DB should not use this version of SR Ops.
-   **Version 12.0.0 - March 2021**
    -   New:
        -   SR Ops now supports Quebec.
        -   Updated the on-call escalation tracking mechanism.
        -   The alert action processing is switched at the backend to the new Alert Rules Management app.
    -   Fixed:
        -   The Delete Service offering link will no longer be available in the Overflow menu when Service Portfolio Management \(SPM\) is enabled.
        -   Users will no longer be able to delete a configuration item \(CI\) if the item is used anywhere else in SR Ops.
        -   Users will no longer be able to delete a condition item if the item is used anywhere else in SR Ops. When a user clicks the New button from the Integrations tab on the Service form, the Details tab will now appear.
        -   When a user changes the Action field on the Integration Actions form, the Configuration field will now be cleared.
        -   When the incoming change count is high, the Open Changes card count now gives the correct value.
        -   EM Connectors: Issue when customers run on-premises using Oracle DB. Customers running on-prem with Oracle DB should not use this version of SR Ops.Workaround: None \(as of now\).
        -   Azure Push Connector: The Configuration item\(CI\) on the alert is not getting populated. Workaround: Use the set service action to set the CI field on the alert.

**Parent Topic:**[ServiceNow Store - IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itsm.md)

