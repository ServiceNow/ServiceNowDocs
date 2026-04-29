---
title: Log in to ITOM Mobile Agent
description: Log in to your ITOM Mobile Agent instance on the ServiceNow Agent app to manage alerts, incidents, and on-call schedules on the go.
locale: en-US
release: australia
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, ITOM Mobile Agent, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Log in to ITOM Mobile Agent

Log in to your ITOM Mobile Agent instance on the ServiceNow Agent app to manage alerts, incidents, and on-call schedules on the go.

## Before you begin

ITOM Mobile Agent must be installed, and the ServiceNow Agent app must be downloaded on your device. See [Install ITOM Mobile Agent](install-itom-mobile.md) and [Download the ServiceNow Agent app](download-agent-app.md) for more information.

You must also have your instance address, for example `nebula-dev.service-now.com`, or a QR code for the instance. If you don't have one, contact your admin.

Role required: srm\_manager, srm\_responder, or srm\_admin

## Procedure

1.  Tap the ServiceNow Agent icon \(![ServiceNow Agent app icon](../../service-reliability/image/sr-mobile-agent-app.png)\) on your device.

2.  Enter the address of your instance manually or with a QR code.

<table id="choicetable_o5x_tby_q2c"><tbody><tr><td id="d327989e120">

**Manual entry**

</td><td>

Replace `example.service-now.com` with the address of your instance. You don't need to include `service-now.com`. For example, enter `nebula-dev` for `nebula-dev.service-now.com`.

</td></tr><tr><td id="d327989e149">

**QR code**

</td><td>

Tap the QR code icon and scan the QR code.

</td></tr></tbody>
</table>3.  In the **Nickname** field, enter an alternative name for your instance.

    Alternative names can help you quickly navigate between different instances on your device.

4.  Tap **Save and log in**, enter your credentials, and then tap **Log in**.

    The app displays `Logged into <instance-name> as <username>` and the ITOM Mobile Agent **My work** tab.

    **Note:** You must be logged in to get push notifications about alerts and incidents. If you aren't, you only get email notifications.


## What to do next

Visit these links to start using ITOM Mobile Agent:

-   [Work with alerts in ITOM mobile](../concept/work-itom-mobile-alerts.md)
-   [Managing incidents and major incidents on mobile](../reference/itom-mobile-incidents.md)
-   [Working with On-Call Scheduling on mobile](../reference/itom-mobile-on-call-scheduling.md)
-   [Working with tasks on mobile](../reference/itom-mobile-tasks.md)

