---
title: Set properties to control pricing processing
description: Activate or deactivate system properties that control how pricing features are processed in Sales Customer Relationship Management applications.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring product pricing, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Set properties to control pricing processing

Activate or deactivate system properties that control how pricing features are processed in Sales Customer Relationship Management applications.

## Before you begin

Role required: admin

## About this task

You can control the following pricing features using pricing system properties:

-   Logging of pricing engine requests for debugging.
-   Method for applying multiple pricing adjustments defined in various pricing matrices.
-   Parallel processing of a large set of pricing engine requests, typically 100 transaction lines or more, to optimize performance. You can also set the threshold, which is the number of transaction lines that triggers parallel processing.

## Procedure

1.  Navigate to **All** &gt; **Pricing** &gt; **Administration** &gt; **Properties**.

2.  Set the following properties:

<table id="table_vn2_m5m_l1c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Logging Pricing Requests\(sn\_csm\_pricing.log\_pricingengine\_request\)

</td><td>

Control the logging of pricing engine requests for debugging. Select **Yes** to activate logging or **No** to turn off the pricing request log.

</td></tr><tr><td>

Method used to stack multiple adjustments defined in matrices\(sn\_csm\_pricing.matrix\_multiple\_adjustments\_handling\)

</td><td>

Control how multiple pricing adjustments from different pricing matrices are applied. Select one of the following:-   Starting List Price: Calculate adjustments based on the list price of the product.
-   Running Total: Calculate current adjustment by applying the adjustment calculations on the previous adjusted value.


</td></tr><tr><td>

Pricing Engine Parallel Execution-   Enable the pricing engine to perform parallel processing of transaction lines when a transaction threshold is met.

\(sn\_csm\_pricing.enable\_pricing\_engine\_parallel\_execution\)

-   Set the number of transactions that must be met before the pricing engine can run parallel processing.

\(sn\_csm\_pricing.pricing\_engine\_parallelism\_lines\_threshold\)

</td><td>

Set properties that optimize the processing time for pricing transactions.-   The parallel execution property is set to **Yes** by default. Select **No** to turn off parallel execution and process the transaction lines serially. If you select **No**, the system ignores the threshold value.
-   The default threshold value is 100. You can enter a different number that represents the minimum number of transaction lines that must be met before the pricing engine can perform parallel processing using multiple threads.
**Note:** Parallel processing isn't performed by the pricing engine for calls to the product configurator pricing integrations, even if the number of transaction lines meets the parallelism threshold.

</td></tr></tbody>
</table>3.  Select **Save**.


