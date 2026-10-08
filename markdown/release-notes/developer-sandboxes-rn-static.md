---
title: Developer Sandboxes release notes
description: The ServiceNow Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. See the following sections for release notes by version.The October 2026 release of Developer Sandboxes includes fully automated self-serve license assignment from App Engine Management Center and four free sandbox licenses available on all non-production instances.The Brazil Early Availability release introduces sandbox pooling for faster provisioning and automatic update set sources between production and sandbox instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/developer-sandboxes-rn-static.html
release: brazil
topic_type: topic
last_updated: "2026-09-15"
reading_time_minutes: 3
keywords: [developer sandbox, sandbox management, isolated development environment, parallel development, sandbox release notes, com.glide.dsb.licensing, sandbox plugin, source control integration, Git sandbox, delegated developer]
audience: administrator
breadcrumb: [App development and low-code release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Developer Sandboxes release notes

The ServiceNow® Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. See the following sections for release notes by version.

## About Developer Sandboxes

-   Work in fully isolated environments, so changes in one sandbox don't affect teammates, the baseline instance, or other sandboxes running in parallel.
-   Provision sandboxes on demand and align them to specific stories, developers, or test plans, enabling multiple workstreams to run concurrently without waiting for shared resources.
-   Integrate with source control \(Git\), reducing merge conflicts and making co-development smoother compared to shared development instances.
-   Safely test configurations, workflows, and integrations within your own sandbox before promoting changes, reducing rework and protecting system stability.

See  for more information.

## Activation and other requirements

-   **Activation information**

    Install the Developer Sandbox License Management \(`com.glide.dsb.licensing`\) plugin on your license management instance, install the sandbox plugin on your non-production instances, and use the license management UI in App Engine Management Center on the controller instance to distribute packs.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/build-automate-rn-landing.md)

## October 2026

The October 2026 release of Developer Sandboxes includes fully automated self-serve license assignment from App Engine Management Center and four free sandbox licenses available on all non-production instances.

### What's new

-   **Fully automated setup with self-serve license assignment**

    Assign purchased sandbox packs to non-production instances directly from the **Developer Sandbox Management** tab in App Engine Management Center \(AEMC\), without opening a support case. Install the new licensing plugin on your license management instance, install the sandbox plugin on your non-production instances, and use the license management UI on the controller instance to distribute packs. Each pack provides 10 sandboxes, and you can assign a maximum of 3 packs to a single non-production instance.

    In support, the following have been added when the new com.glide.dsb.licensing plugin is installed:

    -   A new instance allocation table \[sys\_dsb\_instance\_allocation\] is now installed with Developer Sandboxes.
    -   The new sandbox admin role \(`sn_dsb_commons.sandbox_license_admin`\) lets users distribute sandbox packs to non-production instances without full admin access.
-   **Four free sandbox licenses**

    All instances now get four free sandboxes per non-production instance to try out Developer Sandboxes. You can use the four free licenses on the same instance as purchased sandboxes, for a maximum of 34 sandboxes on an instance.


### Plugin information

-   **New plugins**

    Developer Sandbox License Management \(`com.glide.dsb.licensing` \): Use this plugin to assign sandbox licenses from AEMC. Install on your controller instance to distribute sandbox packs to non-production instances. Use the com.glide.dsb.licensing plugin from only one production instance, the instance you're using to assign licenses.


## Brazil Early Availability

The Brazil Early Availability release introduces sandbox pooling for faster provisioning and automatic update set sources between production and sandbox instances.

### What's new

-   **Sandbox pooling for faster provisioning**

    Allocate sandboxes faster using pre-pooled instances. When you allocate a sandbox, you claim one from a pre-created pool rather than waiting for a new instance to be provisioned. Sandbox URLs are randomly generated strings and no longer match the sandbox display name. The display name remains configurable, but you can't change the URL.

    **Note:** Because pooled sandboxes are precreated, they may be out of date from the current base instance state, but are refreshed every 24 hours.

-   **Automatic update set sources**

    Transfer update sets between production and sandbox instances without manual configuration. When a sandbox is created, an update set source pointing to the sandbox is automatically created on the base instance, and an update set source pointing to production is automatically created on the sandbox. When a sandbox is retired, both update set sources are automatically removed.


### What's deprecated or removed

-   **Form changes**
    -   The **Sandbox alias** URL field has been removed from the Allocate Sandbox form. Because sandbox URLs are now randomly generated, you no longer specify a URL at allocation time.
    -   Sandbox templates have been removed from the Allocate Sandbox form.

