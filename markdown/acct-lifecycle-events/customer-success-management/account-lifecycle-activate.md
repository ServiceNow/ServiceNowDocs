---
title: Activate Customer Success Management
description: The Customer Success Management \(com.sn\_acct\_lc\) plugin is available as a separate subscription. Activating this plugin also activates the related plugins required to use the application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/customer-success-management/account-lifecycle-activate.html
release: australia
product: Customer Success Management
classification: customer-success-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Getting started, Configure, Customer Success Management]
---

# Activate Customer Success Management

The Customer Success Management \(com.sn\_acct\_lc\) plugin is available as a separate subscription. Activating this plugin also activates the related plugins required to use the application.

## Before you begin

Role required: sn\_customerservice.customer\_admin

## About this task

If the related plugins aren’t already active, the Customer Success Management plugin activates them. For more information, see [Plugins activated with Customer Success Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-required-plugins.md).

## Procedure

1.  Navigate to **All** &gt; **Application Manager**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you can’t find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install**, and then in the Activate Plugin dialog box, select **Activate**.

    **Note:** When domain separation and delegated admin are enabled in an instance, you must be in the **global** domain. Otherwise, the following error message appears:

    ```
    Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>
    ```

    .


## What to do next

After activating the application, complete the following steps:

-   To enable account onboarding, configure the onboarding playbook. See [Configure the account onboarding playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-configure.md).
-   To enable customer success, create the choice and definition records. See [Getting started with Customer Success](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-basic-config.md).

**Parent Topic:**[Getting started with Customer Success Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-get-started.md)

