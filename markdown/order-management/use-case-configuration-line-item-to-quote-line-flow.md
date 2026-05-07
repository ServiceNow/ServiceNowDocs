---
title: Use case: Configuration line item to quote line flow
description: By making a few adjustments to a flow template includes with the CPQ Extension package version 1.8 or later, you can parse the extended information from a configuration and map it to custom fields without using a QCP script.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use cases, Using CPQ, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Use case: Configuration line item to quote line flow

By making a few adjustments to a flow template includes with the CPQ Extension package version 1.8 or later, you can parse the extended information from a configuration and map it to custom fields without using a QCP script.

**Note:** This article applies to the CPQ Extension for Salesforce CPQ package version 1.8 or later. If your CPQ CPQ package is version 1.7 or earlier, see [Use case: Using the Salesforce Quote Calculator plugin to integrate data from CPQ to Salesforce quotes and quote lines](integrate_config_data_from_productlist_extended_to_salesforce_quote_and_quote_lines_using_quote_calculator_pluginqcp.md).

By default, if you add any extended info to a line item \(using ProductList.extended\), it will be added as a JSON to the corresponding configuration line item object created as the following:

![configuration line item objects](../images/cpq-config-to-quote-line-flow-1.png)

Before this flow was created, the only way to parse the individual keys and map them to custom fields on the configuration line items or their corresponding Quote Lines was to write a QCP script to do so. This guide will show you how to achieve the same result by making a few adjustments to a flow template included with our CPQ Extension package starting versions 1.8 or later.

Letʼs take the case of the first custom field in the screenshot above. A product is added using an advanced product rule and the freight information is entered as extended info, for this example we will be using SG\_Freight so adjust as necessary for your extended info name:

```
ProductList.extended = {};
ProductList.extended.SG_Freight = cfg.sRFreight;  
```

You must create a `SG_Freight_c` field on the configuration line item and Quote Line objects \(if you just enter “SG\_Freight,” SFDC will automatically add the \_c\). It is recommended to do so with the Schema Builder since itʼs much faster. If you do choose to add them through the Object Manager, make sure to check the Field Accessibility settings for the created fields so that the flows are able to modify them. Be sure to set the field-level security on the custom field to be visible for any profile that will be using them.

Next, in SFDC, go to Setup &gt; Process Automation &gt; Flows. Look for the “Configuration Line Item to Quote Line” flow and click it. It should look like this:

![Workflow](../images/cpq-config-to-quote-line-flow-2.png)

Select the Update Fields flow element and click `Edit Element`. This will open a popup window:

![Edit update records](../images/cpq-config-to-quote-line-flow-3.png)

Click **+ Add Field**, and then in the Field column, enter the SFDC field name as below \(autocomplete should help you type it in\):

![Set filter condition](../images/cpq-config-to-quote-line-flow-4.png)

If the data is entered correctly, you should see the value for the created field change to the same format as the value above it:

![Set filter conditions](../images/cpq-config-to-quote-line-flow-5.png)

Save the flow and activate. Itʼs recommended to save the flow as a a new flow instead of as a new version, so that youʼll always have the original template to go back to if needed.

Add your fields to the configuration line item and quote line layouts in order to see these values where they belong:

![list](../images/cpq-config-to-quote-line-flow-6.png)

![Quote line screen](../images/cpq-config-to-quote-line-flow-7.png)

**Parent Topic:**[Use cases](use-cases.md)

