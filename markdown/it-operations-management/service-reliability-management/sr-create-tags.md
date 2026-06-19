---
title: Manually create SRM tags
description: Add tags to classify, categorize, and add context to data. Service Reliability Management \(SRM\) imports tags and attaches them to services, alerts, and incidents. You can also manually create tags.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-reliability-management/sr-create-tags.html
release: australia
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SRM interface, Get started with Service Reliability Management, Exploring Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Manually create SRM tags

Add tags to classify, categorize, and add context to data. Service Reliability Management \(SRM\) imports tags and attaches them to services, alerts, and incidents. You can also manually create tags.

## Before you begin

Role required: srm\_admin, srm\_manager, or srm\_responder

## About this task

There are two ways that tags can enter the system and attach to an alert or incident. The first is automated but the last one is manual.

-   Imported from a third-party integration such as Datadog.
-   Using the tag icon in the header of a service, alert, or incident.
-   Added using the **Modify field values** action in an automation rule.

This task describes how to add tags to services and incidents in SRM. For information about managing alerts, see [Alerts in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/view-alert-workspace-itom.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You're taken to your SRM Home page.

    **Note:** If you use other Service Operations Workspace \(SOW\) applications, you may see the SOW Home page instead of the SRM Home page. The SOW Home page includes SRM alerts and incidents in its metrics.

2.  From the primary navigation, select **Services** or **Reliability tasks**.

3.  Open a service or incident.

4.  In the header, select the **Tag** icon \[Omitted image "icon-sr-tag.png"\] Alt text: Tag icon to add tags.

5.  Enter your tag in the pop-up window.

    Your tag is saved and appears below the Add Tag box alongside any existing tags.

6.  Select anywhere in the form to close the pop-up.

    **Note:**

    Tags are also shown under the description in the incident list view.


**Parent Topic:**[SRM interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-reliability-management/sr-navigate-interface.md)

