---
title: CPQ and Salesforce managed packages
description: Learn about the Logik Extension Package and the Logik Extension for Salesforce CPQ.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [CPQ integration with Salesforce B2B Commerce, CPQ with other apps, Integrate, Sales and Order Management]
---

# CPQ and Salesforce managed packages

Learn about the Logik Extension Package and the Logik Extension for Salesforce CPQ.

CPQ offers two managed packages for Salesforce\(SFDC\) orgs: the Logik Extension Package and the Logik Extension for Salesforce CPQ. This article discusses what each package does and how they are different. Details on how to set up or upgrade an environment's managed packages are provided at the end of the article.

## Logik Extension Package

This is the base package for CPQ interacting with Salesforce. This package allows the user to:

-   Enable any SFDC Product2 record to be a CPQ configurable product through custom fields added to the Product2 record. For detailed steps, see [Configurable products](configurable-products-explore.md).
-   Launch the CPQ Admin from in Salesforce by navigating to the Salesforce Products tab, select the list view of 'CPQ View', find a CPQ enabled product, and click the corresponding Click Here link located in the View Logik Setup column or through the Product2 record itself by clicking the link in the **View Logik.io Setup** section on the product's page.
-   Support embedding the CPQ UI in Salesforce applications outside of CPQ using Visualforce. See [Use case: Embed CPQ UI in a Salesforce VisualForce page](use_case_embed_logik_io_ui_in_salesforce_visualforce_page.md).
-   Call CPQ admin APIs using Salesforce Tokens. For detailed steps, see [Admin APIs: Authentication using a Salesforce-connected app](admin-apis-authentication-via-salesforce-connected-app.md).

Notable components of this package include:

-   Configuration line item object: This object stores the product data that comes out of a configuration including product id or code, price, BOM type, quantity, and extended information. It also includes the unique configuration ID that ties the data back to a specific configuration session and can be referenced in other flows or triggers in SFDC. Finally, it allows users to populate quote line custom fields with information from CPQ. For additional information, review the following video: [Populate quote line Custom Fields from Logik.mp4](https://drive.google.com/file/d/1aojT9Pv0BceH2fLbUtEDmBmesn40YSto/view?usp=sharing)

    ![Configuration line item](../images/cpq-managed-packages-config-line-item-object.png)

-   Configuration field data object: This object stores the values set to fields in the configuration and contains the unique configuration ID of that session in order to reference that information upon reconfiguration.

    ![Configuration field data object](../images/cpq-managed-packages-config-field-data-object.png)

-   Custom settings to control the end points by setting the Administration URL and Runtime Configuration URL. Navigate to the CPQ Admin custom settings Item:

    ![Menu](../images/cpq-managed-packages-salesforce-logik-admin-custom-settings.png)

    And update these settings here:

    ![Admin settings](../images/cpq-managed-packages-salesforce-logik-urls.png)


## Logik Extension for Salesforce CPQ

In order to install the Logik Extension for Salesforce CPQ. You must have the base package and Salesforce CPQ installed on your org, and at least version 244 or later for your Salesforce CPQ package. This package contains CPQ object specific enhancements over the base package and leverage the CPQ configuration in Salesforce CPQ. This package gives the user the ability to:

-   Launch a CPQ configuration in a CPQ new or amendment quote flow.
-   Populate prior quantity and price in the BOM object for amendment flows.
-   Create child quote lines for the top quote line. Automatically populate the quantity and list price values for each line item based on the information coming from CPQ. This also sets the parent item to be the top line so that the line item appears as a bundle view in the quote.

![Edit quote](../images/cpq-managed-packages-quote-lines.png)

Notable components of this package include:

-   Custom fields added to top level quote line object:
    -   Configuration UD: The universally unique identifier \(UUID\) of the configuration session. Used upon reconfigure to restore configuration to previously determined state.
    -   Committed Configuration UD: When an amendment quote is created. This field is populated with the Configuration ID. During an amendment, when Reconfigure is finished, the Committed Configuration UD is used to populate Prior Quantity and Prior Price columns on the Configuration Line Item object.
    -   BOM Data: Sales line item data serialized in JSON format. Allows for use of data with the quote line calculator or other actions in Salesforce to perform some calculations or custom logic on top of the BOM data coming from a CPQ configuration.

        ![quote line script](../images/cpq-managed-packages-bom-data.png)

        For more information on these objects and the user capabilities they add review the following video: [Delta BOM Feature.mp4](https://drive.google.com/file/d/10Uffs0C7aFWPqkLYRILqZcwgIq2-uxsp/view?usp=sharing)

-   Custom Salesforce REST endpoint that creates a quote and quote lines based on a previously saved configuration, without going through Salesforce CPQ's UI. For more information, review this video: [Request for quote for Omnichannel using Logik APIs.mp4](https://drive.google.com/file/d/1yaPTCzjU12lNLbznqlQ7CxmQskX_YOQ8/view?usp=sharing)
-   [Flightpath](cpq-flightpath.md): allows the administrator to understand how the rules engine responds to end-user inputs by presenting a visual interaction between inputs and triggered rule actions.
-   Configuration Line Item to quote line flow: flow template to populate quote line fields from Configuration Line Item object.

    ![Workflow](../images/cpq-managed-packages-flow-template.png)

    The flow starts inactive and must be enabled.

    Writes Configuration Line Item field to quote line as an example for reference, write the extended info data to the BOM data field. This is where the user would define what fields should be mapped, as well as an optional filter:

    ![Edit update records](../images/cpq-managed-packages-edit-update-records.png)

-   Triggers: Two triggers are included with this package.

    -   Product configurable trigger: This trigger is responsible for setting up configurable products to be configurable. That includes providing the link to CPQ and making the configurable product show up in the CPQ Admin \(on the Configurable Products page\), as well as setting up some product-related data for basic functionality in CPQ quoting.
    -   Amendment quote line trigger: This trigger acts on the custom field Committed Configuration ID. This field gets populated when an amendment quote is created. If the subscription lines originated from a CPQ configuration, this trigger will automatically populate the current Configuration UD to the Committed Configuration UD field. During an amendment, when Reconfigure is finished, the Committed Configuration UD is used to populate Prior Quantity and Prior Price columns on the Configuration Line Item object. The Configuration UD custom field of the amended quote line is updated with new Configuration UD generated during the reconfigure flow. The Configuration UD field on the original subscription is also updated with the new value, so that amendments can be repeated with the latest changes made during the amendment.
    You can disable these triggers through managing the CPQ Admin custom settings referenced above:

    ![Admin settings screen](../images/cpq-managed-packages-salesforce-cpq-settings.png)


## All package components

To view all the components contained in each package, go to Setup, search for "Installed Packages" in the Quick Find box, drill into either package, and click **View Components**. To request an environment setup or upgrade, ensure that a user has been created with the email address of [provisioning@Logik.io](mailto:provisioning@Logik.io), and request the setup or upgrade through our support site or by emailing [support@Logik.io.](mailto:support@Logik.io).

