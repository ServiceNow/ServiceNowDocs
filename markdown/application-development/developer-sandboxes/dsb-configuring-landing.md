---
title: Developer Sandboxes installation and configuration
description: Developer Sandboxes installation and configuration covers Developer Sandboxes on your instance. Review entitlements, install the plugins, assign licenses, and look up the roles, tables, and properties that control how sandboxes work.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/developer-sandboxes/dsb-configuring-landing.html
release: australia
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: concept
last_updated: "2026-10-26"
reading_time_minutes: 3
keywords: [configure, install, developer sandboxes, sandbox license assignment, sandbox properties]
breadcrumb: [Developer Sandboxes, Build, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Developer Sandboxes installation and configuration

Developer Sandboxes installation and configuration covers Developer Sandboxes on your instance. Review entitlements, install the plugins, assign licenses, and look up the roles, tables, and properties that control how sandboxes work.

## Configuration overview

Complete these tasks in the following order. You must install Developer Sandboxes and set up the instance before you can assign licenses to it.

1.  [Review your entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dev-sbx-entitlements.md)

    Review the entitlements that determine whether you have access to Developer Sandboxes, how sandbox packs are sized, and how many sandboxes an instance can have.

2.  [Install Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dev-sbx-installing.md)

    Review the prerequisites, install the plugins, and set the required properties.

3.  [Enable SSO if needed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dev-sbx-sso.md)

    If you use single sign-on \(SSO\), set the properties on the base instance that let developers use SSO to access sandboxes.

4.  [Assign licenses to instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dsb-license-allocation-about.md)

    Assign purchased sandbox packs to non-production instances from App Engine Management Center \(AEMC\) without opening a support case. You need access to AEMC with the sandbox\_license\_admin role role to open the license assignment page, and the app\_engine\_admin role is required.


## Additional configuration information

Use these topics to set up related features and look up what is installed with Developer Sandboxes.

-   [Developer Sandboxes domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dsb-domain-separation.md)

    Set up domain separation on the base instance before sandboxes are created, so that sandboxes inherit the domains you define.

-   [Components installed with Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dsb-installed-with.md)

    Look up the roles, plugins, and tables that are installed with Developer Sandboxes.

-   [Properties installed with Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dsb-properties-installed.md)

    Look up the system properties that govern sandbox behavior, such as node counts, table configuration, and data copy settings.


-   **[Developer Sandboxes entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dev-sbx-entitlements.md)**  
Your company's entitlements determine whether you have access to Developer Sandboxes.
-   **[Developer Sandboxes installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dev-sbx-installing.md)**  
Developer Sandboxes is installed on your instance, with licenses from a pack assigned by your admin. Review prerequisites and plugin requirements before installation begins.
-   **[Single sign-on for Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dev-sbx-sso.md)**  
Sandboxes use the same login credentials as the base instance, including single sign-on \(SSO\) when it's enabled there. Set the required properties on the base instance so developers can use SSO to access sandboxes.
-   **[License assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dsb-license-allocation-about.md)**  
License assignment in App Engine Management Center \(AEMC\) lets Developer Sandboxes admins distribute purchased sandbox packs across non-production instances without opening a support case. Each pack contains 10 sandboxes, and assignments are managed from a license management instance.
-   **[Developer Sandboxes domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dsb-domain-separation.md)**  
Domain separation is supported for Developer Sandboxes. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Components installed with Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dsb-installed-with.md)**  
Several types of components are installed with activation of Developer Sandboxes, including tables and user roles.
-   **[Properties installed with Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dsb-properties-installed.md)**  
The system properties available in Developer Sandboxes govern application behavior, enabling developers to configure and optimize their testing environments effectively.

**Parent Topic:**[Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/sandboxes-landing.md)

