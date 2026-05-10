---
title: Activate the Knowledge Article View page on upgrade
description: If upgrading from a previous release, take advantage of the latest article view features by activating the Knowledge Article View page route map. New capabilities include article versioning and using links and images in article feedback. This map is active by default in new instances and applies to all portals in the system.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Upgrading Service Portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Activate the Knowledge Article View page on upgrade

If upgrading from a previous release, take advantage of the latest article view features by activating the **Knowledge Article View** page route map. New capabilities include article versioning and using links and images in article feedback. This map is active by default in new instances and applies to all portals in the system.

## Before you begin

Role required: admin

## About this task

The **Knowledge Article View** page route map routes the **kb\_article** page to the **kb\_article\_view** page. By default, users with the public role cannot access the **kb\_article\_view** page. However, your administrator can modify this behavior. For more information, see [Enable external or public users to view knowledge articles from the Knowledge Management Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/make-knowledge-visible-to-public.md).

After activating the **Knowledge Article View** page route map, you can:

-   [Comment on a knowledge article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/comment-article.md)
-   [Create an article version by importing a Word document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/upload-new-version-article.md)
-   [Create a version of a knowledge article from a managed document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/document-management-services/t_ViewKnowledgeLinkedToADocument.md)

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Page Route Maps**.

2.  Open the **Knowledge Article View** record.

3.  Select **Active**.

4.  Click **Update**.


## Result

Your end users view knowledge articles in the Service Portal using the **kb\_article\_view** page.

**Parent Topic:**[Upgrading Service Portal](upgrading-service-portal.md)

