---
title: Activate Multi-Provider SSO plugin
description: This integration requires the Integration - Multiple Provider Single Sign-On Installer \(com.snc.integration.sso.multi.installer\) plugin.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Activate Multi-Provider SSO plugin

This integration requires the Integration - Multiple Provider Single Sign-On Installer \(com.snc.integration.sso.multi.installer\) plugin.

## Before you begin

Role required: admin.

The com.snc.integration.sso.multi.installer plugin can also be used for OIDC, SAML, and Digest.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Integration - Multiple Provider Single Sign-On Installer \(com.snc.integration.sso.multi.installer\) plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


