---
title: Installing Generative AI Controller
description: You can install the Generative AI Controller application \(sn.generative.ai\) with Now Assist applications if you have the admin role.
locale: en-US
release: xanadu
product: Generative AI Controller
classification: generative-ai-controller
topic_type: concept
last_updated: "2024-11-18"
reading_time_minutes: 1
keywords: [Now Assist, installing, Generative AI, Gen AI, controller, admin console]
breadcrumb: [Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Installing Generative AI Controller

You can install the Generative AI Controller application \(sn.generative.ai\) with Now Assist applications if you have the admin role.

## Installation requirements

You must be on Vancouver patch 2 or later.

Generative AI Controller is included as a dependency for all Now Assist applications. It is not recommended to install the application by itself. Instead, you can install Now Assist applications from the Now Assist Admin console or directly from the ServiceNow Store. For details, see [Install Now Assist plugins](../../now-assist-admin/task/install-now-assist-feature-plugins.md).

![Now Assist Admin console links to browse plugins by workflow](../image/now-assist-console-install-plugins.png "Now Assist Admin console plugin installation")

The Sensitive Data Handler plugin is required to successfully use Generative AI Controller. It is installed with the latest version of the application, but if you have an earlier version of Generative AI Controller on your instance you may need to add the Sensitive Data handler manually.

