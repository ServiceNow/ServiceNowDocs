---
title: Activate ITSM Enhanced Security Features for Change Management
description: Prevent unauthorized access to change-related tables using deny-unless ACLs by activating the ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ITSM Enhanced Security Features for Change Management, Reference section for Change Management, Change Management, IT Service Management]
---

# Activate ITSM Enhanced Security Features for Change Management

Prevent unauthorized access to change-related tables using deny-unless ACLs by activating the ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin.

## Before you begin

Role required: admin

**Note:** An admin can install and activate this plugin via support request.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[ITSM Enhanced Security Features for Change Management](../reference/features-itsm-enhanced-security-change.md)

