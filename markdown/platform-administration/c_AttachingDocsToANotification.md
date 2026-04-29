---
title: Document attachments on an email notification
description: You can attach documents and reports to email notifications by scripting or linking to the sys ID of the record.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Document attachments on an email notification

You can attach documents and reports to email notifications by scripting or linking to the sys ID of the record.

You can include all attachments from the source record with the notification. For example, if an incident update generates a notification, you can include all attachments from the incident record with the notification. To include all attachments from the source record, go to **Advance view** and select the check box for the **Include attachments** under **What will it contain** tab. The email messages, including attachments, cannot exceed the maximum email size. This size includes MIME encoding. For details on MIME encoding, see [Email service size restrictions](../../reference-pages/concept/c_EmailConfiguration.md#EmailService).

## Attaching documents with scripting

Using scripting, you can attach documents by linking to them, or you can attach various types of reports by specifying their IDs in the system.

## Linking to an attachment

You can add an attachment to a notification by linking to the attachment record in the message of the notification. Upon clicking the link, email recipients log in to the instance to view the attachment record.

Linking to attachment records in this fashion requires using email notification scripting. For example:

```
template.print ( 'Attachment: <a href="/sys_attachment.do?sys_id=' + now_GR. sys_id + '">' + now_GR. file_name + '</a>\n ' ) ;
```

## Attaching reports using the Sys ID

You can also attach various types of reports, including gauges, dashboards, and charts, to a notification. The scripts to attach these reports take the following syntax:

```
${report:X:Y}
```

where:

X is the type of report you want to attach \(reportID, gaugeID, dashboardID, or chartID\).

Y is the sys ID of the report, gauge, dashboard, or chart to be attached.

For example:

-   $\{report:reportID:&lt;abc123&gt;\}
-   $\{report:gaugeID:&lt;abc123&gt;\}
-   $\{report:dashboardID:&lt;abc123&gt;\}
-   $\{report:chartID:&lt;abc123&gt;\}

**Note:** Multilevel pivot reports can’t attach to email notifications.

**Parent Topic:**[Create an email notification](../task/t_CreateANotification.md)

