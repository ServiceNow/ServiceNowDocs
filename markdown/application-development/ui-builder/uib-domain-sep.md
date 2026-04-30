---
title: Learn about domain separation
description: Domain separation is supported for UI Builder . Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Learning UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Learn about domain separation

Domain separation is supported for UI Builder. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Overview

UI Builder is a web user interface builder. UI Builder enables developers to build new pages or customize existing pages for web-based workspace experiences using Next Experience Components and custom web components. In addition, UI Builder supports Domain Separation, which is the ServiceNow® instance-wide multi-tenant architecture.

Enable developers or dashboard builders in domain-separated environments to safely create UI application screens or dashboards while in the same browser window. Domain Separation in UI Builder works similarly to application scope to help administrators safely create or edit in a multi-tenant environment.

It’s important to understand a key principle to maintaining a stable, healthy, and scalable ServiceNow® instance, where Domain Separation is installed.The primary principle is standardization. Standardization means a common configuration that most the instance operates by. When an instance has hundreds or thousands of domains, managing them successfully requires rigorous governance. Domain-specific configurations should be used only if they are deemed necessary by the instance owners. Generally, most instances should follow the common instance configuration. Doing so provides a more uniform experience across the instance. It also lets instance owners minimize code sprawl that slows the adoption of new ServiceNow® features included as part of release upgrades.

## How domain separation works in UI Builder

Domain separation in UI Builder works similarly to application scope to help administrators safely create or edit in a multi-tenant environment.

UI Builder is compromised of a framework of interlocked components that you use to create web-based workspaces, dashboards, or portals. While the application supports domain separation, it does not mean every component or table is domain separated, which is important for instance owners to understand.

If the current domain does not match the domain of the variant or dashboard, the record is read-only. If a user has access to the domain, they can choose to switch their domain to the domain of the record. Alternatively, users can edit the record. Editing the record temporarily forces the user session into that record’s domain. They can then make edits without fear of accidentally creating an override.

The following diagram shows what is \(in green\) and is not \(in blue\) domain separated in UI Builder.

![Diagram of what is, and what is not, domain separated in UI Builder.](../image/UIB-domain-separation-included.png)

Not shown in the diagram are viewports, declarative actions, and screen applicabilities, which are domain supported as process.

Data and Process/UI separation are important when considering domain separation architecture. UI Builder fully supports data and process/UI separation, and any data \(records\) displayed in the web-based workspace, dashboard, or portal experiences.

For example, a change request that belongs to the domain of Acme only shows for users who have access to the domain of Acme in an experience built using UI Builder. Conversely, if an application does not support data separation, its records won't be domain separated by the workspace or portal experience.

Process/UI separation tables that form the underpinning framework in UI Builder are process separated, and a sys\_override column exists on those tables. For example, if a page is created in Global, any changes to the logic created and saved in a sub domain results in an override.

For items that are not domain separated, any change to the logic globally affects any page or dashboard that references its content. Understanding domain separation is critical when interacting with these elements.

## Domain Selection menu, messaging, and managing overrides

When designing a workspace, dashboard, or portal experience using the UI Builder \(including Dashboard Builder\), a system administrator or ui\_builder\_admin has access to a **Domain Selection** menu in UI Builder. A system administrator or ui\_builder\_admin should switch to the proper domain prior to creating, editing, or overriding a variant or dashboard page.

By default, the ui\_builder\_admin role does not have access to the **Domain Selection** menu. The **Domain Selection** menu must be coupled with a role that grants access, such as ITIL, or it can be added via system property. For more information, see [Enable domain selection menus in Core UI](https://www.servicenow.com/docs/access?context=t_EnableDomainReferencePickerProperty&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

In addition, the **Domain Selection** menu also shows **Expand/Collapse Domain Scope**, that is displayed while the system administrator or ui\_builder\_admin is in Global. Select **Expand** to show any variant or dashboard that has been overridden, or exists as a standalone in a sub domain. Select **Collapse** to only show variants or dashboards created in Global.

Lastly, domain hierarchy is available from the **Domain Selection** menu. For deep-domain hierarchies, the user may have to collapse the branches of the domain hierarchy to physically select the domain. In these environments, perform a search to find the domain.

UI Builder has governance controls for editing and overriding variants or dashboards, similar to the way application scope is handled. Both application scope and domain scope are handled concurrently in UI Builder.

For example, if a variant was created in Global, but the current domain of the system administrator is set to Acme, then that variant is read-only. As long as that screen is not in a private scope that prevents editing, the system administrator or ui\_builder\_admin have two options. They can temporarily transact into the global domain if they have access to Global. Or, they can create an override.

You can edit the domain separation to make quick changes to the variant or dashboard and its content. When you edit the domain, you temporarily transact into the same domain scope as the variant or dashboard. Going into the same scope prevents accidental overrides when modifying certain settings such as Name, Order, Event Mappings, Page Definition configurations\) tied to the variant. While in edit mode, not all settings are available in page management. For full capabilities, switch into the correct domain prior to editing the record.

Create Override allows a system administrator or ui\_builder\_admin to create an override of an existing variant or dashboard. Create an override of a variant or dashboard to perform an extensive copy of the page definition content, minus screen conditions and audiences in the user’s currently selected domain. The sys\_override column is then updated appropriately.

Viewports, which are variants in and of themselves, are domain separated, and are typically nested inside page definition content. Some viewports may not copy over. For example, a viewport \(displayed as a tab set\) that was created as an override in a domain of a Global viewport would not be carried in the page definition content during the override creation process.

As screen conditions and audiences may be specific to a domain, this content is not carried over during the override creation process. A screen prompts the system administrator or ui\_builder\_admin to create screen conditions and audiences.

A user cannot create an override of a variant or dashboard in Global if the item exists in a sub domain, or if an override exists for that variant or dashboard in the same sub domain.

After the override and the conditions and audiences are set, the content and configurations can be configured as needed. As standard to domain separation, the override is no longer affected by any changes done to the original variant or dashboard. The workspace, dashboard, or portal experience displays these overridden configurations if the user’s current domain session is within the affected domain or sub domains where this override was created. Audiences further determine what a user may or may not see.

In addition, a user can access the domain hierarchy to view existing overrides from higher domains. For example, Global &lt;- Top &lt;- Acme &lt;- Current domain. If no overrides exist, the default variant or dashboard are displayed. The exception is if the default variant or dashboard is in a child domain or a peer domain.

![Example overrides in domain separation.](../image/UIB-domnain-separation-example1.png)

If you select **Expand Domain Scope** while in Global, all variants and overrides in sub domains are shown as previously mentioned.

System administrators and ui\_builder\_admin can see what has been created in the ServiceNow® platform.

## Viewports and domain separation

Viewports are variants that can be nested in page definition content. They can be created as a common configuration in Global, or can be overridden per sub domain.

## Declarative actions and domain separation

Declarative Actions can be overridden per domain as well. A system administrator or ui\_builder\_admin should select the appropriate domain prior to creating a domain specific declarative action override.

**Parent Topic:**[Learning UI Builder](learning-uib.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

