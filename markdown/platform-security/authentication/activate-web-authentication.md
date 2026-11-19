---
title: Activate the Web Authentication plugin
description: The Integration - Web Authentication plugin must be activated for Web Authentication \(FIDO2\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/authentication/activate-web-authentication.html
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Web Authentication, Using MFA, Multi-factor authentication, Authentication, Access Management]
---

# Activate the Web Authentication plugin

The Integration - Web Authentication plugin must be activated for Web Authentication \(FIDO2\).

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the **Integration - Web Authentication** \(com.snc.integration.webauthn\) plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/find-components.md).


