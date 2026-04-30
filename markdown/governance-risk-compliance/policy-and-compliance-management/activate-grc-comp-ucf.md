---
title: Activate Compliance UCF
description: The GRC: Compliance UCF \(com.sn\_comp\_ucf\) plugin is available as a separate subscription.
locale: en-US
release: xanadu
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage the UCF integration, Using the Classic user interface for Policy and Compliance tasks, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Activate Compliance UCF

The GRC: Compliance UCF \(com.sn\_comp\_ucf\) plugin is available as a separate subscription.

## Before you begin

Role required: admin

## About this task

This plugin includes demo data and activates related plugins if they are not already active.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

Configure the source of your control library using an API key supplied by UCF \(this is the recommended method\) or using the UCF Common Controls Hub, which you can purchase as a subscription from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). For more information, see [Common Controls Hub](https://commoncontrolshub.com/pricing/) or [Unified Compliance Framework](https://www.unifiedcompliance.com/company/).

**Parent Topic:**[Manage the UCF integration](../../grc-ucf-import/concept/manage_compliance_frameworks.md)

