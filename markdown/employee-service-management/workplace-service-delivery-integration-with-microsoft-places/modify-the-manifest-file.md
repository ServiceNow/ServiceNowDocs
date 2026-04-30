---
title: Modify the manifest file
description: Modify the manifest file as part of WSD for Microsoft places application in Microsoft Teams.
locale: en-US
release: xanadu
product: Workplace Service Delivery Integration with Microsoft Places
classification: workplace-service-delivery-integration-with-microsoft-places
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure WSD for Microsoft places, WSD for Microsoft places, Workplace Service Delivery, Employee Service Management]
---

# Modify the manifest file

Modify the manifest file as part of WSD for Microsoft places application in Microsoft Teams.

## Before you begin

Role required: admin

Ensure to download the manifest file.

For more information on downloading the manifest files, refer to [Download manifest files](download-manifest-files.md)

## Procedure

1.  Unzip the manifest file.

2.  Open the .json file

3.  Follow the instructions to modify:

    1.  Search for **id** in the .json file and replace it with the **Application \(client\) ID**.

    2.  Look for **bots**,**Composeextensions**, and **activities** and remove them.

    **Note:** If the users want to open multiple portals, then the second part of the content url **sn\_now\_teams\_ms\_login.do** should be replaced with **n\_ms\_teams\_wsd\_ms\_login.do**.

4.  In the ServiceNow instance, navigate to **System properties**&gt; **sn\_now\_teams.portal.suffix**.

5.  Enter **wsp** in the value field.

6.  Save the .json file and zip all the files.


## What to do next

Follow up with upload the application process to complete the integration of WSD for Microsoft places application with Microsoft Teams.

