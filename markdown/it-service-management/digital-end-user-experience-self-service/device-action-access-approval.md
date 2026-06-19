---
title: Device action access and approval control
description: Approval-based access helps control how sensitive device actions are triggered and supports authorized use of actions that impact device performance or system behavior.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-self-service/device-action-access-approval.html
release: australia
product: Digital End-user Experience Self-service
classification: digital-end-user-experience-self-service
topic_type: concept
last_updated: "2026-05-20"
reading_time_minutes: 1
breadcrumb: [Device actions, Configure, Digital End-user Experience Self-service, Digital End-User Experience, IT Service Management]
---

# Device action access and approval control

Approval-based access helps control how sensitive device actions are triggered and supports authorized use of actions that impact device performance or system behavior.

Device actions that terminate processes, uninstall applications, or use significant system resources can impact device performance or system behavior. To limit unintended use, such resolutions can be configured as catalog items to add an approval step. Routing these actions through an approval step helps prevent users from triggering sensitive actions without authorization and creates an approval record alongside execution details. For information on configuring a remedial action as a catalog item, see [Create a remedial action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/create-remedial-action.md).

**Note:** Device actions are limited to once a calendar day for each device.

Device actions run using the Agent Client Collector \(ACC\) service account configured on the device — `_servicenow` on macOS and the configured service account on Windows. End users can't perform actions beyond the permissions granted to this account. The service account is configured at agent installation and can't be modified through device action settings.

