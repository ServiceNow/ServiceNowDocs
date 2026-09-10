---
title: Automatic subscription assignment
description: If your organization has never manually allocated user-based subscriptions before, entitlements are automatically assigned based on user roles and ACL access. Reviewing how roles are evaluated for automatic subscription assignment can help you make decisions about which roles users should have.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/user-subscription-auto-assignment.html
release: australia
topic_type: concept
last_updated: "2026-07-24"
reading_time_minutes: 1
breadcrumb: [Managing per-user subscriptions, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Automatic subscription assignment

If your organization has never manually allocated user-based subscriptions before, entitlements are automatically assigned based on user roles and ACL access. Reviewing how roles are evaluated for automatic subscription assignment can help you make decisions about which roles users should have.

If your organization has never manually allocated user-based subscriptions,Subscription Management evaluates user roles and assigns users the lowest-cost subscription that meets the access needs of their roles..

Custom and customized roles are classified for auto-assignment according to the Access Control Lists \(ACLs\) each role contains. Users with custom or customized roles are assigned subscription entitlements based on access granted to tables within a subscription product. For more information about subscription auto-assignment for custom and customized roles, see the article [Understanding Custom Role Validation - Use Verification \[KB1637906\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637906) on the Now Support Knowledge Base.

**Parent Topic:**[Managing per-user subscriptions in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/managing-user-subscriptions-v2.md)

