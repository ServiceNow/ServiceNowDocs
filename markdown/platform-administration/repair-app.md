---
title: Repair a ServiceNow application
description: Repair a ServiceNow application by reinstalling it.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Legacy Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Repair a ServiceNow application

Repair a ServiceNow application by reinstalling it.

## Before you begin

**Note:**

Legacy Application Manager is being prepared for deprecation. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

A known issue affects the use of bookmarks to access the Legacy Application Manager. For details about possible issues with accessing the Legacy Application Manager, see the [Deprecated Classic App Manager URL usage causes issues on instances running ZP5 / YP10 and above \[KB2804238\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2804238) article in the Now Support knowledge base.

A new Application Manager experience is available. The new experience simplifies the process of managing your licensed applications by consolidating them in one convenient location, displaying all applications, plugins, installed applications, and available updates. For more information, see [Application Manager](../concept/application-manager.md).

Role required: admin

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Select the **Installed** option.

    All the installed apps are displayed.

3.  Select an application tile to navigate to the details page of the application.

4.  In the **Quick Actions** list, select **Repair**.


## Result

The application and its dependencies are reinstalled.

**Note:**

-   When repairing an application with a customization, the customization is repaired as well, unless it's linked to a source control repository.
-   It is assumed the complete set of customizations for an application is within the application customization. When repairing, installing, or upgrading the underlying application or plugin that has an associated app customization, changes made outside of that application customization are overwritten.

    With a repair, all the files with sys\_update\_xml records are added to the remote update set. The remote update set is named with the format: "Repair/Upgrade app &lt;app scope name&gt; at &lt;timestamp&gt;".


**Parent Topic:**[Using Legacy Application Manager](../../../build/applications/task/using-legacy-application-manager.md)

