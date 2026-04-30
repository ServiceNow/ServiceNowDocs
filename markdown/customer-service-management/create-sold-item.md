---
title: Create a sold product
description: Create a sold product to track the products or services that are sold to an account or consumer.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Sold products, Configure Install base, Configure product data, Product data, Set up your environment, Configure, Customer Service Management]
---

# Create a sold product

Create a sold product to track the products or services that are sold to an account or consumer.

## Before you begin

Verify that the Customer Service Install Base Management \(com.snc.install\_base\), Customer Service with Service Portfolio Management \(SPM\) \(com.snc.csm\_spm\), and the Product Catalog Management Core \(com.sn\_prd\_pm\) plugins are installed.

Role required: sn\_customerservice\_manager or admin

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Products** &gt; **Sold Products**.

2.  Select **New**.

3.  On the Sold Product form, fill in the fields.

    To learn more about the descriptions, see [Sold product form](../reference/sold-product-form.md).

4.  Select and hold the form header and select **Save**.

    The Child Sold Products, Install Base Items, Cases, Entitlements, Contracts, Additional Contacts, and Additional Consumers related lists are displayed.

5.  Fill in the related lists as required.

<table id="table_zch_sgz_3hb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Child Sold Products

</td><td>

Create a child sold product by selecting **New**.

</td></tr><tr><td>

Install Base Items

</td><td>

Edit an Install base item by selecting **Edit**.

</td></tr><tr><td>

Cases

</td><td>

Add a case to the sold product by selecting **New**. The system displays any open cases that are related to the sold product automatically.

</td></tr><tr><td>

Entitlements

</td><td>

Add an entitlement for the sold product by selecting **Select**. **Note:** Customer service managers create entitlements. Customer service agents can view entitlements.

</td></tr><tr><td>

Contracts

</td><td>

Associate a contract with the sold product by selecting **Edit**.**Note:**

You can also associate a contract with a sold product from the Service Contracts form.

Customer service managers associate the contracts to the sold products. Customer service agents can view the contract information.

</td></tr><tr><td>

Additional Contacts

</td><td>

Add additional contacts to the sold product by selecting **New**.You can associate a contact with a sold product by defining its name and responsibility. The additional contacts added can be from the same account, partner account, or contact relationship.

 You can see the Additional Contacts related list for the sold products that are associated with the B2B account.

 **Note:** Starting with the Utah release, the sn\_install\_base\_rel\_soldproduct\_to\_contact table has been deprecated for new customers.

For upgrade customers, the table continues to be supported and extends the sold product related parties table \[sn\_install\_base\_sold\_product\_related\_party\].

</td></tr><tr><td>

Additional Consumers

</td><td>

Add additional consumers to the sold product by selecting **New**.You can associate a consumer with a sold product by defining its name and responsibility.

 You can see the Additional Consumers related list for the sold products that are associated with the B2C account.

 **Note:** Starting with the Utah release, the sn\_install\_base\_rel\_soldproduct\_to\_contact table has been deprecated for new customers.

For upgrade customers, the table continues to be supported and extends the Sold Product Related Parties table \[sn\_install\_base\_sold\_product\_related\_party\].

</td></tr><tr><td>

Sold Product Related Parties

</td><td>

Add contacts, accounts, and consumers as related parties by selecting **New**.

</td></tr></tbody>
</table>    **Note:** For business-to-business and business-to-consumer, you can see both the additional contacts and additional consumers in the sold product related lists and also add new records.

6.  Select **Update**.

    The sold product is added to the account or consumer that you selected. Select an account or consumer to see a list of all sold products that are related to the account or consumer. You can also view a list of sold products according to the product model.

    **Note:** You can also create sold products directly from an account or a consumer.

    1.  Navigate to **Customer Service** &gt; **Customer** &gt; **Accounts** or **Customer Service** &gt; **Customer** &gt; **Consumer**.
    2.  Select an account or a consumer.
    3.  Select the Sold Products related list.
    4.  Select **New**.

**Related topics**  


[Create and manage sold products for a business location](create-sp-for-business-location.md)

[Edit a contract](edit-contract.md)

[Create an entitlement](create-entitlement.md)

