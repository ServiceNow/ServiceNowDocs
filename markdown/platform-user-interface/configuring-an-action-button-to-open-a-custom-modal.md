---
title: Configuring an action button to open a custom modal
description: After you add an action button to your configurable workspace, you can configure the button to open a custom modal.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Customizing Configurable Workspace with declarative actions, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configuring an action button to open a custom modal

After you add an action button to your configurable workspace, you can configure the button to open a custom modal.

Buttons execute actions in your configurable workspace. Custom modals provide information or interactive elements without navigating away from the current page through pop-up boxes. Integrating custom modals with action buttons creates a seamless and interactive experience, enabling you to perform actions intuitively.

## Processes for creating a custom modal

Configuring an action button to open a custom modal involves several processes:

1.  Adding the action button to the form:

    Creating an action adds the button to the form without assigning it to do anything when selected. For more information, see [Create a form action](create-a-new-form-action.md).

2.  Activating Customer Service Management:

    Adding the Customer Service plugin provides demo data and activates related plugins that are not already active. For more information, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

3.  Opening your record page in UI Builder:

    Accessing your record page in UI Builder enables you to design and configure the page variant with a custom modal. For more information, see [Create a page variant](https://www.servicenow.com/docs/access?context=create-variant&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

4.  Designing the page variant in UI Builder:

    Using UI Builder to design a page variant passes the modal into the workspace record page. For more information, see [Design a page variant in UIB](design-a-page-variant-in-uib.md#).

5.  Configuring the page variant as a modal in UI Builder:

    Using UI Builder to configure the page variant defines the modal to appear in the workspace record page. For more information, see [Configure a page variant as a modal in UIB](configure-a-page-variant-as-a-modal-in-uib.md#).

6.  Creating a UX add-on event mapping:

    Setting up a UX add-on event mapping connects the action button to your custom modal. For more information, see [Create a UX add-on event mapping](create-a-ux-add-on-event-mapping.md#).

7.  Defining the payload for a custom modal:

    Configuring the payload sets the action button to open the custom modal in your workspace. For more information, see [Define the payload for a custom modal](define-the-payload-for-a-custom-modal.md#).


