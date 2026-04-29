---
title: Exploring Embedded Help
description: Embedded help provides targeted help content to a user in a UI page, based on their role. Some embedded help content comes with the base instance. Your organization can add or replace embedded help content.
locale: en-US
release: australia
product: Adoption Services
classification: adoption-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Embedded Help, In-product help, Adoption services, Configure user experiences]
---

# Exploring Embedded Help

Embedded help provides targeted help content to a user in a UI page, based on their role. Some embedded help content comes with the base instance. Your organization can add or replace embedded help content.

## Embedded Help overview

Embedded Help enables you to provide the help that your users need, as well as benefit from help topics available in the base system. You can add new embedded help content or replace content. Replacing content involves deactivating the existing topic and adding a topic.

Your organization may want to add or replace embedded help content for some of the following reasons:

-   To provide help for custom applications.
-   To provide more specific instructions or embedded videos to describe your business process.
-   To provide embedded help content where none exists for a page.
-   To provide embedded help content in languages other than English \(default\).
-   To provide different content for different roles.

The UI page name identifies embedded help content. To find the page name, look for the table name in the URL for that view. For example, the page name for the list view of Assessment Metric Types is asmt\_metric\_type\_list and is found in this address: `instancename.service-now.com/nav_to.do?uri=%2Fasmt_metric_type_list.do%3Fsysparm_userpref_module%`. The page name for the form view is asmt\_metric\_type.

You cannot edit the content in a base system topic. In base system topics, the read-only **ServiceNow Help** check box is selected. If you edit the content and try to save changes, you see an error message. To change the information that appears in a base system topic, make a copy of the topic, which clears the **ServiceNow Help** check box. Modify the topic with your content and save it. Customized content takes precedent over ServiceNow help content and is displayed when a user opens help for that UI page.

Starting this release, Embedded Help also supports non-English content import without overriding the last uploaded language content.

## Embedded Help workflow

The ServiceNow datacenter contains the Content Delivery Network \(CDN\) where embedded help content is stored. Topics in the local \(instance\) Embedded Help Content \[sys\_embedded\_help\_content\] table are populated from the CDN. Help content in the CDN is refreshed every 30 days.

When a user accesses a UI page, the embedded help process displays a custom topic if one exists for the user's role. If there is no custom topic, the following steps are performed.

1.  Checks the browser cache first, and displays the content if found in the cache. It then checks the Embedded Help Content \[sys\_embedded\_help\_content\] table for the corresponding embedded help topic with the role and qualifier, if applicable.
    -   If a topic is found, it checks the date in the **Last sync** field. If the date is 15 or more days old, it places a request in the Embedded Help Queue \[sys\_embedded\_help\_queue\] table with the last sync date and the resource ID.
    -   If a topic is not found, it places a request in the Embedded Help Queue \[sys\_embedded\_help\_queue\] table with the current date and the resource ID.
2.  Within a minute of the page being viewed, the system processes the request and checks the CDN. In the first case, it checks whether the topic was updated since the **Last sync** date. In either case, after a minute, refresh the page to see the content.
    -   If the topic was updated, it pulls the updated topic into the table and updates the **Last sync** date.
    -   If the topic was not updated, it displays the local cached or database topic, and updates the **Last sync** date.
3.  If the topic was not in the local database, it pulls the topic into the table if it exists on the CDN. If it does not exist, there is no action.

The administrator can modify the default 15-day synchronization duration in [system properties](../reference/embedded-help-sys-properties.md)

