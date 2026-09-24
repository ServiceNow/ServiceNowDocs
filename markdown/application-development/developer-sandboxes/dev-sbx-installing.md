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
reading_time_minutes: 2
breadcrumb: [Developer Sandboxes, Developing your application, Building applications]
---

# Installing Developer Sandboxes

Developer Sandboxes is a installed on your instance, with licenses from a pack assigned by your admin. Review prerequisites, plugin requirements, and SSO configuration before installation begins.

## Developer Sandboxes installation

Check your entitlements to determine whether you have access to Developer Sandboxes. For more information, see [Developer Sandboxes entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dev-sbx-entitlements.md).

Developer Sandboxes is a paid feature and is enabled only after procurement is complete. To install Developer Sandboxes once you're entitled, open a case with Now Support specifying the instance name and licensed number of sandboxes.

## Prerequisites for installing Developer Sandboxes

Verify the following prerequisites before installing Developer Sandboxes.

Non-production instances must be:

-   On ADCv3 \(Application Delivery Controller version 3\)

    **Note:** If a non-production instance is not on ADCv3, it will be moved it as part of the setup.

-   Yokohama or higher

## Instances and sandboxes

Sandboxes are instance-specific, which means that you can't move a sandbox from one instance to another. If a new instance needs to be sandbox enabled, it will be a net-new order.

Each sandbox is hosted in its own app-node. Therefore, a key part of the setup is adding the required number of additional nodes on the instance. For example, to support 10 sandboxes, 10 new nodes would be added to an instance.

Developer Sandboxes are available in packs of 10.

**Note:** The minimum is one pack of sandboxes \(10\) per instance, and a maximum of three packs \(30 sandboxes\) can be assigned to a single instance. For example, if you buy two packs, you can't split them 5-15. Each instance must have at least 10 sandboxes. However, with the free pack, you can have a maximum of 34 sandboxes on one instance.

Developer Sandboxes does not support self-hosted instances by default, though you can set up your own networking and routing changes to support sandboxes.

For more information on sandboxes and instances, see [General guidelines and use cases for Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dev-sbx-general-guidelines.md).

## Contact Now Support to finish installation

The number of available sandboxes on an instance is defined by the number of purchased entitlements. You must contact Now Support to open a case to finish installing and configuring Developer Sandboxes.

## Enabling SSO

Developers can access sandboxes using instance credentials and Single Sign-On \(SSO\).

The following properties must be set in the base instance before developers can use SSO to access sandboxes:

-   Disable ACR: `sys_property glide.sso.acr.enable = false`
-   Enable SSO: `glide.authenticate.multisso.enabled = true`

