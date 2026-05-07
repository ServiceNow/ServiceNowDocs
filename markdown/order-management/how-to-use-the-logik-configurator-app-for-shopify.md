---
title: Integrating CPQ with Shopify
description: The CPQ app for Shopify enables stores to seamlessly manage and sell configurable products using CPQ advanced CPQ \(Configure, Price, Quote\) features. Installation and setup are streamlined, and robust Admin options are provided for both technical and non-technical users.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# Integrating CPQ with Shopify

The CPQ app for Shopify enables stores to seamlessly manage and sell configurable products using CPQ advanced CPQ \(Configure, Price, Quote\) features. Installation and setup are streamlined, and robust Admin options are provided for both technical and non-technical users.

The CPQ app for Shopify is a fully featured connector for a Shopify store. The app ensures the entire product catalog is available in CPQ for use with a CPQ blueprint. The app also includes an app block to add a configurator to any page on a storefront without the need to create a dedicated UI. The configurator app block is fully functional out of the box which means customers can start adding configurable products to their cart as soon as the storefront changes are published.

-   The CPQ app brings your entire Shopify product catalog into CPQ, allowing complex configurations for B2C and B2B sales.
-   Features an app block to easily add a product configurator to any storefront page—no custom code required.
-   Provides live catalog sync from Shopify to CPQ every fifteen minutes \(one-way sync\).
-   Enables Shopify B2B Pricing by deferring to Shopify catalog prices for B2B users.

The CPQ app for Shopify is free to download on the Shopify app store:

