---
title: Activate Approval with e-Signature plugin
description: The Approval with e-Signature plugin \(com.glide.e\_signature\_approvals\) allows users to approve requests by re-entering their login credentials.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [E-signature for Multi-Provider SSO, Multi-Provider SSO configurations, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Activate Approval with e-Signature plugin

The Approval with e-Signature plugin \(com.glide.e\_signature\_approvals\) allows users to approve requests by re-entering their login credentials.

## Before you begin

Role required: admin

**Note:** You must install the Code Signing Signatures \(`com.glide.code_signing.signatures`\) to install the E-signature plugin.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


