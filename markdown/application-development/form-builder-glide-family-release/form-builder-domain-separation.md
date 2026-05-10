---
title: Domain separation and Table Builder
description: Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Form Builder \(Glide Family Release\)
classification: form-builder-glide-family-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Table Builder, Table Builder, Builder library, Developing your application, Building applications]
---

# Domain separation and Table Builder

Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard\*

The support level is Standard but has some exceptions or special conditions.

-   Includes all aspects of **Basic** level support.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must be able to configure minimum viable product \(MVP\) business logic and data parameters. This configuration is done per tenant, as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## Overview of domain separation

Table Builder enables developers to configure the layout and logic for each form view for tables in their application. When launched from UI Builder, Table Builder supports domain separation, which is the ServiceNow instance-wide multi-tenant architecture.

**Note:** Domain separation is supported for Table Builder when it is launched from UI Builder. Domain separation is not supported when launching Table Builder from App Engine Studio.

Table Builder enables developers in domain-separated environments to create forms while they are in the same browser window. Domain separation in Table Builder works similarly to an application scope that helps administrators to create or edit in a multi-tenant environment.

Standardization is the key principle to maintaining a stable, healthy, and scalable ServiceNow instance, where domain separation is installed. By having standardization, you have a common configuration that most of the instance operates by. When an instance has hundreds or thousands of domains, managing them successfully requires rigorous governance. Domain-specific configurations should be done only if they are deemed necessary by the instance owners. Most instances should follow the common instance configuration to provide a more uniform experience across the instance. It also lets instance owners minimize the code sprawl that slows the adoption of new ServiceNow features that are included as part of the release upgrades.

## How domain separation works in Table Builder

Table Builder enables developers to switch the session domain to create domain overrides to the form layout, section layout, and form logic. System dictionary record changes \(such as field metadata for a field label\) do not require domain overrides. Form layout changes require domain overrides to both the form record and the section when the change is performed at a lower domain. When creating a domain override, section labels can't be edited prior to saving the override.

**Note:** UI policies can have overrides at lower domains, as well. An override indicator appears on the UI policy.

In the global domain, a developer can expand the domain scope to see all form views from different domains. Developers can see all form views and views with overrides that are indicated with an icon.

**Note:** Single section form records do not have a **sys\_ui\_forms** record attached to it. Instead, these records only have an attached **sys\_ui\_section** record until a second section is created. If a single section form has existing domain overrides, and the developer adds another section to the form, the existing domain overrides will break.

**Parent Topic:**[Exploring Table Builder](exploring-fb.md)

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

