---
title: Activate the Return Merchandise Authorization plugin
description: If you have the admin role, you can activate the RMA Case Management plugin \(com.sn\_csm\_rma\_case\). The plugin enables you to manage and triage return cases for customer products and services, addressing returns, replacements, and repair use cases.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Order operations apps, Configure, Sales Customer Relationship Management]
---

# Activate the Return Merchandise Authorization plugin

If you have the admin role, you can activate the RMA Case Management plugin \(com.sn\_csm\_rma\_case\). The plugin enables you to manage and triage return cases for customer products and services, addressing returns, replacements, and repair use cases.

## Before you begin

Install the following plugins or confirm that they exist before activating the RMA Case Management plugin:

|Plugin|Description|
|------|-----------|
|Lead to Cash Core \[com.snc.l2c\_core\]|Enables you to compose Lead to Cash flow.|
|Customer Service Install Base Management \[com.snc.install\_base\]|Enables you to capture the current state of the install base and establish the relationship to any downstream entities that may impact their functioning.|
|Case lines and workflows \[com.sn\_case\_line\]|Enables a case to hold many line items. The line items are product instances and can be extended for various order to case operations entities.|
|Entitlements Verification \[com.sn\_ent\_verify\]|Provides API to verify entitlement and characteristics.|

Role required: admin

## About this task

The following items are installed with RMA Case Management:

-   Plugin
-   Tables
-   Roles

For more information, see [Return Merchandise Authorization Case Management](../reference/return-merchandise-authorization-case-management-reference.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the RMA Case Management plugin \(sn\_csm\_rma\_case\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


