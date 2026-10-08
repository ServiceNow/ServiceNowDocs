---
title: Default Quota Configuration form
description: A description of the fields on the Default Quota Configuration form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/default-quota-configuration-form.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Reference, Application Runtime Policy \(ARP\), Developing your application, Building applications]
---

# Default Quota Configuration form

A description of the fields on the Default Quota Configuration form.

<table id="table_z3l_zgh_wjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration Name

</td><td>

A unique name to identify the default configuration.

</td></tr><tr><td>

Application

</td><td>

The scoped application's name. To change this field, use the application picker to change the application. This field can't be Global.

</td></tr><tr><td>

Order

</td><td>

A number that dictates the order in which application quotas are evaluated. If multiple default quota configurations apply to an application, the default quota configuration with the lowest number is applied first.

</td></tr><tr><td>

Enable Auto-Generated Quotas

</td><td>

When selected, application resource quotas based on this default configuration are generated in instances that install the application.

</td></tr><tr><td>

Application Condition

</td><td>

The condition that further specifies the scope that the default quota configuration applies to. The condition builder displays conditions that are only applicable to the application scope. For example, Version is 3.0.

</td></tr><tr><td>

Scheduled Job Quota %

</td><td>

Percentage of total processing time that can be allocated to jobs. When the default quota configuration is in enforcing mode and the quota threshold is exceeded, scheduled jobs are deferred until the next available time window.Default value: 20%

</td></tr><tr><td>

API Transaction Quota %

</td><td>

Total percentage of threads that can execute API requests for a given application and scope. When the default quota configuration is in enforcing mode and the quota threshold is exceeded, API requests are rejected.Default value: 30%

</td></tr><tr><td>

Interactive Transaction Quota %

</td><td>

Total percentage of threads that can execute UI requests. When the default quota configuration is in enforcing mode and the quota threshold is exceeded, UI requests are rejected.Default value: 30%

</td></tr><tr><td>

Event Handler Quota %

</td><td>

Percentage of total processing time that can be allocated to event handlers. When the default quota configuration is in enforcing mode and the quota threshold is exceeded, event handler processing is deferred until the next available time window.Default value: 20%

</td></tr><tr><td>

Mode

</td><td>

Determines how default quota configurations are enforced. Options include the following:-   **Disabled** prevents enforcements of a default quota configuration.
-   **Enforced** causes requested resources to be deferred or rejected when the quota threshold is exceeded.

This is the default value.

-   **Log Only** adds log entries to indicate when the quota threshold is exceeded. No resources are rejected or deferred.

</td></tr></tbody>
</table>**Parent Topic:**[Application Runtime Policy reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/application-runtime-policy-reference.md)

