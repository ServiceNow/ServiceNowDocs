---
title: Link knowledge articles or managed documents to an HR catalog item
description: Link knowledge articles or managed documents to an HR catalog item so that employees can refer to the articles or documents when requesting the service through the HR service catalog.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [HR catalog item configuration, HR service catalog management, HR services, HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Link knowledge articles or managed documents to an HR catalog item

Link knowledge articles or managed documents to an HR catalog item so that employees can refer to the articles or documents when requesting the service through the HR service catalog.

## Before you begin

Role required: sn\_hr\_core.admin

For example, an HR catalog item for a beneficiaries inquiry can include links to knowledge articles on who can be named as a beneficiary, the difference between a primary and contingent beneficiary, and so on.

For the link to display on the HR catalog item, make sure the item has a variable that is:

-   **Type** set to **Macro with Label**
-   In the **Type Specifications** related list, with **Widget** set to **HRI Catalog to KB Article Display**

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **HR Services** &gt; **Manage HR Catalog**.

2.  Hover over the HR catalog item that you want to add the knowledge article or managed document to, and click **Manage KB articles**.

    ![Link knowledge articles to an HR catalog item.](../image/link-knowledge-articles-to-hr-catalog-item.png)

3.  Click **New** or open a record to add or edit a link.

4.  Fill in the fields on the form.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the HR catalog item to knowledge article or managed document link.|
    |Catalog Item|This field is automatically set to the HR catalog item.|
    |Knowledge Article|Name of the knowledge article.|
    |Managed Document|Name of the managed document.|
    |Active|Check box to activate the link for use.|
    |Order|Order number for the link. Lowered numbered links are displayed before higher numbered links.|

5.  Click **Submit** or **Update**.

    The knowledge article will display under the **Related Knowledge Documents** section when employees open the HR catalog item in the HR catalog.


**Parent Topic:**[HR catalog item configuration](../concept/hr-catalog-item-configuration.md)

**Previous topic:**[Edit the HR case template for an HR catalog item](edit-hr-case-template-for-hr-catalog-item.md)

**Next topic:**[HR fulfillment instructions](../concept/hr-fulfillment-instructions.md)

