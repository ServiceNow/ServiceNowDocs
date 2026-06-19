---
title: Configure the filters for feedback or product idea overview page
description: Configure the filters for the feedback or product idea overview page to display information based on the preferences of your users. Use filters to find and engage with feedback and product ideas that are the most relevant to their interests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/product-feedback/configure-feedback-or-idea-overview-page.html
release: zurich
product: Product Feedback
classification: product-feedback
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Feedback, Strategic Planning, Strategic Portfolio Management]
---

# Configure the filters for feedback or product idea overview page

Configure the filters for the feedback or product idea overview page to display information based on the preferences of your users. Use filters to find and engage with feedback and product ideas that are the most relevant to their interests.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System properties** &gt; **All properties**.

2.  Open the **sn\_apw\_advanced.product\_feedback\_product\_idea\_filters** property.

3.  Edit the property by selecting **here**.

4.  In the value field, enter the field name in the query.

    You can add field names in the JSON query. JSON has column objects for each filter. Each column object has two properties:

    -   fieldname: The field name on the feedback or product idea table.
    -   encodedQuery: The filter on the reference table.
    You can only add reference or choice type fields on the feedback or product idea tables as filters. You can either add a new filter or add a condition to the existing filter.

5.  Select **Update**.


**Parent Topic:**[Configuring Feedback application in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/product-feedback/configuring-product-feedback-in-sp.md)

