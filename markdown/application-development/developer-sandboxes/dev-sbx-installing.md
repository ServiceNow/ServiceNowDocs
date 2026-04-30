---
title: Installing Developer Sandboxes
description: Developer Sandboxes is installed on your instance with assistance from your ServiceNow account team.
locale: en-US
release: zurich
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: concept
last_updated: "2025-08-11"
reading_time_minutes: 2
breadcrumb: [Developer Sandboxes, Developing your application, Building applications]
---

# Installing Developer Sandboxes

Developer Sandboxes is installed on your instance with assistance from your ServiceNow account team.

## Requesting Developer Sandboxes installation

Check your entitlements to determine whether you have access to Developer Sandboxes. For more information, see [Developer Sandboxes entitlements](dev-sbx-entitlements.md).

Developer Sandboxes is a paid feature and is enabled only after procurement is complete. To install Developer Sandboxes once you're entitled, open a case with Now Support specifying the instance name and licensed number of sandboxes.

**Note:** If your instance is in a regulated environment, check with ServiceNow Support for more information about support for Developer Sandboxes.

**Note:** The Developer Sandboxes plugin should be installed in your production instance, or any clone source to ensure that cloning a sandbox instance correctly maintains entitlement.

## Prerequisites for installing Developer Sandboxes

You must have the following to install Developer Sandboxes:

-   A non-production instance
-   The instance is on ADCv3 \(Application Delivery Controller version 3\)

    **Note:** If the instance is not on ADCv3, it will be moved it as part of the setup.

-   Yokohama or higher

## Instances and sandboxes

Sandboxes are instance-specific, which means that you can't move a sandbox from one instance to another. If a new instance needs to be sandbox enabled, it will be a net new order.

Each sandbox is hosted in its own app-node. Therefore, a key part of the setup is adding the required number of additional nodes on the instance. For example, to support 10 sandboxes, 10 new nodes would be added to an instance.

Developer Sandboxes are available in packs of 10. When you buy two or more packs, you can split the pack between different instances. To do so, open a request with Now Support for each instance.

**Note:** The minimum is one pack of sandboxes \(10\) per instance. For example, If you buy two packs, you can't split them 5-15. Each instance must have at least 10 sandboxes.

Developer Sandboxes does not support self-hosted instances by default, though you can set up your own networking and routing changes to support sandboxes.

For more information on sandboxes and instances, see [General guidelines and use cases for Developer Sandboxes](dev-sbx-general-guidelines.md).

## Contact Now Support to finish installation

The number of available sandboxes on an instance is defined by the number of purchased entitlements. You must contact Now Support to open a case to finish installing and configuring Developer Sandboxes.

## Enabling SSO

Developers can access sandboxes using instance credentials as well as Single Sign-On \(SSO\).

The following properties must be set in the base instance before developers can use SSO to access sandboxes:

-   Disable ACR: `sys_property glide.sso.acr.enable=false`
-   Enable SSO: `glide.authenticate.multisso.enabled = true`

