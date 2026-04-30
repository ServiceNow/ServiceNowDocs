---
title: Monitor service charges in the service pricing console
description: As a service owner use the service pricing console to generate service charge lines, view the service charge lines, and set pricing policy. Setting the pricing policy generates the rate card, which captures the set price, surcharge or discount details.
locale: en-US
release: yokohama
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 4
breadcrumb: [Service charging - Legacy, Financial Charging - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Monitor service charges in the service pricing console

As a service owner use the service pricing console to generate service charge lines, view the service charge lines, and set pricing policy. Setting the pricing policy generates the rate card, which captures the set price, surcharge or discount details.

## Before you begin

Role required: service\_charging\_owner

**Important:**

This feature is available only when you own an ITBM Analyst license.

## Procedure

1.  Navigate to **All** &gt; **Financial Charging** &gt; **Service Charging** &gt; **Console**.

    Open the console to monitor all the details related to the statement items in the following panes:

    My Statement Items: A list of all the statement items owned by the service owner appear on the left pane.

2.  Click the statement item on the left pane, the details of which you want to view.

3.  Click the **Fiscal Period** choice list to select a fiscal period.

4.  Click **Generate Lines** to generate charge lines for the statement item for the specified fiscal period.

    The Generate Charge Lines pop-up opens up.

    **Note:**

    You can view the list of service charge lines generated based on the statement item by navigating to **Financial Charging** &gt; **Service Charging** &gt; **Service Charge Lines**. These service charge lines are records that you can monitor on the console.

5.  Update the fiscal period for the period that you want to generate the charge lines.

6.  Click **Generate**.

    A message appears confirming that the Charge lines generation job has been scheduled successfully.

    The statement item details pane on the right displays all the details of the statement item.

    Overview tab:

    -   Pricing, cost, and charges: The left pane displays the details of the pricing policy method and the pricing policy adopted for the statement item. It also shows the total cost of the statement item and the total charges that has been charged for the statement item.
        -   **Costs** are the actual expenses by service. It is the amount that you incur in buying a product or a service.
        -   **Price** is the amount that is determined for a product or a service based on cost factors involved in production, marketing, selling, and so on.
        -   **Charge** is the amount of money you are charged by the business service for the services or goods they provided.
    -   **Cost trend**: The spline chart shows the trend of the cost against the price over the different fiscal periods.
    -   **Charge lines**: The service charge lines are generated for statement item. Each service charge line lists the name of the product or the service used and the associated unit cost of the item computed with the quantity, giving you the total cost.

<table id="table_ibq_fts_tz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the statement item.

</td></tr><tr><td>

Average unit cost

</td><td>

Average cost of one unit of the statement item.

</td></tr><tr><td>

Quantity

</td><td>

Number of items at the statement item and at the statement item breakdown level.

</td></tr><tr><td>

Total cost

</td><td>

Unit Cost \* Quantity.

</td></tr><tr><td>

Price Adjustment \(%\)

</td><td>

Price adjustment is based on the pricing policy method that you defined in the statement item definition form.Adjust the price either on percentage or unit price by incrementing or decrementing a percentage of the Average Unit Cost. The adjusted price reflects as the Total Charges.

</td></tr><tr><td>

Unit Price

</td><td>

Sets a predefined unit rate for a service. It is determined for a quantity of service that is delivered or the cost of a single statement item.

</td></tr><tr><td>

Total Charges

</td><td>

Total amount of money charged for each business service, which is the adjusted price of the average unit cost.

</td></tr></tbody>
</table>7.  Click **Set Pricing Policy** button.

    You can see more details of the statement item in the right pane of the console that opens up.

8.  Click the statement item level or the statement item line level price adjustment box \(based on the pricing policy that you have set\) to adjust the price and arrive at the total charges.

9.  Click **Set Price**.

    The price adjustment that you made reflects in the **Total Charges** field.

10. Click the Drilldown tab to view the drilldown details of the statement items at the drilldown entity level.

    You can view the statement item breakdown or compare it with the other charge line item breakdowns to get better visibility on cost by breakdown.

    Drilldown tab:

    -   **Drilldown**: Click **Drilldown** field to view the detailed data of statement item’s cost by breakdown for each drilldown entity on a chart.
    -   **Charge line item Breakdown**: Click **Charge line item Breakdown** field to view the charge line item breakdown by cost for each statement item breakdown.
    -   **Charge line item Breakdown accounts**: Click **Charge line item Breakdown accounts** field to view the accounts for each service charge line of the statement item breakdown.

## What to do next

The charges that you define are attached as a rate card to a statement item. As a service charging analyst and service charging owner, you can also [define service charge price rate cards.](create-ratecards-for-business-service.md)

**Parent Topic:**[Service charging - Legacy](../concept/service-charging.md)

