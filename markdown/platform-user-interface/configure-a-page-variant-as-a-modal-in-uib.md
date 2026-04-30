---
title: Configure a page variant as a modal in UI Builder
description: Define your page variant to appear as a modal using UI Builder configurations. This step acts as part of the process to configure an action button to open a custom modal.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure a custom form modal, Configure action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure a page variant as a modal in UI Builder

Define your page variant to appear as a modal using UI Builder configurations. This step acts as part of the process to configure an action button to open a custom modal.

## Before you begin

Complete the following actions:

-   [Create a form action](create-a-new-form-action.md)
-   [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)
-   Open your record page in UI Builder or [create a page variant in UI Builder](https://www.servicenow.com/docs/access?context=create-variant&version=zurich&pubname=zurich-application-development&ft:locale=en-US)
-   [Customize a page variant in UI Builder](design-a-page-variant-in-uib.md#)

Role required: admin

## Procedure

1.  Open your page variant.

2.  Open the **sys\_ux\_screen\_type** by selecting the menu icon \(![menu icon](../../workspace/image/menu-icon-save.png)\) and navigating to **Developer** &gt; **Open variant collection record**.

3.  Select the **UX App Route** tab under Related Lists and select your page variant.

4.  Open UI Builder in a new browser tab and open your configurable workspace experience.

5.  Find the page that you want your modal to appear by opening the overview of records for the experience and selecting the page.

6.  Select the menu icon \(![menu icon](../../workspace/image/menu-icon-save.png)\) and navigate to Open page definition.

7.  Select **Copy sys\_id**.

8.  Return to the browser tab with the **sys\_ux\_app\_route**.

9.  Open the page's machine-readable value in a browser alert modal by double-selecting the **Parent Macroponent** field and selecting **OK**.

10. Define the variant to appear in a modal by entering `modalContainerViewport` in the **Parent Macroponent Composition Element ID** field.

11. Select **Update**.


