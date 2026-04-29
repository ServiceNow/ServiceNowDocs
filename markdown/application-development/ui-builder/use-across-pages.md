---
title: Use pages across experiences
description: Use pages created in one in experience in another without needing to rebuild the page.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage UI Builder pages and page variants, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Use pages across experiences

Use pages created in one in experience in another without needing to rebuild the page.

## Benefits of sharing pages across experiences

Pages shared across experiences enable administrators and page builders to reuse a single page in multiple experiences without creating duplicate copies. When a page is shared, you can access it from any experience where available, reducing context switching and providing a consistent experience.

A shared page exists as a single source, any updates to that page are automatically reflected everywhere it's used. This simplifies maintenance, reduces the risk of errors from managing multiple copies, and requires less time.

## Viewing shared pages in Experience View

Pages that can be used across experiences display a blue icon containing two pages in UI Builder's experience view. You can select the icon to go to the **UX App Route** settings page on the platform where you can enable or disable the ability to use the page across experiences.![Reuse page across experiences](../image/use-across-exp-icon.png)

Reusable pages added to your experience display the name of their source experience. Select the icon next to the page title to view details about the page, access the original experience, adjust page settings, or explore linked pages.![View reusable page details by selecting the page](../image/use-across-exp-page.png)

## Limitations

When sharing a page, you must specify all the linked pages associated with it. **Linked pages** are pages whose routes are tied to the same source experience. This is required so that the experience receiving a shared page has references to all necessary outbound pages.

**Note:** Shared pages can only be configured in the ServiceNow® platform currently. However, you can view these pages while in the Experience View of UI Builder.

-   **[Enable pages to be used across experiences](../task/enable-use-across-exp.md#)**  
Select pages that you want to share across experiences in UI Builder.
-   **[Add shared pages to an experience](../task/add-shared-pages-to-an-experience.md)**  
Add a page from another experience so that users can access shared content without duplicating pages.

**Parent Topic:**[Manage UI Builder pages and page variants](work-pages.md)

