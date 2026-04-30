---
title: Use case: Modifying layout text with SLDS styles
description: Learn how to implement styles in the Salesforce Lightning Design System to control the appearance of text.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 1
breadcrumb: [Use cases, Using ServiceNow CPQ, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Use case: Modifying layout text with SLDS styles

Learn how to implement styles in the Salesforce Lightning Design System to control the appearance of text.

Using Salesforce Lightning Design System \(SLDS\) styles, admins have some control over the appearance of text in the ServiceNow CPQ configurator UI. Note that this functionality is not fully supported and may be limited in a number of scenarios. Consult [this Salesforce documentation](https://www.lightningdesignsystem.com/utilities/text/) for the available SLDS styles.

Due to the lack of complete support, utilizing an SLDS class will affect everything in the field. That means if you use “slds- text-title\_bold”, everything in the field will be bolded. Therefore, consider whether you can use SLDS styling for your use case, as a new field will need to be created for us to insert the class and isolate the styling. A good use case as a result is using styles to make headers, and weʼll use that as the basis for this article.

If we want to make a header using SLDS, the first step is to identify which field\(s\) you want a header for, and make sure theyʼre displayed in the layout. Then, from the layout screen, navigate to the field and remove its label. This will leave you with just the fieldʼs variable name.

![Graphics card](../images/cpq-layout-field-label-removed.png)

Next, create a new text field and give it some text. This new field will be placed above the existing field and essentially act as its “header”. Place it in the layout and remove its label. Your layout should resemble this example.

**Note:** Instead of creating a new field, you can also just add text directly to the layout. In the image below, you would click the down arrow to create the text. However, unlike when using fields, you wouldnʼt be able to conditionally hide the text.

![graphics card](../images/cpq-layout-field-new-no-label.png)

Finally, in the layout, hover over the new field you created that will act as the header, and click the gear to bring up the Field Properties. For Class Name, add the desired SLDS class. In this example, we have used `slds-text-heading_large`.

![Fieldproperties](../images/cpq-layout-field-properties.png)

Redeploy your blueprint and youʼre done. Open an applicable product in the configurator to see the result.

![Graphics card](../images/cpq-layout-custom-headings.png)

**Parent Topic:**[Use cases](use-cases.md)

