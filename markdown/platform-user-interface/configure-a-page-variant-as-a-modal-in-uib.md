---
title: Configure a page variant as a modal in UIB
description: Define your page variant to appear as a modal using UI Builder configurations. This steps acts as part of the process to configure an action button to open a custom modal.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure a custom form modal, Configure action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure a page variant as a modal in UIB

Define your page variant to appear as a modal using UI Builder configurations. This steps acts as part of the process to configure an action button to open a custom modal.

## Before you begin

Complete the following actions:

-   [Create a form action](create-a-new-form-action.md)
-   Open your record page in UIB or [create a page variant in UIB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/create-variant.md)
-   [Design your page variant in UIB](design-a-page-variant-in-uib.md#)

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


