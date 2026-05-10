---
title: Configuring a form action to open a custom modal
description: Configure a form action to open a custom modal that provides information or interactive elements without navigating away from the current page.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configuring a form action to open a custom modal

Configure a form action to open a custom modal that provides information or interactive elements without navigating away from the current page.

To configure a declarative action to open a custom modal, complete the following actions:

-   **Create a declarative action button**
-   **Configure a page variant**
-   **Configure a modal**
-   **Configure a UX add-on event mapping record**
-   **Define the payload**

Configuring an action button to open a custom modal involves several processes:

1.  Opening your record page in UI Builder:

    Accessing your record page in UI Builder enables you to design and configure the page variant with a custom modal. For more information, see [Create a page variant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/create-variant.md).

2.  Designing the page variant in UI Builder:

    Using UI Builder to design a page variant passes the modal into the workspace record page. For more information, see [Design a page variant in UIB](design-a-page-variant-in-uib.md#).

3.  Configuring the page variant as a modal in UI Builder:

    Using UI Builder to configure the page variant defines the modal to appear in the workspace record page. For more information, see [Configure a page variant as a modal in UIB](configure-a-page-variant-as-a-modal-in-uib.md#).

4.  Creating a UX add-on event mapping:

    Setting up a UX add-on event mapping connects the action button to your custom modal. For more information, see [Create a UX add-on event mapping](create-a-ux-add-on-event-mapping.md#).

5.  Defining the payload for a custom modal:

    Configuring the payload sets the action button to open the custom modal in your workspace. For more information, see [Define the payload for a custom modal](define-the-payload-for-a-custom-modal.md#).


