---
title: Activate Customer Service Management
description: You can activate the Case Management Core \(com.sn\_customerservice\) plugin, if you have the admin role. This plugin includes demo data and activates related plugins if they aren’t already active.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/t\_ActivateCustomerService.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Getting started with Customer Service Management, Set up your environment, Configure, Customer Service Management]
---

# Activate Customer Service Management

You can activate the Case Management Core \(com.sn\_customerservice\) plugin, if you have the admin role. This plugin includes demo data and activates related plugins if they aren’t already active.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/find-components.md).


**Parent Topic:**[Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/c_CustomerServiceManagement.md)

