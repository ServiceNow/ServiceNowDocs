---
title: Install Notify connector for Microsoft Teams
description: Install and activate the Notify connector for Microsoft Teams plugin to be able to initiate a Microsoft Teams meeting directly from a Task record or via the Major Incident Workbench.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/setup-notify-ms-teams.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Plan your installation, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Install Notify connector for Microsoft Teams

Install and activate the Notify connector for Microsoft Teams plugin to be able to initiate a Microsoft Teams meeting directly from a Task record or via the Major Incident Workbench.

## Before you begin

Ensure you have installed the following plugins on your ServiceNow instance.

-   Notify plugin `com.snc.notify`.
-   Microsoft Teams Communications spoke plugin `sn_msteams_com_spk`.
-   Azure Active Directory User Mapping plugin `sn_now_azure`.

For more information about Microsoft Teams Communications spoke, see Microsoft Teams Communications spoke.

For more information about Notify, see .

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Enter `Notify Connector for Microsoft Teams` or `sn_notify_msteams` in the search field.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from the ServiceNow store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests on the store. For cumulative release note information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Select **Install**.


## What to do next

Integrate Notify connector for Microsoft Teams in ServiceNow instance.

-   To set up pre-published app \(Single Microsoft Teams tenant to single ServiceNow instance\), see [Integrate Notify connector pre-published app with Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/setup-notify-ms-teams-multi-tenant.md).
-   To set up self-configured app \(Single Microsoft Teams tenant to multiple ServiceNow instance\), see [Integrating Notify connector self-configured app with Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/setup-notify-ms-teams-single-tenant.md).

**Parent Topic:**[Plan your installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/plan-installation-ms-teams.md)

