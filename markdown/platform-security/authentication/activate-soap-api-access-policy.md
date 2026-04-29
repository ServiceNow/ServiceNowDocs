---
title: Activate SOAP API access policy
description: For SOAP API access policy, install the SOAP API Access Policy \(com.glide.soap.policy\) plugin.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SOAP API access policies, API access policy, Authentication, Access Management]
---

# Activate SOAP API access policy

For SOAP API access policy, install the SOAP API Access Policy \(`com.glide.soap.policy`\) plugin.

## Before you begin

Role required: admin

## About this task

The following item is installed with SOAP API Access Policy Plugin: Processor Access Policy \(`com.glide.processor.policy`\)

Dependent Plugin: Authentication Profile \(`com.glide.auth.profile`\)

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the SOAP API Access Policy plugin \(`com.glide.soap.policy`\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


