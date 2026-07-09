---
title: Reconnect ServiceNow CPQ after refreshing the Salesforce org
description: Reconnect the ServiceNow CPQ environment to a new or refreshed SFDC org.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/reconnect-logik-after-refreshing-the-salesforce-org.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow CPQ integration with Salesforce B2B Commerce, ServiceNow CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# Reconnect ServiceNow CPQ after refreshing the Salesforce org

Reconnect the ServiceNow CPQ environment to a new or refreshed SFDC org.

## Before you begin

Role required: Admin

## Procedure

1.  Submit a support case through the support site.

    Open a ticket by using the [ServiceNow Support portal](https://support.servicenow.com). For step-by-step instructions, see [Create a case on Now Support for CPQ Customers](https://support.servicenow.com/kb?sys_kb_id=d67d3e71475d7a90f64de825126d4326&id=kb_article_view).

    Provide the new org ID, the My Domain URL, and the custom URL of the ServiceNow CPQ environment. The custom URL will have the form `https://<tenant>.<sector>.cpq`.

2.  If a ServiceNow CPQ user exists on the org, send a password reset request for the user.

3.  If no ServiceNow CPQ user exists on the org, create a user.


## Result

You will be notified when the migration of the ServiceNow CPQ environment to the new org is complete.

If ServiceNow CPQ has confirmed the migration is complete but you are unable to give a user access to the org, follow these steps:

1.  Navigate to the ServiceNow CPQ Tenant: Setup &gt; Custom Settings &gt; Click Manage next to the ServiceNow CPQ Tenant.
2.  Edit or confirm that the Administration URL is set to the custom URL of your ServiceNow CPQ environment: `https://<tenant>.<sector>.cpq`.
3.  Navigate to Installed Packages &gt; Find Salesforce CPQ &gt; Configure &gt; Additional Settings, and update the Salesforce CPQ External Configurator URL to your ServiceNow CPQ URL followed by `/ui/configure: https://<tenant>.<sector>.cpq/ui/configure`.

