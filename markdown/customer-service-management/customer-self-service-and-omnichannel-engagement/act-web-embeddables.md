---
title: Activate Web Embeddables
description: You can enable the ServiceNow Components for Customer Service \(sn\_cx\_components\), Web Components for Guest \(sn\_guest\_component\), and Web Embeddable Core \(sn\_embeddable\_core\) to enable Web Embeddables on your instance. The application establishes related plugins if they aren’t already installed.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Activate Web Embeddables

You can enable the ServiceNow Components for Customer Service \(sn\_cx\_components\), Web Components for Guest \(sn\_guest\_component\), and Web Embeddable Core \(sn\_embeddable\_core\) to enable Web Embeddables on your instance. The application establishes related plugins if they aren’t already installed.

## Before you begin

Role required: None

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


