---
title: Install an update to a ServiceNow Store application
description: Install an update to an application that you purchased from the ServiceNow Store.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use, Legacy Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Install an update to a ServiceNow Store application

Install an update to an application that you purchased from the ServiceNow Store.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application with the filter criteria and search bar.

    If they are available, you can select customized versions to be installed.

3.  Next to the application listing, select the version to install.

4.  Click **Update**.

    **Note:** When customers upgrade to this new version of your application, the Deletes in your author\_elective\_update folder will be written as Skips in the Upgrade History entry for this application upgrade. Your users can browse the Skip list, and apply the changes on a case-by-case basis. Your customers have the option of setting com.glide.apps.include\_my\_deletes to false, which will skip writing Skip records as well.


**Parent Topic:**[Using Legacy Application Manager](using-legacy-application-manager.md)

**Related topics**  


[Developer and deployment permissions](https://www.servicenow.com/docs/access?context=t_AddADeveloper&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)

[System-managed developer and deployment roles](https://www.servicenow.com/docs/access?context=delegated_deployment_user_roles&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)

