---
title: Install Notify connector for Microsoft Teams
description: Install and activate the Notify connector for Microsoft Teams plugin to be able to initiate a Microsoft Teams meeting directly from a Task record or via the Major Incident Workbench.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Plan your installation, Integrating ServiceNow with Microsoft Teams and Microsoft 365, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Install Notify connector for Microsoft Teams

Install and activate the Notify connector for Microsoft Teams plugin to be able to initiate a Microsoft Teams meeting directly from a Task record or via the Major Incident Workbench.

## Before you begin

Ensure you have installed the following plugins on your ServiceNow instance.

-   Notify plugin `com.snc.notify`.
-   Microsoft Teams Communications spoke plugin `sn_msteams_com_spk`.
-   Azure Active Directory User Mapping plugin `sn_now_azure`.

For more information about Microsoft Teams Communications spoke, see [Microsoft Teams Communications spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/msteams-comm.md).

For more information about Notify, see [Notify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/notify-landing-page.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Enter `Notify Connector for Microsoft Teams` or `sn_notify_msteams` in the search field.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from the ServiceNow store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests on the store. For cumulative release note information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Select **Install**.


## What to do next

Integrate Notify connector for Microsoft Teams in ServiceNow instance.

-   To set up pre-published app \(Single Microsoft Teams tenant to single ServiceNow instance\), see [Integrate Notify connector pre-published app with Microsoft Teams](../concept/setup-notify-ms-teams-multi-tenant.md).
-   To set up self-configured app \(Single Microsoft Teams tenant to multiple ServiceNow instance\), see [Integrating Notify connector self-configured app with Microsoft Teams](../concept/setup-notify-ms-teams-single-tenant.md).

**Parent Topic:**[Plan your installation](../../sn-teams/concept/plan-installation-ms-teams.md)

