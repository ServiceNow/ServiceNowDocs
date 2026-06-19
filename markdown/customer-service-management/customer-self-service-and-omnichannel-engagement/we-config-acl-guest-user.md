---
title: Configure ACL for guest access
description: Enable guest users to access Web Embeddables components by activating the required guest access control lists \(ACLs\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/customer-self-service-and-omnichannel-engagement/we-config-acl-guest-user.html
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Guest user access for Web Embeddables, Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Configure ACL for guest access

Enable guest users to access Web Embeddables components by activating the required guest access control lists \(ACLs\).

## Before you begin

You must activate the Web Components for Guest \(sn\_guest\_component\) plugin. For more information, see [Guest users support activation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/we-guest-user-support.md).

Role required: security\_admin

## About this task

Guest ACLs control which component \(not content like article or catalog item\) and actions are accessible to guest users on your website. By default, all guest ACLs are inactive to maintain security.

Activate only the ACLs that correspond to the components you want to make available to guests. For example, if you embed catalog item components on your website, activate the catalog item ACLs. If you embed knowledge article components, activate the knowledge ACLs. This selective activation confirms guests can access only the content and functionality you explicitly allow.

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

