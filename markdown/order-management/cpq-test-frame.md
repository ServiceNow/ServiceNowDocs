---
title: The test frame
description: Use a test frame to quickly validate the behavior of a configurator without creating a web page or running the full quoting flow. This lightweight test page lets you load a product and pass key parameters to preview the configuration in an iframe, either from on-page inputs or directly from URL parameters.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# The test frame

Use a test frame to quickly validate the behavior of a configurator without creating a web page or running the full quoting flow. This lightweight test page lets you load a product and pass key parameters to preview the configuration in an iframe, either from on-page inputs or directly from URL parameters.

The test frame streamlines testing by providing a lightweight interface to preview configuration behavior before deploying changes.

## Accessing the test frame

To access the test frame page in CPQ, navigate to the appropriate URL, replacing `{tenant}` and `{sector}` with values for your instance:

```
https://{tenant}.{sector}.logik/ui/configure/testFrame.html
```

Typically, the value of `{sector}` is `test` for sandbox or `prod` for production.

**Note:** If the test frame page displays CPQ administration, clear your browser cache.

## Using the test frame

The testFrame HTML provides easy inputs to a variety of parameters that can be sent to the CPQ configurator.

![Test frame](../images/cpq-test-frame.png)

1.  Product ID: Product ID of the configurable product to load
2.  Pricebook ID: Salesforce Pricebook ID
3.  Reconfigure ID: Logik UUID of existing configuration to load for reconfiguration
4.  Quote Line ID: Salesforce Quote Line ID
5.  Layout: Name of the Layout to load from the Blueprint of the Configurable Product
6.  Runtime Token: Runtime Token from Logik Admin Setup
7.  Runtime Client API: Needs to be encoded and URL-safe. Highly recommended if using the Runtime Token parameter
8.  Config Editability: Control the ability to save a configuration
    -   Active: Displays the Quote button on the configuration page
    -   Available: Displays the Save button on the configuration page
    -   None: No Save or Quote button is displayed. End user cannot save configuration
9.  Flightpath: Determines whether the execution of CPQ Rules is logged
    -   Active: Displays Flightpath controls and automatically starts recording
    -   Available: Displays Flightpath controls and does not start recording
    -   None: No Flightpath controls are displayed
10. Use URL Parameters: if checked, use parameters from the URL instead of values in inputs.
11. Update Configuration: On click, this will send the parameters to the CPQ Configuration iframe and update.
    -   If using the HTML inputs, parameters are passed via easyXDM
    -   If Use URL Parameters is checked, the src of the iframe will be set using the URL parameters

## test frame page

![Example for test frame](../images/cpq-test-frame-example.png)

-   URL to access the test frame page
-   Parameter inputs
-   Configuration iframe

For more information, see [Use case: Embed CPQ UI in an HTML page](use_case_embed_logik_io_ui_in_an_html_page.md).

