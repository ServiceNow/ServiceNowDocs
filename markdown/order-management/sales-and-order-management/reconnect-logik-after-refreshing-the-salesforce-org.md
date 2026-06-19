---
title: Reconnect Logik after refreshing the Salesforce org
description: Reconnect the Logik environment to a new or refreshed SFDC org.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/reconnect-logik-after-refreshing-the-salesforce-org.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ integration with Salesforce B2B Commerce, CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# Reconnect Logik after refreshing the Salesforce org

Reconnect the Logik environment to a new or refreshed SFDC org.

## Before you begin

Role required: Admin

## Procedure

1.  Submit a support case through the support site.

    Open a ticket by using the [ServiceNow Support portal](https://support.servicenow.com). For step-by-step instructions, see [Create a case on Now Support for CPQ \(Logik.ai\) Customers](https://support.servicenow.com/kb?sys_kb_id=d67d3e71475d7a90f64de825126d4326&id=kb_article_view).

    Provide the new org ID, the My Domain URL, and the custom URL of the Logik environment. The custom URL will have the form `https://<tenant>.<sector>.logik.io`.

2.  If a Logik user exists on the org, send a password reset request for the user.

3.  If no Logik user exists on the org, create a user.


## Result

You will be notified when the migration of the Logik environment to the new org is complete.

If Logik has confirmed the migration is complete but you are unable to give a Logik user access to the org, follow these steps:

1.  Navigate to the Logik Tenant: Setup &gt; Custom Settings &gt; Click Manage next to the Logik Tenant.
2.  Edit or confirm that the Administration URL is set to the custom URL of your Logik environment: `https://<tenant>.<sector>.logik.io`.
3.  Navigate to Installed Packages &gt; Find Salesforce CPQ &gt; Configure &gt; Additional Settings, and update the Salesforce CPQ External Configurator URL to your Logik URL followed by `/ui/configure: https://<tenant>.<sector>.logik.io/ui/configure`.

