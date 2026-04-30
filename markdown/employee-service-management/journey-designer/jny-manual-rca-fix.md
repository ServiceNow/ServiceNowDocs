---
title: Fix Restricted Caller Access \(RCA\) approval requests
description: After you install or upgrade to the latest Journey designer application from ServiceNow Store, you might encounter RCA approval messages requesting for an update in the access request.
locale: en-US
release: xanadu
product: Journey Designer
classification: journey-designer
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Installation and configuration overview, Journey designer, HR Service Delivery, Employee Service Management]
---

# Fix Restricted Caller Access \(RCA\) approval requests

After you install or upgrade to the latest Journey designer application from ServiceNow Store, you might encounter RCA approval messages requesting for an update in the access request.

## Before you begin

Role required: admin

## About this task

RCA requests that are generated after the installation of a newer version of the Journey designer application that are in the **Requested** state can be manually updated to **Allowed**. You can manually update the requests, or you can follow the directions in [KB1432208](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sys_kb_id%3D334062e0973b69d08a073cbe2153afb3) to upload and run a script to update RCA requests in bulk.

## Procedure

1.  Navigate to **All** &gt; **System Application** &gt; **Application Restricted Caller Access**.

2.  In the **Status** column, right-click **Allowed** and select **Filter Out**.

    A list of **Requested** RCA privileges is displayed.

3.  In the **Operation** column, double-click the entry you want to update.

    **Note:** If needed, change to the application that the request is for.

4.  Select **Allowed** in the **Status** list.

5.  Select **Update**.

    If there are multiple RCA requests, you must follow this task for each request.


**Parent Topic:**[Installation and configuration overview](../concept/jny-inst-config-overview.md)

