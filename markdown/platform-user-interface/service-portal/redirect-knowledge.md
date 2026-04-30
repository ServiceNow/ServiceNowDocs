---
title: Activate the Knowledge Article View page on upgrade
description: If upgrading from a previous release, take advantage of the latest article view features by activating the Knowledge Article View page route map. New capabilities include article versioning and using links and images in article feedback. This map is active by default in new instances and applies to all portals in the system.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Upgrading Service Portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Activate the Knowledge Article View page on upgrade

If upgrading from a previous release, take advantage of the latest article view features by activating the **Knowledge Article View** page route map. New capabilities include article versioning and using links and images in article feedback. This map is active by default in new instances and applies to all portals in the system.

## Before you begin

Role required: admin

## About this task

The **Knowledge Article View** page route map routes the **kb\_article** page to the **kb\_article\_view** page. By default, users with the public role cannot access the **kb\_article\_view** page. However, your administrator can modify this behavior. For more information, see [Enable external or public users to view knowledge articles from the Knowledge Management Service Portal](https://www.servicenow.com/docs/access?context=make-knowledge-visible-to-public&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

After activating the **Knowledge Article View** page route map, you can:

-   [Comment on a knowledge article](https://www.servicenow.com/docs/access?context=comment-article&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
-   [Create an article version by importing a Word document](https://www.servicenow.com/docs/access?context=upload-new-version-article&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
-   [Create a version of a knowledge article from a managed document](https://www.servicenow.com/docs/access?context=t_ViewKnowledgeLinkedToADocument&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Page Route Maps**.

2.  Open the **Knowledge Article View** record.

3.  Select **Active**.

4.  Click **Update**.


## Result

Your end users view knowledge articles in the Service Portal using the **kb\_article\_view** page.

**Parent Topic:**[Upgrading Service Portal](upgrading-service-portal.md)