[Logik‑ Product Configuration](https://apps.shopify.com/logik-1)

## Setup

After downloading the CPQ app it will automatically appear in the Apps section of the store.

To start using the app, the CPQ environment details and a token must be entered in the CPQ settings section of the app landing screen. For more information about creating a CPQ token, see [Set up a runtime client](../task/cpq-set-up-a-runtime-client.md).

**Note:** Ensure the storefront and the Admin URLs are added as an origin for the token. All stores should also include the following static URL to their list of origins: [https://shpfy-connect.ecommerce.logik.io](https://shpfy-connect.ecommerce.logik.io/).

## CPQ app Admin screen overview

![Admin screen overview](../images/cpq-app-admin-screen.png)

-   **Logik Settings**: Logik environment settings which is required in order for the configurator to display
-   Instructions: This block summarizes at a high level what is needed for a configurable product. The ‘Add to Current Themeʼ button will also automatically place the app block on the product page template.
-   Configurable Products: Redirects to a page for **Logik enabled products** in the store catalog
-   Order Configuration: Redirects to a Logik specific create order page so that an Admin can add a Logik configurable product to an order

## Managing products

When the app is installed and the **Logik settings** have been successfully saved, an automated catalog sync will begin and the custom CPQ attribute is added to the product details Admin page.

## Product catalog synchronization

Products are synced down from Shopify to CPQ every fifteen minutes. All products in the store catalog will be synced to CPQ. Changes will be synced the next time the job runs.

Products from Shopify will appear on the Products and Configurable Products table. The Shopify GID is automatically mapped to the Product ID field on the table.

![Product catalog](../images/cpq-product-catalog-sync.png)

**Note:** The product syncs are one way. Changes to the product table will not be reflected in the Shopify catalog.

## Configurable products

In order for a product to appear on the Configurable Products table as well the configurator to display, a product must have **Logik is Configurable** attribute set to True.

![metafields](../images/cpq-cps.png)![configurable products](../images/cpq-cps-1.png)

## Using Shopify B2B pricing

In order to use Shopify B2B Pricing, all products associated to a CPQ Blueprint must be present in a catalog. The catalog must also have at lease one company location associated to it alongside a user who belongs to that company.![Shopify B2B](../images/cpq-b2b-test.png)

When a user is logged in from an included company location, CPQ pricing will default to the Shopify catalog price. This will overwrite any CPQ price rules for these products. It is recommended that B2B specific blueprints are created to avoid any confusion around pricing in this scenario.

## Adding a configurator to a page

The CPQ Configurator can be added to any page via an included app block through the page editor. The app block is automatically added to your store when the app is installed. You can find the block under apps when adding a new page section.

The look and feel of the **Logik configurator** is managed in CPQ Admin through use of the layout editor. However, there are additional options in the CPQ app block. If you encounter issues where the Font is too small or large, that can be modified in the app block settings along with spacing.

## Product Pages

For product pages, the CPQ app landing page has a shortcut to directly add the app block to the product page template.

The default behavior on a product page is to use the current product as the configurable product. If the product is **Logik configurable**, the configurator will display. If not, the app block will remain hidden.

However, it is better to create a specific template for a **Logik enabled product** page, since modifications to the page content besides the app block could be needed.

![App block instructions for a product page](../images/cpq-product-pages.png)

## Content pages

When adding a **Logik configurator** to a non-product page, a specific product must be selected for use.

By default, a select option will be displayed. When clicked, a list of all products will be shown. Either click a product or enter a search term. Once selected, the product will be displayed in the app block settings.

To change the product used, click the current product then click ‘Replaceʼ to reopen the product list.![Replace product](../images/cpq-content-pages.png)

## Add to Cart vs Add to Order

The **Logik configurator** app block provides two options for how it will function. Either the app will add the configuration to the customerʼs cart directly, or a draft order of the configuration can be created for the customer. To control the behavior of the configurator on the page, the option ‘Checkout As Draft Orderʼ can be enabled or disabled.

When enabled, a customer will need to be logged in. If the customer is currently logged out, the configurator will not be shown and instead a message to inform the customer to login is displayed. Once logged in, the customer can complete the configuration as usual. After completing the configuration, the configurator will close and display a success message. This configuration will then show as a draft order in the Shopify orders screen in the Admin. The customerʼs email used to login will be included in the order.

![Check out screen](../images/cpq-add-to-cart.png)

If the setting is disabled, once the configuration is completed. All items included in the configuration are added directly to the customerʼs cart and the customer is redirected to the cart page.

## Managing configurable products in Shopify Admin

Configurable Products List:

On the Logik app landing page, once the CPQ credentials have been saved, a configurable product section is shown.

Clicking into the page will display a list of all products that are **Logik configurable** and any variants.

On the Configurable Products page, each product has two buttons. The details button redirects the Shopify user to that productʼs details page in the Shopify Admin so they can edit any product details.

The order button will redirect the Shopify user to the Create Draft Order page and open the configurator for the selected product.

## Creating a draft order

![Creating a draft order](../images/cpq-draft-order1.png)

On the Create Draft Order page, a Shopify user can select a CPQ configurable product to launch itʼs configurator. Once a product is selected and the submit button is clicked, the associated blueprint is displayed.

![Creating a draft order](../images/cpq-draft-order.png)

Once the configurator has been loaded, the Shopify user can complete a configuration just like a customer. Once complete, all items in the configuration are added to a new draft order and the user is redirect to that orderʼs page.

![Creating a draft order](../images/cpq-draft-order2.png)

From the order page, the user can complete the order like any other Shopify order.

## Editing a Configurable Product in a draft order

On the draft order page, a Shopify user can edit a Logik configurable product that is included in the order. The user will select the product from the dropdown then click the ‘Reconfigureʼ button, which will redirect to the create draft order page.

![Editing a Configurable Product in a draft order](../images/cpq-draft-order3.png)

The existing configuration will automatically load on the page and the user will then have the ability to make any changes before saving. Once saved, the user will be redirected to the order.

## Using the app with headless implementations

The CPQ Shopify app is not required for users who wish to integrate CPQ with their Shopify storefront. However, the app is designed with headless implementations in mind.

Here are some considerations when using the app for your headless implementation:

The app will streamline the setup with CPQ and reduce the overall need for custom middleware by providing a product sync between platforms, a custom CPQ Configurable product attribute and Draft Order functionality.

A Custom UI can be used in place of the CPQ app block which is completely optional.

Saving a configuration, even heedlessly, will trigger the CPQ add to cart function which facilitates dynamic pricing and attributes Automated add to cart on save can be disabled through a DevOps request.

## Clearing app settings

In any case where you need to clear the app settings, they can be manually deleted in your Shopify store settings: Go to the Metafields and metaobjects page and select **logikconfig**.

Click the ‘More Actionsʼ drop down menu and click ‘Delete metaobjectʼ.

![Clearing app settings](../images/cpq-clear-app-settings.png)![Clearing app settings](../images/cpq-clear-app-settings2.png)

