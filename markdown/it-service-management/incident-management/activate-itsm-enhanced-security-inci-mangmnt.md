---
title: Activate ITSM Enhanced Security Features for Incident Management
description: Help prevent unauthorized access to incident-related tables by activating the ITSM Enhanced Security Features plugin \(com.snc.itsm.enhanced\_security\), which uses deny unless authenticated access control lists \(ACLs\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/activate-itsm-enhanced-security-inci-mangmnt.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Enhanced security model features, Reference, Incident Management, IT Service Management]
---

# Activate ITSM Enhanced Security Features for Incident Management

Help prevent unauthorized access to incident-related tables by activating the ITSM Enhanced Security Features plugin \(com.snc.itsm.enhanced\_security\), which uses deny unless authenticated access control lists \(ACLs\).

## Before you begin

Role required: admin

**Note:** A user with the admin role can install and activate this plugin by submitting a support request.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).


**Parent Topic:**[Enhanced security model features for incident tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/comp-instal-itsm-enhanced-sec-features.md)

