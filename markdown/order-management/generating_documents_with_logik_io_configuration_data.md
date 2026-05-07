---
title: Document generation
description: You can use third-party document generation software to output configuration data by pushing information from CPQ to Salesforce.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using CPQ, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Document generation

You can use third-party document generation software to output configuration data by pushing information from CPQ to Salesforce.

Document generation allows you to create professionally formatted documents using a library of customizable templates. Document generation software directly interfaces with your CRM and associated tools and packages \(such as CPQ and Billing tools\) to output relevant data. For example, you can send a customer a quote document with billing and shipping details, product and pricing information, and so on. These documents can then be submitted to their intended recipient, sometimes with the option for electronic signatures.

## Prerequisites

CPQ does not directly interface with any document generation tools; however, CPQ configuration information can be pushed to Salesforce and used in documents from there. This can be accomplished by enabling **Push Config Data to Logik Salesforce Object** in the Admin Settings if you have not done so already; this will create the Configuration Field Data and Configuration Line Items objects in Salesforce and generate records containing CPQ configuration data.

![Admin settings](../images/cpq-settings-push-config-data-to-SO.png)

## Using the Salesforce CPQ document generator

In order to display CPQ configuration data in out-of-the-box Salesforce CPQ quote documents, you must first map the data from your Configuration Line Itemsʼ extended info to custom fields on their associated quote lines. This can be accomplished by using the configuration line item to quote line” flow that is included with CPQ. For more information, see [Use case: Configuration line item to quote line flow](use-case-configuration-line-item-to-quote-line-flow.md)

Once these fields are populating on your quote lines, they can be [used as line columns](https://help.salesforce.com/s/articleView?id=sf.cpq_line_columns.htm&type=5) to be displayed in your CPQ line items template content. These fields can also be utilized in other [CPQ quote template fields](https://help.salesforce.com/s/articleView?id=sf.cpq_quote_template_fields.htm&type=5), such as the group and subgroup fields, to further customize your quote documents.

## Using a third-party document generator

Third-party document generators include Conga Composer, DocuSign Gen, PDF Butler, and others. Most third-party document generation tools let you use merge fields to pull data directly from any Salesforce object, including the Configuration Field Data and Configuration Line Items objects. This means you can use your document generator's merge fields to display CPQ configuration data in your quote documents directly from those objects instead of mapping all of your data to fields on the Quote Line object. This provides additional layers of flexibility. For example, CPQ configuration data can be displayed in separate tables or used for grouping or organizing your data.

**Parent Topic:**[Using CPQ](cpq-using.md)

