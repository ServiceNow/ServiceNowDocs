---
title: Developer Sandboxes installation
description: Developer Sandboxes is installed on your instance, with licenses from a pack assigned by your admin. Review prerequisites and plugin requirements before installation begins.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/developer-sandboxes/dev-sbx-installing.html
release: australia
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: concept
last_updated: "2026-10-29"
reading_time_minutes: 4
breadcrumb: [Install and configure, Developer Sandboxes, Build, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Developer Sandboxes installation

Developer Sandboxes is installed on your instance, with licenses from a pack assigned by your admin. Review prerequisites and plugin requirements before installation begins.

**Warning:** The installation instructions in this topic are for the Brazil release and later. If you're on Australia or earlier, you must open a Now Support request. See the Australia version of this topic for details.

## Developer Sandboxes installation

Check your entitlements to determine whether you have access to Developer Sandboxes. For more information, see [Developer Sandboxes entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dev-sbx-entitlements.md).

To install Developer Sandboxes:

-   The com.glide.dsb plugin must be installed on each non-production instance that will host sandboxes.

    **Warning:** Do not install or enable the `com.glide.dsb` plugin on a production instance or any instance where sandboxes will not be hosted.

-   After you install the com.glide.dsb plugin, set the **glide.dev\_sandbox.enabled** property to `true` on the instance before you add it through license management. The com.glide.dsb plugin doesn't enable Developer Sandboxes automatically.
-   Reconfigure the **glide.dev\_sandbox.num.controller** property to reflect the number of nodes currently on your instance \(the default is 2\). For more information, see [Properties installed with Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dsb-properties-installed.md).
-   The com.glide.dsb.licensing plugin must be installed on your production or controller instance to manage sandbox license assignment from App Engine Management Center \(AEMC\).
-   A sandbox license admin must assign licenses. For more information, see [License assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dsb-license-allocation-about.md).
-   If your instance is in a regulated environment, check with ServiceNow Support for more information about support for Developer Sandboxes.

## Prerequisites for installing Developer Sandboxes

Verify the following prerequisites before installing Developer Sandboxes.

The controller instance must be the license management instance.

Non-production instances must be:

-   On ADCv3 \(Application Delivery Controller version 3\)

    **Note:** If a non-production instance is not on ADCv3, it is moved as part of the setup.

-   Yokohama or higher

## Enable sandboxes on the instance

Starting with the Brazil Patch 2 release, Developer Sandboxes isn't enabled automatically when the com.glide.dsb plugin is installed. Set the following properties on the instance before you add it through license management:

-   **glide.dev\_sandbox.enabled** set to `true`.
-   Optional: **glide.dev\_sandbox.num.controller** to set the number of nodes that service the base instances. The default value is 2.

For more information about these properties, see [Properties installed with Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dsb-properties-installed.md).

## Instances and sandboxes

Sandboxes are instance-specific, which means that you can't move a sandbox from one instance to another. If a new instance needs to be sandbox enabled, a new order is required.

**Note:** A free pack of four sandboxes is automatically available to all organizations. The free pack can be assigned to one non-production instance and can't be split across instances.

Each sandbox is hosted in its own app-node. Therefore, a key part of the setup is adding the required number of additional nodes on the instance. For example, to support 10 sandboxes, 10 new nodes would be added to an instance.

Developer Sandboxes are available in packs of 10.When you buy two or more packs, you can distribute them across instances using the self-serve license assignment UI in \(AEMC.

**Note:** The minimum is one pack of sandboxes \(10\) per instance, and a maximum of three packs \(30 sandboxes\) can be assigned to a single instance. For example, if you buy two packs, you can't split them 5–15. Each instance must have at least 10 sandboxes. However, with the free pack, you can have a maximum of 34 sandboxes on one instance.For more information, see [License assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dsb-license-allocation-about.md).

Developer Sandboxes is supported on on-premises instances. For setup steps, see the Knowledge Base article on [Developer Sandboxes on-premises architecture](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2670540). You're responsible for networking setup, adding the required nodes to the instance, and enabling sandboxes. License management isn't supported on on-premises instances.

For more information about sandboxes and instances, see [General guidelines and use cases for Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dev-sbx-general-guidelines.md).

**Parent Topic:**[Developer Sandboxes installation and configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dsb-configuring-landing.md)

