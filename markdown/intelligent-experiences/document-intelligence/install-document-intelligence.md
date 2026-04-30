---
title: Install Document Intelligence
description: You can install Document Intelligence \(sn\_docintel\) and Document Intelligence Admin \(sn\_docintel\_admin\) if you have the admin role. The sn\_docintel\_admin application installs related ServiceNow Store dependencies if they aren’t already installed.
locale: en-US
release: zurich
product: Document Intelligence
classification: document-intelligence
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Document Intelligence, Enable AI experiences]
---

# Install Document Intelligence

You can install Document Intelligence \(sn\_docintel\) and Document Intelligence Admin \(sn\_docintel\_admin\) if you have the admin role. The sn\_docintel\_admin application installs related ServiceNow® Store dependencies if they aren’t already installed.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](../concept/docintel-nowassist-landing.md).

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Document Intelligence](https://store.servicenow.com/sn_appstore_store.do#!/store/application/19b40605edae411005e8007f82757635) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Review the Document Intelligence [Admin](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8700f4efc3a411101d9a3cadb140ddad) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Role required: admin

## About this task

The following items are installed with Document Intelligence:

-   Plugins
-   Roles
-   Tables

For more information, see [Components installed with Document Intelligence](../reference/installed-with-document-intelligence.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Document Intelligence Admin application \(sn\_docintel\_admin\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you’re displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  Select **Install**.


