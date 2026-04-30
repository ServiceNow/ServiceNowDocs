---
title: Twinning: pulling Salesforce CPQ quote information into ServiceNow CPQ
description: You can set up Salesforce.com and ServiceNow CPQ to bring quote data into a ServiceNow CPQ configuration at runtime.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 2
breadcrumb: [ServiceNow CPQ integration with Salesforce B2B Commerce, ServiceNow CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# Twinning: pulling Salesforce CPQ quote information into ServiceNow CPQ

You can set up Salesforce.com and ServiceNow CPQ to bring quote data into a ServiceNow CPQ configuration at runtime.

**Note:** This article is relevant only to use cases that are integrated with Salesforce CPQ.

On occasion, the ServiceNow CPQ Admin will need to bring Salesforce.com \(SFDC\) quote data into ServiceNow CPQ, to drive configuration, rules, calculations, and so on. This article describes the setup in both SFDC and ServiceNow CPQ that will bring relevant quote data into a ServiceNow CPQ configuration experience at runtime. This method of data transfer is nicknamed Twin Field or "field twinning."

ServiceNow CPQ rules run differently depending on whether the account is a new prospect or an existing customer. ServiceNow CPQ allows new prospects to select from a subset of offers such as starter packages, whereas existing customers are limited to renewing their existing products or upgrading to higher value products.

## Prerequisites

The ServiceNow CPQ managed package installed in your SFDC environment should be version 0.8 \(released February 4, 2022\) or later. If the managed package has not been upgraded, log an Upgrade SFDC Managed Package Request ticket in the Help Center.

Navigation in SFDC: Setup -&gt; Object Manager -&gt; quote \(SBQQ Quote\_c\) -&gt; Field Sets.

In the SFDC CPQ quote object \(SBQQ\_Quote\_c\), confirm that there is a field set named ReferencedFields. If no field set named ReferencedFields exists, create it. Navigation in SFDC: Setup -&gt; Object Manager -&gt; quote \(SBQQ Quote\_c\) -&gt; Field Sets.

## Implementation

1.  In SFDC, add a custom field to the SFDC CPQ quote object with the format &lt;someName&gt;LGK. This will create a field with the API name &lt;someName&gt;LGK\_c.

    In Logik, variable names begin with a lowercase character by default. Take care to make sure your twinned quote object in SFDC begins with a lowercase character as well.

2.  Add this custom field to the ReferencedFields field set on the quote object. In SFDC, navigate to Setup -&gt; Object Manager -&gt; quote \(SBQQ\_Quote\_c\) -&gt; Field Sets -&gt; ReferencedFields. From the list of quote fields, drag and drop your new custom field into the In the Field Set box.

    ![SFDC CPQ quote object](../images/cpq-salesforce-field-sets.png)

3.  In ServiceNow CPQ, add a field with variable name &lt;someName&gt;.

    **Note:** &lt;someName&gt; should be the same case-sensitive string as the one defined in the SFDC API name of the corresponding field to import, &lt;someName&gt;LGK\_c. This ServiceNow CPQ field should not have LGK suffix. Twinned fields can have different field types.

4.  Associate this field to the Blueprint that will utilize it.

When a user transitions from a SFDC quote into ServiceNow CPQ, the new field in ServiceNow CPQ, &lt;someName&gt;, will be populated with the data that SBQQ Quote\_c. &lt;someName&gt;LGK\_c stored in SFDC.

In Salesforce, the ReferencedFields field set is a custom field set that can be created on the Quote, Quote Line, and Quote Line Group objects. For more information, see [SFDC: ReferencedFields Field Set in Salesforce CPQ](https://help.salesforce.com/s/articleView?id=000382259&type=1).

