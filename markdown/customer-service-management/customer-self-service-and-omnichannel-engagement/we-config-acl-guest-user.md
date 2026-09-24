---
title: Configure ACL for guest access
description: Enable guest users to access catalog items or knowledge articles by activating the required guest access control lists \(ACLs\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/customer-self-service-and-omnichannel-engagement/we-config-acl-guest-user.html
release: brazil
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Guest user access for Web Embeddables, Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Configure ACL for guest access

Enable guest users to access catalog items or knowledge articles by activating the required guest access control lists \(ACLs\).

## Before you begin

You must activate the Web Components for Guest \(sn\_guest\_component\) plugin. For more information, see [Activate Web Embeddables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/act-web-embeddables.md).

Role required: security\_admin

## About this task

Guest ACLs control what components and actions are available to guest users on your website. The guest ACLs make the Knowledge Article View and Catalog Item components accessible to guest users. They do not control access to specific knowledge articles or catalog items. Content-level access is managed separately through your knowledge base and catalog configuration. By default, all guest ACLs are inactive to ensure controlled access.

Activate only the ACLs that correspond to the components you want to make available to guests. For example, if you embed catalog item components on your website, activate the catalog item ACLs. If you embed knowledge article components, activate the knowledge ACLs. This selective activation ensures guests can access only the content and functionality you explicitly allow.

## Procedure

1.  In the filter navigator, enter `Access Control (ACL)`.

2.  On the Access Controls page, in the Application column, enter `Web Components for Guest Embeddables`.

3.  In the Description field, enter any of the following:

    -   Enter `*[Guest Embeddables | Knowledge]` to view ACLs related to knowledge articles.
    -   Enter `*[Guest Embeddables | Catalog Item]` to view ACLs related to catalog items.
4.  In the Name column, search for and select the ACLs you need to activate.

5.  In the ACLs page, select the **Active** check box.

6.  Select **Update**.


## Result

Guest users can now access the Knowledge Article View and Catalog Item components based on the ACLs you activated. These ACLs enable access to the components, not to specific knowledge articles or catalog items within them. The system applies these ACLs when guests interact with embedded components on your website.

