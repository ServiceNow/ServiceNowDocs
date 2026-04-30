---
title: Activate the SCIM Client plugin
description: For SCIM Client activation, install the SCIM v2 - ServiceNow Cross-domain Identity Management Client \(com.snc.integration.scim2.client\) plugin.
locale: en-US
release: xanadu
product: Identity
classification: identity
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SCIM Client, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# Activate the SCIM Client plugin

For SCIM Client activation, install the SCIM v2 - ServiceNow Cross-domain Identity Management Client \(com.snc.integration.scim2.client\) plugin.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the SCIM v2 - ServiceNow Cross-domain Identity Management Client \(com.snc.integration.scim2.client\) plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


