---
title: Viewing blueprint deployments
description: The Deployments page shows the fifty most recently deployed blueprints together with their timestamps and associated users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/deployments\_page.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up blueprints, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Viewing blueprint deployments

The Deployments page shows the fifty most recently deployed blueprints together with their timestamps and associated users.

In CPQ Admin's Utilities menu, the first visible page is the Deployments page.

\[Omitted image "cpq-deployments-page.png"\] Alt text: Deployments page

This page shows the fifty most recent blueprints by the date and time of the deployment, together with the user responsible.

Because the configuration’s behavior can change depending on the rules, fields, and enrichments that have changed since the last deployment, this page is useful for troubleshooting. Noting the last time that a deployment behaved as intended is useful for both the admin implementing CPQ and for our support team when helping solve an issue.

Note that the Last Deployed column’s date and time will differ from the completion date and time as viewed from the notification bell. This is because the Last Deployed column shows the last time a blueprint was submitted for deployment, not when the deployment was completed. This is helpful in determining how long a deployment takes to complete, especially for large blueprints with hundreds or thousands of fields and rules.

\[Omitted image "cpq-deployments-last.png"\] Alt text: Deployments notifications

If your blueprints take longer than thirty minutes to complete, create a support ticket by using the [ServiceNow Support portal](https://support.servicenow.com). For step-by-step instructions, see [Create a case on Now Support for CPQ \(Logik.ai\) Customers](https://support.servicenow.com/kb?sys_kb_id=d67d3e71475d7a90f64de825126d4326&id=kb_article_view).

**Related topics**  


[Tracking a blueprint's deployment history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/blueprints_deployment_history.md)

