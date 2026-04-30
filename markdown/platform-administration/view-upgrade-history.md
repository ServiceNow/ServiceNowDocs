---
title: View the upgrade history of a ServiceNow Store application
description: View the upgrade history of an application that you purchased and installed from the ServiceNow Store.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Installation considerations, Use, Legacy Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# View the upgrade history of a ServiceNow Store application

View the upgrade history of an application that you purchased and installed from the ServiceNow Store.

## Before you begin

Role required: admin, sn\_appclient.app\_client\_company\_installer \(can only install applications that match the instance company\), sn\_appclient.app\_client\_user, unified\_plugin\_read\_only

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search bar.

3.  Click the menu icon \( ![Menu icon](../image/menu-icon.png) \) on the application tile, and then click **View upgrade history**.

    **Note:** When customers upgrade to this new version of your application, the Deletes in your author\_elective\_update folder will be written as Skips in the Upgrade History entry for this application upgrade. Your users can browse the Skip list, and apply the changes on a case-by-case basis. Your customers have the option of setting com.glide.apps.include\_my\_deletes to false, which will skip writing Skip records as well.


**Parent Topic:**[Installation considerations](../concept/install-considerations.md)

