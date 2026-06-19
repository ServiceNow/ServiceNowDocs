---
title: Activate the Enhanced Web Service Provider - Common plugin
description: Administrators can activate the Enhanced Web Service Provider - Common plugin to enable unsigned WS-Security requests and specify what authentication requirements SOAP requests have.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/t\_ActivateEnhancedWSPPlugin.html
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Activate the Enhanced Web Service Provider - Common plugin

Administrators can activate the Enhanced Web Service Provider - Common plugin to enable unsigned WS-Security requests and specify what authentication requirements SOAP requests have.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Enhanced Web Service Provider - Common plugin \(com.glide.web\_service\_provider\_v2\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see Find components installed with an application.


-   **[Installed with the Enhanced Web Service Provider - Common plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/r_InstallWEnhancedWSPCommPlugin.md)**  
The following components installed with the Enhanced Web Service Provider - Common plugin.

**Parent Topic:**[SOAP web service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_SOAPWebService.md)

