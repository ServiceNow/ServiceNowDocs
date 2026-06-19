---
title: Sample process administration with domain specific applications
description: The following example illustrates process administration with domain-specific applications and modules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/servicenow-ai-platform-security/r\_ExDelAdmDomAppMod.html
release: zurich
product: ServiceNow AI Platform Security
classification: servicenow-ai-platform-security
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Process administration, Setup and administration, Domain separation for service providers, Access Management]
---

# Sample process administration with domain specific applications

The following example illustrates process administration with domain-specific applications and modules.

As the administrator of the Oceanic domain, David Loo decides to customize the Configuration application. To start with, David reviews the modules available in the Configuration application module.

\[Omitted image "Domain\_overrides\_appmod\_01.png"\] Alt text:

David decides to rename the Configuration application to CMDB and to allow the inventory\_admin role to see the application.

\[Omitted image "Domain\_overrides\_app\_02.png"\] Alt text:

Next, David decides to change the Incident application by activating the **Open - in "New" State** module and adding a new filter item to show open incidents in the Oceanic category.

\[Omitted image "Domain\_overrides\_mod\_03.png"\] Alt text:

This creates a new module entry in the application rather than overwriting the existing module in the global domain.

\[Omitted image "Domain\_overrides\_mod\_04.png"\] Alt text:

If another administrator from another domain, such as Fred Luddy, logs in and looks at the Configuration application, the settings from the global domain appear.

\[Omitted image "Domain\_overrides\_appmod\_04.png"\] Alt text:

\[Omitted image "Domain\_overrides\_appmod\_05.png"\] Alt text:

