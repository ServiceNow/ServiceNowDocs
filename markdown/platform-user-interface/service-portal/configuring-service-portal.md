---
title: Configuring Service Portal
description: Plan and set up a self-service portal for your employees or customers.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Service Portal, Configure UIs and portals, Configure user experiences]
---

# Configuring Service Portal

Plan and set up a self-service portal for your employees or customers.

## Configuration overview

The following list is a high-level overview of the workflow to get started configuring a portal. However, there may be use cases where performing these steps in a different order is preferred.

1.  [Upgrade Service Portal](../task/upgrading-service-portal.md)

    If you upgraded from a previous release, you might need to perform additional tasks to take advantage of new or updated functionality in Service Portal.

2.  [Create a new portal or update a base system portal](../task/create-a-portal.md)

    A portal is the engine that houses all the references to content for your site. The portal record defines the URL extension for a site, as well as things like the knowledge base, catalog, and homepage. You can also use the portal record to define the header menu and the portal branding. You can create a new portal or update an existing base system portal to suit your needs.

3.  [Configure portal branding](c_BrandingEditor.md)

    With the Branding Editor, you can configure the styles and theme of your portal in a view with real-time updates. You can see how your portal appears to users with the click of a button. More advanced users still have the option of creating CSS style sheets for the portal theme. However, they won't take advantage of the real-time update that the Branding Editor provides. Changes made in the Branding Editor or to specific components of the portal \(such as a widget or a page container\) override any customizations made to the theme. If you need more customization than what the Branding Editor can provide, see [Create a portal theme](c_CustomCSS.md).

4.  [Create new pages or update base system pages](../task/t_ConfigureAPage.md#) and [configure widgets](service-portal-widgets.md)

    Pages are the centerpiece of the end-user experience. Page definitions not only control the layout of the content, they craft the experience for the user. Pages also help define mobile responsiveness, which is a key component in the user experience. Use any existing base system pages as an example for your own creation or create new pages from scratch.

    Widgets are what define the content of your pages. You can use the base system widgets provided with Service Portal to get started configuring pages.

5.  [Configure search in a portal](search-service-portal.md)

    Search data displays within a widget on the search page. To make data searchable from a portal, create a search source that fetches data from a single table within your instance, from multiple tables, or from an external site. Enable AI Search to take advantage of intelligent query features and quickly find the answers they need.

6.  [Manage access to a portal](portal-security.md)

    Manage who can access your portal by making pages public, configuring user logins and single sign-on, limiting page access by role, or enabling multi-factor authentication. You can also use advanced user criteria for access to pages, widgets, and more.


## Common portal configurations

Refer to this video for examples of common configurations for portals.Learn about configuring redirection, landing page branding, and language selection in portals.

