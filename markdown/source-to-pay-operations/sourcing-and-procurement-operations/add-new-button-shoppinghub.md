---
title: Add a button in Shopping Hub
description: You can add a button to a Shopping Hub page by using UI Builder.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/add-new-button-shoppinghub.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-08-31"
reading_time_minutes: 3
breadcrumb: [Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Add a button in Shopping Hub

You can add a button to a Shopping Hub page by using UI Builder.

## Before you begin

Role required: ui\_builder\_admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  On the **Experiences** list, select **Shopping Hub**.

    \[Omitted image "sh-experiences.png"\] Alt text: UI Builder Experiences list filtered to Shopping Hub, with the Shopping Hub row selected.

3.  Under **Pages**, select the page where you want to add the button.

    \[Omitted image "sh-shoppinghub-pages.png"\] Alt text: Shopping Hub experience overview showing the list of pages, such as Home, Categories, and Checkout.

    Make sure you're editing in the same application scope as the rest of the page before you start.

4.  Select the **+** in the container where you want the button to appear, and then select the **Button** component from the toolbox.

5.  Select the component, select the **Configure** tab, and set the button's label and any other properties you want to change.

6.  Select the **Events** tab, and then select **Add event mapping** \(or **Add handler**\) to make the button perform an action when a user selects it.

    A button component has only one event, `button-clicked`. Choose the handler you want from the list \(for example, navigating to another page, or opening a modal\), select **Continue**, configure the payload for the event, and then select **Add**.

7.  Select **Save**, and then select **Preview** to confirm that the button works as expected.


## Result

The new button is displayed on the Shopping Hub page and performs the configured action when a user selects it.

## What to do next

For more information about UI Builder, see [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder-overview.md).

**Parent Topic:**[Configuring Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/configuring-spo.md)

**Related topics**  


[Sourcing and Procurement Operations product tile]()

[Sourcing and Procurement Operations Product Hub]()

[Install Sourcing and Procurement Operations]()

[Sourcing and Procurement Operations Configuration Console]()

[Configure Sourcing and Procurement Operations]()

[Setting up primary data for ShoppingHub]()

[Configure punchout for third-party site purchases]()

[Configuring work prioritization]()

[Add a footer link in Shopping Hub]()

[Customize your top suppliers on Shopping Hub]()

[Configure conditions for merging purchase requisitions]()

[Service portal configuration for ShoppingHub]()

[Install ShoppingHub Mobile]()

[Advanced Work Assignment for Source-to-Pay Operations]()

[Install Universal Request for Sourcing and Procurement Operations]()

