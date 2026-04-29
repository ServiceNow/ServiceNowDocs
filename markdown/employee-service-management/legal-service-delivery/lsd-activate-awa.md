---
title: Activate Advanced Work Assignment for Legal Service Delivery
description: You can activate the Advanced Work Assignment for Legal Service Delivery plugin \(sn\_lg\_awa\) for Legal Service Delivery if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Advanced work assignment for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Activate Advanced Work Assignment for Legal Service Delivery

You can activate the Advanced Work Assignment for Legal Service Delivery plugin \(sn\_lg\_awa\) for Legal Service Delivery if you have the admin role.

## Before you begin

Advanced Work Assignment for Legal Service Delivery requires a separate subscription from the rest of the ServiceNow AI Platform.

To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance.

**Note:**

Before purchasing a subscription, you can evaluate the feature on a non-production instance without charge by requesting it from the Now Support Service Catalog.

Role required: admin

## About this task

Roles are installed with Advanced Work Assignment for Legal Service Delivery:

For more information, see [Components installed for Advanced Work Assignment for Legal Service Delivery reference](../reference/lsd-components-installed-awa.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Advanced Work Assignment for Legal Service Delivery plugin \(sn\_lg\_awa\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

-   If you are going to use skill determination rules to map a skill to an legal request, activate Skills Management \[com.snc.skills\_management\].

    **Note:** If you're using skill management, ensure you have the right subscription.

-   Configure live agent support for legal services. For more information, see [Configure Virtual Agent conversation topics for legal services](../../legal-request-management/task/configure-legal-va.md).

