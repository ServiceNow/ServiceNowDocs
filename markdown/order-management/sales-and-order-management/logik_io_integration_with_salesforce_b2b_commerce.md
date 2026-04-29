---
title: CPQ integration with Salesforce B2B Commerce
description: Learn how to configure CPQ to work with Salesforce B2B Commerce.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [CPQ with other apps, Integrate, Sales and Order Management]
---

# CPQ integration with Salesforce B2B Commerce

Learn how to configure CPQ to work with Salesforce B2B Commerce.

## Prerequisites

This guide assumes the following:

-   Commerce is enabled in Salesforce
-   The CPQ Base Managed Package is installed
-   System Administrator or similar access is available in order to perform the steps listed

## Install files to Salesforce

1.  If it isn't already installed, download and install the Salesforce Command Line Interface \(CLI\) using the instructions here:

    [Install Salesforce CLI](https://developer.salesforce.com/docs/atlas.en-us.sfdx_setup.meta/sfdx_setup/sfdx_setup_install_cli.htm)

2.  Download and extract the logik-b2b.zip file, which contains the components used for the B2B integration, from [github.com](https://github.com/logikioopensource/b2b-accelerator/tree/main).

    -   On Mac, double-click the file. Its contents will be extracted automatically in the same location.
    -   On Windows, right-click and select Extract All". Follow the prompts that appear on screen.
    a. refer the following:

3.  Start Terminal \(Mac or Linux\) or Powershell \(Windows\).
4.  Navigate to the directory containing the extracted files. For example, if the files were extracted in the Downloads folder, type and enter the command `cd Downloads/logik-b2b`.
5.  Run the `ls` command to see a list of files and folders in that directory.

    You should see `src` and `sfdx-project.json`, as well as a plain text copy of this guide.

    ![Json file details](../images/cpq-integration-SFB2B-ls.png)

6.  Run the following command, making the changes indicated just below:

    ```
    sfdx auth:web:login --setalias myOrg -r https://example-dev-ed.my .salesforce.com
    ```

    -   Replace the URL following `-r` with the one that the Logik-B2B integration will be set up on.
    -   The text following `--setalias` is a nickname that is used to identify and reference the correct Salesforce org. The example `myOrg` will be used for the purposes of this guide. Be sure to use your own alias in the following steps.
    The URL specified in the previous login command will be opened in the default browser.

7.  Log in and authorize the "Salesforce CLI" connected app.
8.  In the command line, run the command `sfdx force:source:deploy -p src -u myOrg`.

    After a few moments, the command line will return a confirmation message, "Deploy Succeeded."

    ![json file details](../images/cpq-integration-SFB2B-deploy-succeeded.png)

    If the Salesforce org isnʼt already open in a browser, it can be opened by running the command `sfdx force:org:open -u myOrg`.


## Post-installation setup in Salesforce

You must complete the following steps after installing the components to Salesforce.

Setting Field Level Security:

1.  From Setup Home, go to the Object Manager tab, or navigate to Objects and Fields &gt; Object Manager.
2.  From Object Manager, search for and open Cart Item \(CartItem\).

    ![Object manager screen](../images/cpq-integration-SFB2B-cart-item.png)

3.  Go to Fields &amp; Relationships. Search for and open the field Configuration Id \(ConfigurationId\_\_c\).
4.  Click **Set Field-Level Security**.

    ![object manager screen](../images/cpq-integration-SFB2B-set-field-level-security.png)

5.  Make sure the Visible option is selected and Read-Only is not selected for profiles that will be configuring products in Commerce, and then click **Save**.

    ![Config screen](../images/cpq-integration-SFB2B-field-level-security-options.png)


A similar set of steps need to be followed for a Product2 field.

1.  From Object Manager, search for and open Product \(Product2\).
2.  Go to Fields &amp; Relationships. Open the field CPQ Enabled \(LGK\_\_IsConfigurable\_\_c\).
3.  Click “Set Field-Level Security”. Make sure the Visible option is selected for any shopper profiles. Read-Only can either be enabled or disabled.
4.  Save.

More field level security permissions are required if using the Add to Cart API. First, from Object Managed, search for and open Configuration Line Item \(LGK ConfigurationLineItem c\). Then, make sure shopper profiles have Field-Level Security to Visible for the following fields:

-   Quantity
-   ProductId
-   Price
-   ConfigurationId
-   Type

In addition, the following CartItem fields will need to be set to Visible \(Read-Only must not be checked\):

-   ConfigurationId \(this should already be done for the UI integration\)
-   Quantity
-   ProductId
-   Price
-   Type

## Obtaining and applying the runtime token

1.  In Logik, create a Runtime Client, with an Origin matching the Logik base URL. Click **Copy** to get the client token.

    ![Edit runtime client](../images/cpq-integration-SFB2B-runtime-client-origin.png)

2.  In Salesforce, from Setup home, go to Custom Code &gt; Custom Settings.
3.  For Logik Tenant, click `Manage`.

    ![Custom settings screen](../images/cpq-integration-SFB2B-SF-options-manage.png)

4.  If settings already exist, click “Edit”. Otherwise, click “New” above the “Default Organization Level Value” header.

    ![Tenant details](../images/cpq-integration-SFB2B-SF-custom-setting-edit.png)

5.  For the Runtime Client Token field, paste the copied token for the runtime client. Make sure the URL field\(s\) are set to the same URL as one of the runtime clientʼs Origins in CPQ Admin.

    ![Edit tenant screen](../images/cpq-integration-SFB2B-SF-custom-settings-2.png)

6.  Save.

## Setting Visualforce page access

1.  From Setup home, go to Feature Settings &gt; Digital Experiences &gt; All Sites.
2.  For your store, click `Workspaces`.

    ![Home page screen](../images/cpq-integration-SFB2B-VF-page-access-1.png)

3.  Go to Administration &gt; Pages &gt; Go to [Salesforce Platform for Application Development](http://force.com/).

    ![Admin pages](../images/cpq-integration-SFB2B-VF-page-access-3.png)

4.  Under “Site Visualforce Pages”, click `Edit`.
5.  Move `commerceConfigurationWindow` from Available to Enabled and save.

    ![Visualforce page](../images/cpq-integration-SFB2B-VF-page-access-4.png)


## Configuring the Experience Builder

1.  From the Commerce home page, open Experience Builder.
2.  Click **Home** on the top left to open the list of pages. Search or navigate to Product and click **Product Detail**. Either add the custom Logik button to the existing Product Detail page, or use the packaged page as a variation.

    ![Product details](../images/cpq-integration-SFB2B-experience-builder-1.png)

    -   To add the button to an existing page:
        1.  Click the lightning bolt on the left and go to Custom Components \(the last section in the list\).
        2.  Drag the Configurator from the list and move it to where you want it in the layout.

            ![Configurator](../images/cpq-integration-SFB2B-experience-builder-2.png)

    -   To use the packaged page as a variation:
        1.  Reopen the page navigation menu on the top left.
        2.  On the Product Detail option, click the three dots and go to the Page Variations tab.
        3.  Click New Page Variation and choose “Configurable Product Detail” as the layout.

            ![New page screen](../images/cpq-integration-SFB2B-experience-builder-3.png)

        4.  Give the variation a name and click **Create**.

## Add to Cart API

Endpoint: `/services/apexrest/add-to-cart`

Methods: Receives and returns `application/json`

POST: Use to add items to the currently active cart. \(If a cart is not active, a cart is created.\) Requires the following:

-   `configurableProductId`
-   `configurationId`
-   `webstoreId`
-   `effectiveAccountId`

**Note:** `webstoreId` and `effectiveAccountId` are part of Salesforce Commerceʼs standard APIs, so that information should be readily available to users.

`configurableProductId` and `configurationId` must correspond to the same configurable product.

PATCH: Use to add items to a specified cart. Requires the following:

-   `configurableProductId`
-   `configurationId`
-   `cartId`

Response: an array of cart item \(CartItem\) records.

Example request \(create new quote\):

```
{
	"configurableProductId": "01t8a0000061GQPAA2",
	"configurationId": "7e45beb9-790c-46ef-a05f-9195718bcda7",
	"effectiveAccountId": "0018a00001nsFoNAAU",
	"webstoreId": "0ZE8a000000XwckGAC"
}
```

Example request \(add to existing quote\):

```
{
	"configurableProductId": "01t8a0000061GQPAA2",
	"configurationId": "7e45beb9-790c-46ef-a05f-9195718bcda7",
	"cartId": "0a68a000000kXQeAAM"
}
```

Example response:

```
[
	{
		"attributes": {
			"type": "CartItem",
			"url": "/services/data/v56.0/sobjects/CartItem/0a98a000000kWtlAAE"
		},
		"CartId": "0a68a000000kXDsAAM",
		"Product2Id": "01t8a0000061GQPAA2",
		"Type": "Product",
		"CartDeliveryGroupId": "0a78a000000kWwxAAE",
		"SalesPrice": 10000.00,
		"UnitAdjustedPrice": 10000.00,
		"TotalLineAmount": 10000.00,
		"TotalPrice": 10000.00,
		"TotalPriceAfterAllAdjustments": 10000.00,
		"LGK__ConfigurationId__c": "7e45beb9-790c-46ef-a05f-9195718bcda7",
		"Name": "LGK Machine",
		"Id": "0a98a000000kWtlAAE"
	},
	{
		"attributes": {
			"type": "CartItem",
			"url": "/services/data/v56.0/sobjects/CartItem/0a98a000000kWtkAAE"
		},
		"CartId": "0a68a000000kXDsAAM",
		"Product2Id": "01t8a0000061GQOAA2",
		"Type": "Product",
		"CartDeliveryGroupId": "0a78a000000kWwxAAE",
		"Quantity": 1.00,
		"SalesPrice": 0.00,
		"UnitAdjustedPrice": 0.00,
		"TotalLineAmount": 0.00,
		"TotalPrice": 0.00,
		"TotalPriceAfterAllAdjustments": 0.00,
		"Name": "Warranty",
		"Id": "0a98a000000kWtkAAE"
	},
	{
		"attributes": {
			"type": "CartItem",
			"url": "/services/data/v56.0/sobjects/CartItem/0a98a000000kWtjAAE"
		},
		"CartId": "0a68a000000kXDsAAM",
		"Product2Id": "01t8a0000061GQKAA2",
		"Type": "Product",
		"CartDeliveryGroupId": "0a78a000000kWwxAAE",
		"Quantity": 1.00,
		"SalesPrice": 0.00,
		"UnitAdjustedPrice": 0.00,
		"TotalLineAmount": 0.00,
		"TotalPrice": 0.00,
		"TotalPriceAfterAllAdjustments": 0.00,
		"Name": "1.5T Magnet",
		"Id": "0a98a000000kWtjAAE"
	},
	{
		"attributes": {
			"type": "CartItem",
			"url": "/services/data/v56.0/sobjects/CartItem/0a98a000000kWtiAAE"
		},
		"CartId": "0a68a000000kXDsAAM",
		"Product2Id": "01t8a0000061GQGAA2",
		"Type": "Product",
		"CartDeliveryGroupId": "0a78a000000kWwxAAE",
		"Quantity": 1.00,
		"SalesPrice": 1.50,
		"UnitAdjustedPrice": 1.50,
		"TotalLineAmount": 1.50,
		"TotalPrice": 1.50,
		"TotalPriceAfterAllAdjustments": 1.50,
		"Name": "MRI Platform Table",
		"Id": "0a98a000000kWtiAAE"
	},
	{
		"attributes": {
			"type": "CartItem",
			"url": "/services/data/v56.0/sobjects/CartItem/0a98a000000kWthAAE"
		},
		"CartId": "0a68a000000kXDsAAM",
		"Product2Id": "01t8a0000061GQLAA2",
		"Type": "Product",
		"CartDeliveryGroupId": "0a78a000000kWwxAAE",
		"Quantity": 1.00,
		"SalesPrice": 2.50,
		"UnitAdjustedPrice": 2.50,
		"TotalLineAmount": 2.50,
		"TotalPrice": 2.50,
		"TotalPriceAfterAllAdjustments": 2.50,
		"Name": "MRI Scanner",
		"Id": "0a98a000000kWthAAE"
	},
	{
		"attributes": {
			"type": "CartItem",
			"url": "/services/data/v56.0/sobjects/CartItem/0a98a000000kWtgAAE"
		},
		"CartId": "0a68a000000kXDsAAM",
		"Product2Id": "01t8a0000061GQRAA2",
		"Type": "Product",
		"CartDeliveryGroupId": "0a78a000000kWwxAAE",
		"Quantity": 25.00,
		"SalesPrice": 1.00,
		"UnitAdjustedPrice": 1.00,
		"TotalLineAmount": 1.00,
		"TotalPrice": 1.00,
		"TotalPriceAfterAllAdjustments": 1.00,
		"Name": "MRI Gradient Coils",
		"Id": "0a98a000000kWtgAAE"
	},
	{
		"attributes": {
			"type": "CartItem",
			"url": "/services/data/v56.0/sobjects/CartItem/0a98a000000kWtfAAE"
		},
		"CartId": "0a68a000000kXDsAAM",
		"Product2Id": "01t8a0000061GQHAA2",
		"Type": "Product",
		"CartDeliveryGroupId": "0a78a000000kWwxAAE",
		"Quantity": 25.00,
		"SalesPrice": 3.00,
		"UnitAdjustedPrice": 3.00,
		"TotalLineAmount": 3.00,
		"TotalPrice": 3.00,
		"TotalPriceAfterAllAdjustments": 3.00,
		"Name": "MRI Radio Frequency Coils",
		"Id": "0a98a000000kWtfAAE"
	}
]

```

**Related topics**  


[CPQ and Salesforce base package overview](logik_io-salesforce_base_package_overview.md)

[Salesforce amendments and CPQ](salesforce_amendments_and_logik_io.md)

[CPQ and Salesforce managed packages](logik_io-salesforce_managed_packages.md)

