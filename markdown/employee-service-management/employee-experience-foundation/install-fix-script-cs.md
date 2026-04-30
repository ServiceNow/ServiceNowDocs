---
title: Install fix-script for Collaboration services for Zoom
description: Install the fix\_script\_start\_chat\_field\_decorator\_IT in the ServiceNow instance to display Start Zoom Chat field decorator/icon in the ticket to initiate a chat with the requester.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Collaboration services for Zoom, ServiceNow for Zoom, Zoom integrations, Unified Employee Experience, Employee Service Management]
---

# Install fix-script for Collaboration services for Zoom

Install the **fix\_script\_start\_chat\_field\_decorator\_IT** in the ServiceNow instance to display **Start Zoom Chat** field decorator/icon in the ticket to initiate a chat with the requester.

## Before you begin

Role required: admin

Visit the app store [Collaboration Services](https://store.servicenow.com/sn_appstore_store.do#!/store/application/adbeaa4a53742300ba5d0ef5d5dc34c2) and download the update set **fix\_script\_start\_zoom\_chat\_field\_decorator.xml**.

## Procedure

1.  Navigate to **System Update Sets** &gt; **Retrieved Update Sets** &gt; **Related Links** &gt; **Import Update Set from XML**.

2.  On the Import XML form, do the following.

    1.  Select **Browse**.

    2.  Select **fix\_script\_start\_zoom\_chat\_field\_decorator.xml** XML file.

    3.  Select **Upload** to upload the XML file.

3.  Navigate to **System Update Sets** &gt; **Retrieved Update Sets**.

4.  Select **Fix script to add start zoom chat field**.

5.  Select **Preview Update Set**.

6.  Select **Commit Update Set**.

    The Fix script to add start Zoom chat field decorator will be in Committed state.

7.  Navigate to **System Definition** &gt; **Fix Scripts**.

8.  In the **Name** search field, enter `Fix script to add start zoom chat field`.

9.  Click **Fix script to add start zoom chat field** fix script.

10. Select **Run Fix Script**.

    The ![Start Zoom chat](../images/icon-start-zoom-chat.png) icon is displayed as a field decorator in a record.


**Parent Topic:**[Configuring Collaboration services for Zoom](../concept/configure-sn-zoom.md)

