---
title: Activate Certificate-based authentication
description: You can activate the Certificate-based authentication plugin \(com.glide.auth.mutual\) for ServiceNow AI Platform if you have the admin role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/certificate-based-authentication/activate-certificate-authentication.html
release: brazil
product: Certificate-based Authentication
classification: certificate-based-authentication
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Set up, Certificate-based authentication, Authentication, Access Management]
---

# Activate Certificate-based authentication

You can activate the Certificate-based authentication plugin \(com.glide.auth.mutual\) for ServiceNow AI Platform if you have the admin role.

## Before you begin

Role required: admin

## About this task

The following Tables are installed with Certificate-based authentication:

-   sys\_user\_certificate
-   sys\_ca\_certificate
-   sys\_ca\_certificate\_api\_track

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Certificate-based authentication plugin \(com.glide.auth.mutual\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/find-components.md).


