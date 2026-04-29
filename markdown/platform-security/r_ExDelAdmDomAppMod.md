---
title: Sample process administration with domain specific applications
description: The following example illustrates process administration with domain-specific applications and modules.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Process administration, Setup and administration, Domain separation for service providers, Access Management]
---

# Sample process administration with domain specific applications

The following example illustrates process administration with domain-specific applications and modules.

As the administrator of the Oceanic domain, David Loo decides to customize the Configuration application. To start with, David reviews the modules available in the Configuration application module.

![](../image/Domain_overrides_appmod_01.png "Starting view of the Configuration application")

David decides to rename the Configuration application to CMDB and to allow the inventory\_admin role to see the application.

![](../image/Domain_overrides_app_02.png "Sample domain-specific changes to the Configuration application")

Next, David decides to change the Incident application by activating the **Open - in "New" State** module and adding a new filter item to show open incidents in the Oceanic category.

![](../image/Domain_overrides_mod_03.png "Sample domain-specific changes to the Open - "New" State module")

This creates a new module entry in the application rather than overwriting the existing module in the global domain.

![](../image/Domain_overrides_mod_04.png "Domain-specific view of the Incident application")

If another administrator from another domain, such as Fred Luddy, logs in and looks at the Configuration application, the settings from the global domain appear.

![](../image/Domain_overrides_appmod_04.png "David Loo's view of applications")

![](../image/Domain_overrides_appmod_05.png "Fred Luddy's view of applications")

