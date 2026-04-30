---
title: Configuring ServiceNow CPQ for SalesForce RLM
description: Install and configure the Salesforce Revenue Lifecycle Management package for ServiceNow CPQ \(v0.3 or later\).
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 13
breadcrumb: [ServiceNow CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# Configuring ServiceNow CPQ for SalesForce RLM

Install and configure the Salesforce Revenue Lifecycle Management package for ServiceNow CPQ \(v0.3 or later\).

## Prerequisites

This guide assumes the following:

Salesforce \(SF\) environment:

-   Your Salesforce environment has Revenue Lifecycle Management \(RLM\) license\(s\) provisioned.
-   The setup steps described in [Salesforce RLM documentation](https://help.salesforce.com/s/articleView?id=sf.revenue_lifecycle_management_get_started.htm&type=5) are complete:
    -   Enable RLM features in your SF org
    -   [Enable Product Configurator](https://help.salesforce.com/s/articleView?id=ind.product_configurator_enable_product_configurator.htm&type=5)
    -   Set up your user permissions set licenses and permission set groups for Admin user

Note that Salesforce Development states that its RLM and CPQ apps are incompatible. Therefore, follow these steps:

-   Uninstall the CPQ app, if it is installed.
-   Uninstall any Salesforce CPQ for ServiceNow CPQ package that may be installed on the Salesforce environment.
-   If the ServiceNow CPQ environment previously had a Salesforce Subscription Management for ServiceNow CPQ package installed on it, this must be uninstalled. Some Subscription Management package elements conflict with the elements installed by the Salesforce Revenue Lifecycle Management for ServiceNow CPQ package.

ServiceNow CPQ base package: Salesforce for Logik Base package v2.2, or greater installed.

## Set up ServiceNow CPQ Configuration for SalesForce RLM

This guide walks you through the installation and setup of the Salesforce Revenue Lifecycle Management package for ServiceNow CPQ v0.3 or later. \(This guide does not discuss NGP setup. It will be added in a later version.\)

As the current package is unmanaged, you will be required to uninstall v0.3 to install future releases of this package.

## Salesforce Product Catalog Management \(PCM\) → Setup Configurable Product Bundle

1.  App Launcher → Price Books: Activate "Standard Price Book"
2.  App Launcher → Product Selling Models: Create a new Product Selling Model \(PSM\)
    -   PSM Name: "One Time"
    -   Selling Model Type: "One Time"
    -   Status: "Active"

        ![Product selling model screen](../images/cpq-product-selling-model-details.png)

3.  Setup → Object Manager → Price Book Entry → Page Layouts → "Price Book Entry Layout": Add "Product Selling Model" field to the layout
4.  Setup → Object Manager → Product → Page Layouts → "Product Layout": Add the following fields to the layout
    -   Configure During Sale - makes the product configurable or not
    -   Based On - associates a product to a class
    -   Display URL - used for product images
    -   Product Type
    -   Tax Policy
5.  Add the following related lists to the Product Layout
    -   Product Selling Model Options
    -   Overridden Inherited Attributes
    -   Child Components
    -   Inherited Attributes
    -   Product Component Group
6.  App Launcher → Product Catalog Management → Product Classification: Create a new Product Classification
    -   Name: “Server Racks”
    -   Code: “RACK”
    -   Status: Active
7.  App Launcher → Product Catalog Management → Products: Create a new Product

    -   Product Name: “Product Warranty - 1 Year”
    -   Active: true
    -   Product Code: “WARRANTY”
    -   Configure During Sale: “Not Allowed”
    -   Product Type: “— None —"
    -   Description: “Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.”
    On the related list of the product, add a new Product Selling Model Option named "One Time."

    Click "Add Price Book Entry" in the Price Books related list, and use the following options:

    -   Product Selling Model: "One time"
    -   List Price: 2000
    -   Active: True
    -   Price Book: Standard Price Book
8.  App Launcher → Product Catalog Management → Products: Create another new Product

    -   Name: “Server Rack”
    -   Active: True
    -   Product Code: “RACK“
    -   Configure During Sale: “Allowed”
    -   Based On: “Server Racks”
    -   Product Type: “Bundle”
    -   Display URL: https://someimage.jpg
    -   Product Description: “Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.”
    On the related list of the product, add a new Product Selling Model Option named "One Time."

    Click "Add Price Book Entry" in the Price Books related list, and use the following options:

    -   Product Selling Model: "One time"
    -   List Price: 150000
    -   Active: True
    -   Price Book: Standard Price Book
    On the related list of the product, create a new Product Componnent Group with the following options:

    -   Product Component Group Name: “Warranties”
    -   Code: “WARRANTY”
    -   Sequence: 0
    -   Min Bundle Components: 0
    -   Max Bundle Components: 2
    -   Description: “Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.”
    On the related list of the "Server Rack" product, click "Add" on the Child Components related list, and add "Product Warranty - 1 Year" as a child component with the following options:

    -   Sequence: 0
    -   Quantity: 1
    -   Group: “Warranties”
    -   Allow quantity changes: true
    -   Price includes component: false
    -   Include component by default: true
    -   Min Quantity: 1
    -   Max Quantity: 3
    -   Product Relationship Type: "Bundle to Bundle Component Relationship"
    Notes:

    -   You need to search this and type it - the dropdown is not automatic.
    -   After manually opening the Bundle-to-Bundle Component Relationship record from App Launcher → Product Relationship Types, the record appears in this menu:

        App Launcher → Product Relationship Types → Bundle to Bundle Component Relationship.

        If you donʼt see it, you must manually create it by navigating to App Launcher → Product Relationship Types → New, and setting the following options:

        -   Product Relationship Type Name: “Bundle to Bundle Component Relationship”
        -   Associated Product Role Category: “Bundle Component”
        -   Main Product Role Category: “Bundle Parent”
9.  Create a new Attribute Category \(App Launcher → Product Catalog Management → Attribute Categories\) with the following options:
    -   Name: “Server Rack Specifications”
    -   Code: “SPEC”
    -   Description: “Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
10. Create a new Attribute Definition \(App Launcher → Product Catalog Management → Attributes\) with the following options:
    -   Name: “Load Capacity”
    -   Label: “Load Capacity”
    -   API Name: “LoadCapacity”
    -   Data Type: “Number”
    -   Default Value: 1500
    -   Active: true
    -   Code: “CAP”
    -   Description: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam."
11. Return to the related list of the new "Server Rack Specifications" attribute category you created, and in its related list, under "Attributes", click "Assign" and add the "Load Capacity" attribute to it.
12. App Launcher → Product Catalog Management → Product Classifications → "Server Racks" → "Attributes" tab: Click "Assign" → "Assign individual attributes" → add the "Load Capacity" attribute.

    ![Load capacity screen](../images/cpq-logik-config-for-sf-rlm-38.png)

    ![Service rack specification](../images/cpq-logik-config-for-sf-rlm-39.png)

    ![Server racks](../images/cpq-logik-config-for-sf-rlm-40.png)

    ![Price book entry](../images/cpq-logik-config-for-sf-rlm-41.png)


## Salesforce Transaction Line Editor Setup

A Lightning Web Component is available to perform configure/reconfigure and view the Quote Line Items in their bundled/hierarchical view. To add this component to the layout:

1.  App Launcher → Sales → Quotes → open a quote.
2.  Press the gear icon on the top-right corner of the page and select "Edit Page".

    ![Salesforce Transaction Line Editor Setup](../images/cpq-edit-page.png)

3.  From left menu, drag Transaction Line Editor component onto the layout.

    ![Transaction components](../images/cpq-transaction-line-editor.png)

4.  Save and Activate.

## Salesforce Product Configuration Flows Setup

Instead of assigning a Configurator at the org level, a new object determines which configurator to launch per product.

1.  Search for and open the sObject, "Product Configuration Flow"
2.  Create a new Config Flow record and set the Flow Identifier as "RLMConfiguratorScreen". If you're only using one configurator, make this the Default as well.

If there are multiple config flows being used, the flow can be assigned to individual products or product classifications through the Related records.

![SMC configuration](../images/cpq-product-configuration-flows.png)

## Salesforce Product Discovery Setup

Configure from Quote: With Product Discovery, products can be configured before being added as a quote line.

1.  App Launcher → Sales → Quotes → open a quote.
2.  Press the gear icon on the top-right corner of the page and select "Edit Object".
3.  Go to Page Layouts; for the layouts being used, add the “Browse Catalog” action to the layout and save.

![Setup menu](../images/cpq-edit-object.png)

Configure from account is not currently supported. In the future, the user will be able to configure without reference to a quote. For instance, this could be used to launch product discovery from the account page.

1.  From a Catalog page, open the Admin gears and click “Edit Page”.
2.  Under Components, search for and add the "Product List Page Component" onto the page.

    ![Product list components](../images/cpq-logik-config-for-sf-rlm-46.png)

3.  Save, and if needed, Activate and assign as default.

## ServiceNow CPQ Webhook Setup

1.  If Webhooks are not enabled on your ServiceNow CPQ environment, create a Support case and request Webhooks be turned on in the environment.
2.  When Webhooks are enabled, navigate to ServiceNow CPQ Admin Home → Utilities → Webhooks, and create a new Webhook with the following settings:

    -   Integration Type: Salesforce
    -   Async: false
    -   Content: Either "All" or "BOM and System Fields"
    -   BOM Types: "sales" \(others can optionally be added, but "sales" is required\)
    ![Webhook screen](../images/cpq-webhook-setup.png)


## ServiceNow CPQ Product Selling Models Setup

In a product action, pricing fields for Revenue Lifecycle Management can be set, similar to extended info. These are available in both simple and advanced product actions.

Example of simple product action setup:

![Product selling models setup](../images/cpq-product-selling-models-setup.png)

Available pricing map \(ProductList.pricing\) fields are:

-   productSellingModelId
-   startDate
-   endDate

Assuming Product Selling Models have been created in Salesforce, the productSellingModelId can be found in a subpage of Utilities and will automatically be suggested in the simple product action UI.

Example productSellingModelId based on this image would be "Term\_Defined\_TermDefined\_1\_Months\_2023\_03\_02"

![Product Selling models](../images/cpq-product-selling-models-setup-example.png)

## Salesforce: Enable Context Service

1.  Setup → Feature Settings → Context Service → Context Service Settings: Set “Context Definitions” to "On"
2.  Refresh the page. If you donʼt see the next step, wait 10 seconds and try again.

    If you still donʼt see the next step, wait 20 seconds and try again. This is an asynchronous process.

3.  Setup → Feature Settings → Context Service → Context Definitions: Confirm that under “Standard Definitions”, the “Sales Transaction Context” is present and is “Active”.
    1.  Open dropdown menu for "SalesTransactionContext\_\_stdctx" and press 'Extend'.
    2.  Populate the new Context Definition and Save.
    3.  Go to the Custom Definitions tab. Open the dropdown menu for the newly created Context Definition and press 'Activate'.

![Context definitions](../images/cpq-enable-context-service.png)

## Salesforce: Enable Business Rules Engine \(BRE\) for Qualification

1.  Setup → Feature Settings → Business Rules Engine → Business Rules Engine Settings: Toggle on the switch to enable “Industries Cloud Common Decision Tables Access”
2.  Setup → Context Service → Context Definition: Create a new custom context definition named “BrowseContextdefinition” \(this name must match exactly\). Don't set any other fields.
3.  Click “Next”
4.  Add the following context nodes:
    -   Name: “PriceBook”
    -   Name: “Account”
    -   Name: “Catalog”
5.  Under “Catalog”, add a child node of ”Category“
6.  Under “Category”, add child nodes of “CategoryProduct” and “PricingProduct”
7.  Under “CategoryProduct” add a child node of “Message”, and click Next.
8.  Under “PriceBook”, click “Add Attributes” and add the PricebookID attribute:
    -   AttributeName: “PricebookId”
    -   Type: “INPUT”
    -   Data Type: “STRING”
9.  Under “Account”, click “Add Attributes” and add attributes with the following AttributeNames, a type of INPUT, and a data type of STRING:
    -   Id
    -   contactId
    -   AccountCity\_\_c
    -   SLA\_\_c
    -   CurrencyIsoCode
    -   Region\_\_c
10. Under “Catalog”, click “Add Attributes” and add attributes with the following AttributeNames, a type of INPUT, and a data type of STRING:
    -   Id
    -   CurrentDate
11. Under “Category”, click “Add Attributes” and add the following attributes with a data type of STRING and the type as specified:
    -   CategoryId \(Type: INPUT\)
    -   IsCategoryQualified \(Type: OUTPUT\)
    -   CategoryDisqualifiedReason \(Type: OUTPUT\)
12. Under "CategoryProduct", click "Add Attributes" and add attributes with the following AttributeNames, a type of INPUT, and a data type of STRING, unless otherwise specified:
    -   Id
    -   ProductId
    -   RootProductId
    -   ParentProductId
    -   CategoryId
    -   CatalogId
    -   Name
    -   Code
    -   MaxQuantity \(Data Type: NUMBER\)
    -   MinQuantity \(Data Type: NUMBER\)
    -   Quantity \(Data Type: NUMBER\)
    -   IsQualified \(Type: OUTPUT; Data Type: NUMBER\)
    -   Reason \(Type: Output: Data Type: STRING\)
13. Under "Message", click "Add Attributes" and add the following attributes with a type of OUTPUT and a data type of STRING:
    -   Name
    -   Value
14. Under "PricingProduct", click "Add Attributes" and add the following attributes:
    -   PricingId
        -   Type: INPUT
        -   Data Type: STRING
    -   PricingProductId
        -   Type: INPUT
        -   Data Type: STRING
    -   ProductSellingModelId
        -   Type: INPUT
        -   Data Type: STRING
    -   ProductQuantity
        -   Type: INPUT
        -   Data Type: NUMBER
    -   UnitPrice
        -   Type: OUTPUT
        -   Data Type: CURRENCY
    -   NetUnitPrice
        -   Type: OUTPUT
        -   Data Type: CURRENCY
    -   PriceWaterFall
        -   Type: OUTPUT
        -   Data Type: STRING
    -   PricingErrorMessage
        -   Type: OUTPUT
        -   Data Type: STRING
15. Click Next.
16. For each of the following nodes, add node tags that exactly match the name of the node:
    -   PriceBook
    -   Account
    -   Catalog
    -   Category
    -   CategoryProduct
    -   PricingProduct
17. For each of the following attributes, add the specified attribute tags:
    -   \(For PriceBook:\) PriceBookId: PriceBookId
    -   For Account:
        -   AccountCity\_c: AccountCity
        -   SLA\_c: SLA
        -   CurrencyIsoCode: CurrencyCode
    -   \(For Catalog:\) CurrentDate: CurrentDate
    -   For Category, give each attribute a tag that exactly matches the name:
        -   CategoryId
        -   IsCategoryQualified
        -   CategoryDisqualifiedReason
    -   For CategoryProduct, give each attribute a tag that exactly matches the name:
        -   ProductId
        -   RootProductId
        -   ParentProductId
        -   IsQualified
        -   Reason
    -   For PricingProduct, give each attribute a tag that exactly matches the name:

        -   PricingProductId
        -   ProductSellingModeId
        -   ProductQuantity
        -   PricingId
        -   UnitPrice
        -   NetUnitPrice
        -   PricingErrorMessage
        For PriceWaterFall, assign a tag of price\_water\_fall. Click Save.

18. Open your newly created "BrowseContextDefinition" → click "Map Data" tab → click "Add Mapping":
    -   Mapping Name: "BrowseOperation"
    -   Description: "Browse Operation"
    -   Mapping Type \(select both\):
        -   "Automatic Input Schema Mapping"
        -   "Automatic sObject Mapping"
    -   Mark as Default: TRUE
19. Setup → Context Service → Context Definitions: in "BrowseContextDefinition" menu, click "Activate"
20. App Launcher → Business Rules Engine → Lookup Tables: Click “New” and select “Decision Table”

    -   Name: “ProductQualificationDT”
    -   Description: “Qualification Rules decision table”
    -   API Name: “ProductQualificationDT”
    -   Source Object: “Product Qualification”
    -   Filter Result By: “Any Value”
    -   Usage Type: “Product Qualification”
    On the next screen, because weʼre going for the simplest qualification rule, we have only a single input and output \(i.e. “Given a Product ID, tell me if its qualified or not”\)

21. Next to “ProductId” set “Donʼt Use” to “Optional input”
22. Next to “IsQualified” set “Donʼt Use” to “Output”
23. Click “Next” and “Save"
24. Click the “Activate” button in the upper right corner to activate the decision table
25. App Launcher → Business Rules Engine → Expression Sets: Click "New" to create a new Expression Set
    -   Name: “QualificationProcedure”
    -   Usage Type: “Product Qualification"
    -   Context Definition: “BrowseContextdefinition”
26. In the newly created expression set record home, see the “Expression Set Versions” table and click the first row to launch the Expression Set Builder.
27. In the expression set builder, click the “+” button in the middle of the screen and select “Evaluate Qualification”
    -   Lookup Table Details: “ProductQualificationDT”
    -   ProductId: “ProductId”
    -   IsQualified: “IsQualified”
    -   Reason: “Reason”
28. In the sidebar in the expression set builder, click the cog icon and set the “Rank” equal to 1
29. Click the Element Details tab and select “Include in Output”
30. Click “Save As”, wait for the full-page refresh, and then click “Activate”

    At this point, your BRE Qualification Rules should be setup correctly. To end, we will simulate the configuration to verify that it is working correctly.

31. In the Expression Set Editor, click the “Simulate button”
32. Select “Advanced” for the input and populate the ProductId field with your Cisco Server Rack NX44 product ID

    Leave the IsQualified and Reason fields as empty strings.

33. Click “Simulate”

Inspect the Output JSON to see if your product returns. "IsQualified" will be "null" and "Reason" will be an empty string.

## Salesforce: Pricing Procedure

1.  App Launcher → search for and open "Pricing Procedures" → open the "Revenue Management Default Pricing Procedure" → open the active Pricing Procedure and deactivate it.
2.  Return to the Revenue Management Default Pricing Procedure. Edit it.

    Change the Context Definition to the custom definition that was extended from "SalesTransactionContext\_\_stdctx". Save.

3.  Reactivate the Pricing Procedure Version.

## Troubleshooting

Issue: The ServiceNow CPQ blueprint was loaded into the RLM org, but no products show in the product catalog during quoting.

Diagnosis: This could mean that there's an issue with the Product Discovery settings \(see the [Salesforce: Enable Context Service](https://docs.google.com/document/d/10MqNVlW4X5ikoLvYTH3NeBhQO7mDq6rUUt3bsP428Ig/edit#heading%3Dh.t6hdyrii25c4) section and beyond\).

-   Setup → Feature Settings → Decision Tables. Open both the ProductQualification and Price Book Entries tables and perform the 'Refresh' action on each.
-   If the refresh doesn't solved the problem, view the following Salesforce documentation:
    -   [RLM Product](https://help.salesforce.com/s/articleView?id=sf.qocal_product_discovery_setup.htm&type=5)
    -   [Discovery Setup](https://help.salesforce.com/s/articleView?id=sf.qocal_product_discovery_setup.htm&type=5)

Issue: At runtime, the user receives the following error in RLM: `System.IllegalArgumentException: Looks like you don't have access to the place quote service. Salesforce Customer Support can help with that`

Diagnosis: This is a permission set issue. Make sure that the following three RLM permission sets are assigned to the integration user that facilitates the ServiceNow CPQ integration.

-   Product Catalog Management Designer
-   ProductAndPriceConfiguration API
-   Product Catalog Management Viewer

