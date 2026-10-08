---
title: Installing Developer Sandboxes
description: Developer Sandboxes is a installed on your instance, with licenses from a pack assigned by your admin. Review prerequisites, plugin requirements, and SSO configuration before installation begins.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/developer-sandboxes/dev-sbx-installing.html
release: brazil
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Developer Sandboxes, Build, AI Workflow Factory, Building applications]
---

# Installing Developer Sandboxes

Developer Sandboxes is a installed on your instance, with licenses from a pack assigned by your admin. Review prerequisites, plugin requirements, and SSO configuration before installation begins.

## Developer Sandboxes installation

Check your entitlements to determine whether you have access to Developer Sandboxes. For more information, see [Developer Sandboxes entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dev-sbx-entitlements.md).

To install Developer Sandboxes:

-   The com.glide.dsb plugin must be installed on each license management instance that will host sandboxes.

    **Warning:** Do not install or enable the `com.glide.dsb` plugin on a production instance or any instance where sandboxes will not be hosted.

-   The com.glide.dsb.licensing plugin must be installed on your production or controller instance to manage sandbox license assignment from App Engine Management Center.
-   After you install the com.glide.dsb.licensing plugin, you must reconfigure the `glide.dev_sandbox.num.controller` property. For more information, see [Properties installed with Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dsb-properties-installed.md).
-   A sandbox license admin must assign licenses. For more information, see [License assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dsb-license-allocation-about.md).
-   If your instance is in a regulated environment, check with ServiceNow Support for more information about support for Developer Sandboxes.

## Prerequisites for installing Developer Sandboxes

Verify the following prerequisites before installing Developer Sandboxes.

The controller instance must be the license management instance.

Non-production instances must be:

-   On ADCv3 \(Application Delivery Controller version 3\)

    **Note:** If a non-production instance is not on ADCv3, it will be moved it as part of the setup.

-   Yokohama or higher

## Instances and sandboxes

Sandboxes are instance-specific, which means that you can't move a sandbox from one instance to another. If a new instance needs to be sandbox enabled, it will be a net-new order.

**Note:** A free pack of four sandboxes is automatically available to all organizations. The free pack can be assigned to one non-production instance and can't be split across instances.

Each sandbox is hosted in its own app-node. Therefore, a key part of the setup is adding the required number of additional nodes on the instance. For example, to support 10 sandboxes, 10 new nodes would be added to an instance.

Developer Sandboxes are available in packs of 10.When you buy two or more packs, you can distribute them across instances using the self-serve license assignment UI in AEMC.

**Note:** The minimum is one pack of sandboxes \(10\) per instance, and a maximum of three packs \(30 sandboxes\) can be assigned to a single instance. For example, if you buy two packs, you can't split them 5-15. Each instance must have at least 10 sandboxes. However, with the free pack, you can have a maximum of 34 sandboxes on one instance.For more information, see [License assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dsb-license-allocation-about.md).

Developer Sandboxes does not support self-hosted instances by default, though you can set up your own networking and routing changes to support sandboxes.

For more information on sandboxes and instances, see [General guidelines and use cases for Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dev-sbx-general-guidelines.md).

## Enabling SSO

Developers can access sandboxes using instance credentials and Single Sign-On \(SSO\).

The following properties must be set in the base instance before developers can use SSO to access sandboxes:

-   Disable ACR: `sys_property glide.sso.acr.enable = false`
-   Enable SSO: `glide.authenticate.multisso.enabled = true`

-   **[Developer Sandboxes entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dev-sbx-entitlements.md)**  
Your company's entitlements determine whether you have access to Developer Sandboxes.
-   **[License assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dsb-license-allocation-about.md)**  
License assignment in App Engine Management Center \(AEMC\) lets Developer Sandboxes admins distribute purchased sandbox packs across non-production instances without opening a support case. Each pack contains 10 sandboxes, and assignments are managed from a license management instance.
-   **[Cloning and upgrading considerations for Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dev-sbx-clone-upgrade-info.md)**  
You should understand how plugins and sandboxes work before you clone or upgrade an instance with Developer Sandboxes. Always back up your work in a sandbox before any clone or upgrade, either by exporting the update sets or committing to source control.
-   **[Developer Sandboxes domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dsb-domain-separation.md)**  
Domain separation is supported for Developer Sandboxes. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Components installed with Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dsb-installed-with.md)**  
Several types of components are installed with activation of Developer Sandboxes, including tables and user roles.
-   **[Properties installed with Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dsb-properties-installed.md)**  
The system properties available in Developer Sandboxes govern application behavior, enabling developers to configure and optimize their testing environments effectively.

**Parent Topic:**[Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/sandboxes-landing.md)

