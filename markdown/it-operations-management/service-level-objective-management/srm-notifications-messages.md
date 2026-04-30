---
title: Notifications for breached error budgets
description: Details about the notifications that teams receive for breached error budget policies.
locale: en-US
release: zurich
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SLO Management reference, Service Level Objective Management, ITOM AIOps, IT Operations Management]
---

# Notifications for breached error budgets

Details about the notifications that teams receive for breached error budget policies.

## When notifications are sent

When a service or configuration item breaches its error budget policy and a notification destination is set, Service Reliability Management \(SRM\) sends a notification to the configured Microsoft Teams channel.

## Notification content

The message contains details about the breach to help team members learn about the issue and act. In Microsoft Teams, the message is titled `Error budget policy violation` and lists the following information:

-   Service level objective - Name of the service level objective \(SLO\), for example, `Navigation service availability 99.95`.
-   Service/CI - Name of the associated service or configuration time. Select the name to open the relevant service in SRM.
-   Policy name - Name of the error budget policy that was breached.
-   Error budget remaining - Percentage of error budget left at the time of the breach.
-   View SLO in ServiceNow - Link to view the SLO details in SRM.

## Sample notification

The following image is a sample notification in Microsoft Teams. It shows an error budget policy violation for the Cart service and details about the SLO and error budget remaining.

![Cart service has an error budget violation on its Cart service availability SLO.](../images/srm-msteams-notification2.png)

## Related documentation

See [Create a notification destination in SRM](../task/create-notification-destination.md) and [Create SLOs, SLIs, and error budget policies](../task/sr-create-slo-sli.md).

**Parent Topic:**[SLO Management reference](service-level-objective-management-reference.md)

