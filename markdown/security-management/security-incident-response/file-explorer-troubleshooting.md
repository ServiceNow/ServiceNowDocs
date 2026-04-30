---
title: File Explorer troubleshooting
description: The troubleshooting section can help you resolve some of the technical issues that you may encounter when setting up File Explorer component.Scheduled Jobs are automated jobs that are run to process the notifications from Microsoft SharePoint, ingest the files metadata into ServiceNow instance and renew the file repository subscriptions on a recurring schedule.Following are the available Microsoft SharePoint File Explorer connector system properties.Following are the Flow Designer subflows which are installed with Microsoft SharePoint File Explorer connector.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure File Explorer Component, Configure, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# File Explorer troubleshooting

The troubleshooting section can help you resolve some of the technical issues that you may encounter when setting up File Explorer component.

Refer to the following section on the scheduled jobs, system properties, and File Explorer flow designer subflows in detail.

**Parent Topic:**[Configure File Explorer Component](../../security-incident-response/concept/file-explorer.md)

## Scheduled jobs for File Explorer

Scheduled Jobs are automated jobs that are run to process the notifications from Microsoft SharePoint, ingest the files metadata into ServiceNow instance and renew the file repository subscriptions on a recurring schedule.

Scheduled Jobs are automated jobs which are run in the background to:

-   process the notifications from Microsoft Microsoft SharePoint.
-   ingest the files metadata into ServiceNow AI Platform instance.
-   renew the subscription with Microsoft SharePoint document library to receive notifications.

|Job|Description|
|---|-----------|
|Microsoft SharePoint File Explorer Connector: Process Notification|Runs every 30 seconds and responsible for reading the notifications which indicates any change occurred on the subscribed document library and marks the state of drives \(sn\_fe\_file\_repo\_drive\) as pending.|
|Microsoft SharePoint File Explorer Connector: Ingest Files|Runs every 30 seconds and primarily responsible for processing the drives \(sn\_fe\_file\_repo\_drive\) which are in pending state and pulls the delta file changes from the configured Microsoft SharePoint document library since the last pull.|
|Microsoft SharePoint File Explorer: Renew Subscription|Runs every 10mins and responsible for renewing the Microsoft SharePoint document library subscription a day before its expiry date. Usually, these subscriptions expire in 30 days.|

![Scheduled jobs](../../security-incident-response/image/fe-scheduled-jobs.png)

## Available File Explorer system properties

Following are the available Microsoft SharePoint File Explorer connector system properties.

|Property Name|Description|
|-------------|-----------|
|sn\_fe\_sharepoint.max\_retry\_count|Controls the frequency of attempts that Microsoft SharePoint connector application tried to pull the failed drive or renew the failed subscription. The default frequency value is set to 50.|
|sn\_fe\_sharepoint.retry\_after\_seconds|Time interval between each attempt to pull the failed drive or renew the subscription. The default value is set to 900 sec or 15 mins.|
|sn\_fe\_sharepoint.max\_subscription\_expiration\_time|Maximum subscription expiry period in number of days for Microsoft SharePoint. The default expiry period is set to 30 days.|

## File Explorer Flow Designer Subflows

Following are the Flow Designer subflows which are installed with Microsoft SharePoint File Explorer connector.

|Name|Description|
|----|-----------|
|Add Microsoft SharePoint Permissions|Grants edit permission for a specific folder to specific users.|
|Create Drive Subscription|Subscribes with a configured Microsoft SharePoint document library to receive notifications about any updates occurs on the document library.|
|Create New Microsoft SharePoint Folder|Creates a new Microsoft SharePoint folder under a given parent folder.|
|Delete Microsoft SharePoint Item|Deletes Microsoft SharePoint files and folders.|
|Download Microsoft SharePoint File|Returns the download URL of Microsoft SharePoint files|
|Get Files Metadata|Subscribes and pulls the changes from Microsoft SharePoint document library.|
|Move Microsoft SharePoint Item|Moves the Microsoft SharePoint files/folders to the destination folder|
|Open Microsoft SharePoint Item|Returns the web URL of Microsoft SharePoint file/folder to open in a browser.|
|Renew Drive Subscription|Renews the subscription with Microsoft SharePoint document library.|
|Create Folder Structure|Follows the folder template configurations and creates the folder structure on Microsoft SharePoint document library.|

