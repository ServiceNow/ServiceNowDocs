---
title: Configure ServiceNow AI Lens
description: If you have the admin role, you can enable the ServiceNow AI Lens application \(sn\_ai\_lens\) to extract and comprehend data for various workflows.
locale: en-US
release: yokohama
product: ServiceNow Lens
classification: servicenow-lens
topic_type: task
last_updated: "2025-03-20"
reading_time_minutes: 2
breadcrumb: [ServiceNow AI Lens, Enable AI experiences]
---

# Configure ServiceNow AI Lens

If you have the admin role, you can enable the ServiceNow AI Lens application \(sn\_ai\_lens\) to extract and comprehend data for various workflows.

## Before you begin

To get started with ServiceNow AI Lens, you must have:

-   A ServiceNow Pro Plus or Enterprise Plus license.
-   An instance on Yokohama Patch 6+ or Zurich Patch 1+.

Role required: admin

## About this task

ServiceNow AI Lens isn’t a standalone application that you can install directly. To enable ServiceNow AI Lens on your instance, you must install other Now Assist applications, such as Now Assist for IT Service Management \(ITSM\) or Now Assist for Customer Service Management \(CSM\).

-   Review the [ServiceNow AI Lens](https://store.servicenow.com/sn_appstore_store.do#!/store/application/2527a8af90db9e10f877653916085448/1.0.0) application listing in ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Refer to the [Now Assist Overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/sn-assist-overview.pdf) to see the prebuilt skills that exist and are currently available for purchase in ServiceNow Now Assist packages and to review the number of assists consumed.
-   Perform these steps in your ServiceNow instance.

By enabling the ServiceNow AI Lens application \(sn\_ai\_lens\), you can view the ServiceNow AI Lens and download modules in your ServiceNow instance.

The following items are installed with ServiceNow AI Lens:

-   Roles
-   Tables

For more information, see [Components installed with ServiceNow AI Lens](../reference/components-installed-sn-lens.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  In the search field under the heading Search your licensed applications and plugins, enter the name of the Now Assist application that you want to install.

    For example, you can enter Now Assist for IT Service Management \(ITSM\).

3.  Press **Enter**.

    The Now Assist application listing appears.

4.  Select the Now Assist application card.

5.  Select **Install**.


## Result

Now Assist for Platform, ServiceNow AI Lens, and ServiceNow AI Lens Core applications are installed.

## What to do next

Turn on the ServiceNow AI Lens skill to extract, comprehend, and synthesize visual data to optimize your workflows. For more information, see [Activate the ServiceNow AI Lens skill](activate-lens-skill.md).

