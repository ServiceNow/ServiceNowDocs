---
title: Sold product form
description: Descriptions of the fields on the sold product form.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Customer Service forms, Reference, Customer Service Management]
---

# Sold product form

Descriptions of the fields on the sold product form.

<table id="table_gmm_hdz_pgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the product or service sold.

</td></tr><tr><td>

Parent Sold Product

</td><td>

Parent of the sold product, if applicable.

</td></tr><tr><td>

Account

</td><td>

Account that is associated with the sold product.**Note:** If you select an account, the **Household**, **Service Organization**, and **Consumer** fields are hidden. The **Consumer** field is active only when the B2B2C plugin is installed.

</td></tr><tr><td>

Billing account

</td><td>

Enables direct reference to the associated Billing Account on the Sold Product entity within ServiceNow® CRM allowing agents to access financial information instantly during service delivery.

</td></tr><tr><td>

Contact

</td><td>

Contact that is primarily responsible for the sold product.**Note:** Only the contacts that belong to the chosen account are shown in the Contact column.

</td></tr><tr><td>

Consumer

</td><td>

Consumer that is associated with the sold product.**Note:** This field is active only when the B2B2C plugin is installed.

</td></tr><tr><td>

Derived price

</td><td>

Attribute that identifies whether the current sold product price is derived from another pricing source.

</td></tr><tr><td>

Product

</td><td>

Product model that the sold product belongs to.

</td></tr><tr><td>

Household

</td><td>

Household to which this sold product belongs to.**Note:** If you select a household, the **Service Organization**, **Account**, and **Contact** fields are hidden.

</td></tr><tr><td>

Service Organization

</td><td>

Internal or external entity that is involved in providing a service to the customer.**Note:** If you select a service organization, the **Household**, **Account**, **Contact**, and **Consumer** fields are hidden. The **Service Organization** field is active only when the service organization plugin is installed.

</td></tr><tr><td>

Service Offering

</td><td>

Service offering that is associated with the sold product. **Note:**

-   The **Service Offering** field may not appear by default in the user interface. If it doesn't appear, add the **Service Offering** field by using the form layout.
-   If the product model already has a service offering that is associated with it, this field is automatically populated.

</td></tr><tr><td>

Product Offering

</td><td>

Product offering that is associated with a sold product. **Note:** The **Product Offering** field appears only to CSM agents, managers, and the contributor persona.

</td></tr><tr><td>

Quantity

</td><td>

Quantity of a product that is sold to a customer.

</td></tr><tr><td>

Unit of measurement

</td><td>

Measurement of entitlements and products that a customer has purchased.**Note:** The **Unit of measurement** field appears only to CSM agents, managers, and the contributor persona.

</td></tr><tr><td>

Offering type

</td><td>

Type of product offer that is associated to a sold product.**Note:** Only the sold products that have an offering type as product appear in the sold product related lists on the Accounts page.

The default value of the field remains as **Product**.

</td></tr><tr><td>

Relationship type

</td><td>

Relationship of a sold product that supports implicit entitlements. **Note:** The default value of the **Relationship** field is **None**.

</td></tr><tr><td>

Product location

</td><td>

The service location of the sold product.

</td></tr><tr><td>

Start and end dates

</td><td>

The existing Add order to Sold product to create Sold product state is changed to **In Preparation** if the start date &gt;current date. If `current_date >= start_date` and `current_date <= end_date` then the state is changed to **Active**. If `current_date > end_date` then the state is changed to **Expired**.

</td></tr><tr><td>

Product specification

</td><td>

The product specification associated with a sold product.**Note:** The **Product specification** field is available only if you have the Product Catalog Management Core \(com.sn\_prd\_pm\) plugin and is not available on the form by default.

</td></tr><tr><td>

Provider service organization

</td><td>

The service organization that sells and supports the products or services owned by the customer.

</td></tr><tr><td colspan="2">

**Note:** New fields are added to enhance the traceability for subscription-based products. Add columns to the Sold Product base table and use the **Split from** and **Split from Root** fields to track lineage during upsells, downsells, and expiration date changes ensuring accurate order management, compliance, and analytics.

</td></tr></tbody>
</table><table id="table_zjm_kqp_ydc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Term \(months\)

</td><td>

Validity of a product or service in terms of number of months.

</td></tr><tr><td>

Subscription start date

</td><td>

Start date of access to a product or service.

</td></tr><tr><td>

Subscription end date

</td><td>

End date of access to a product or service.

</td></tr><tr><td>

Price list

</td><td>

Price list used to derive prices while purchasing a product or service.

</td></tr><tr><td>

Unit net price

</td><td>

Net price of a single unit of a sold product.

</td></tr><tr><td>

Pricing method

</td><td>

Pricing method associated to a sold product, whether recurring or one-time.

</td></tr><tr><td>

Periodicity

</td><td>

Frequency of the pricing method, whether it’s weekly, monthly, annually, and so on.**Note:** You can set periodicity only if the pricing method is recurring.

</td></tr><tr><td>

One time price

</td><td>

One-time price to be paid for the usage of a product or service.

</td></tr><tr><td>

Monthly recurring price

</td><td>

Price to be paid on a monthly basis for the usage of a product or service.

</td></tr><tr><td>

Annual recurring price

</td><td>

Price to be paid on a yearly basis for the usage of a product or service.

</td></tr><tr><td>

Cumulative one time price

</td><td>

One-time price to be paid for the parent line and all the child line items.

</td></tr><tr><td>

Cumulative monthly recurring price

</td><td>

Price to be paid on a monthly basis for the parent line and all child line items.

</td></tr><tr><td>

Cumulative annual recurring price

</td><td>

Price to be paid on a yearly basis for the parent line and all child line items.

</td></tr><tr><td>

Cumulative net price

</td><td>

Total value of the sum of cumulative one-time net price and cumulative monthly recurring price multiplied by term.Cumulative net price = Cumulative one time price +Cumulative monthly recurring price \* Term

</td></tr><tr><td>

Unit base price

</td><td>

Allow users to capture the base price of the specific sold product.

</td></tr><tr><td>

Sales agreement line

</td><td>

Allow users to capture the sales agreement directly when creating a sold product.

</td></tr><tr><td>

Unit list price

</td><td>

Allow users to capture the list price of the specific sold product.

</td></tr></tbody>
</table>