---
title: Viewing blueprint deployments
description: The Deployments page shows the fifty most recently deployed blueprints together with their timestamps and associated users.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up blueprints, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Viewing blueprint deployments

The Deployments page shows the fifty most recently deployed blueprints together with their timestamps and associated users.

In CPQ Admin's Utilities menu, the first visible page is the Deployments page.

![Deployments page](../images/cpq-deployments-page.png)

This page shows the fifty most recent blueprints by the date and time of the deployment, together with the user responsible.

Because the configuration’s behavior can change depending on the rules, fields, and enrichments that have changed since the last deployment, this page is useful for troubleshooting. Noting the last time that a deployment behaved as intended is useful for both the admin implementing CPQ and for our support team when helping solve an issue.

Note that the Last Deployed column’s date and time will differ from the completion date and time as viewed from the notification bell. This is because the Last Deployed column shows the last time a blueprint was submitted for deployment, not when the deployment was completed. This is helpful in determining how long a deployment takes to complete, especially for large blueprints with hundreds or thousands of fields and rules.

![Deployments notifications](../images/cpq-deployments-last.png)

If your blueprints take longer than thirty minutes to complete, create a support ticket.

**Related topics**  


[Tracking a blueprint's deployment history](blueprints_deployment_history.md)

