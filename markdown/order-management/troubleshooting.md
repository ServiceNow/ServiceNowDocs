---
title: Troubleshooting
description: Steps to take if you encounter problems using CPQ.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [CPQ, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Troubleshooting

Steps to take if you encounter problems using CPQ.

## Error messages

-   An error occurred. Please contact your administrator.

    ![Error message](../images/cpq-error-generic.png)

    This generic error message appears for every error logged when configuring. This usually points to an edge case that was not previously considered when building the Blueprint and can be rectified by looking into the results of the [Logs](https://logikio.atlassian.net/wiki/spaces/CS/pages/2022735879) tab in CPQ Admin when this error occurs. A more detailed response will usually be present that should point your administrator to the location of the error, such as a rule, enrichment, or an external connection.

    ![Logs](../images/cpq-logs.png)

    If there is no further detail located in the Admin log, or if you are still confused by the messaging of the error, please log a support ticket.

-   Cannot get Configurable Product. Product &lt;Salesforce Product2 Id&gt; is not available in cache.

    The CPQ user that was added when your environment was being set up in your Salesforce org may have been deactivated, causing an issue with the Refresh Token Username and Refresh Token.


## Admin

The Products tab is not visible in Admin view.

The Products Admin page is only shown when CPQ is set up to support a headless use case. In this scenario, CPQ provides its own product master.

In a Salesforce-integrated use case, the CPQ environment is integrated with a Salesforce \[SFDC\] environment. In a headless or eCommerce use case, CPQ is accessed from a resource other than SFDC, such as an eCommerce platform, partner portal, or a non-SFDC CPQ application. In this scenario, the CPQ environment is frequently accessed via APIs only, with the calling resource digesting the results and displaying them in its own user interface.

When a CPQ environment is not integrated with Salesforce, this is commonly called a 'headless' or 'ecommerce' use case. The Products Admin page only displays to CPQ administrators when the environment is set up for this headless mode.

As a point of contrast, when the CPQ environment is integrated with SFDC, the SFDC product2 object is the part master. CPQ administration intentionally does not show a Products administration page when integrated with SFDC.

## APIs

-   The Salesforce Authentication call is returning a Status: 400 Bad Request

    Inspect the permissions of this OAuth App, as defined in Salesforce, by navigating to App Manager in Salesforce Setup. For your connected app, select "Manage" from the drop-down menu on the right, and then click **Review OAuth Policies**. The **IP Relaxation** setting may be set to **Enforce IP restrictions**. Set this to **Relax IP restrictions**.

-   When using the JWT to authenticate the administration API call, you get a 302 Found error with no body.

    Make sure that you insert the string, "Bearer" before the JWT access\_token text in the Authorization value.


## Configuration

For some user profiles, configuring results in a white screen or reconfiguring does not load any of the previously chosen options. In order to properly configure or reconfigure, users need access to certain objects and fields in Salesforce. These can be assigned using permission sets or by going to Setup &gt; Profiles &gt; Select Desired Profile &gt; Object Settings.![Profiles screen](../images/cpq-profiles-object-settings.png)

Users will need read/edit access in the Field Permissions section to the following objects:

Configuration Attributes:

-   Id
-   Name
-   Target Field
-   Product
-   Raw Order
-   Column Order
-   Position

Product features:

-   Id
-   Name
-   Option Selection Method
-   Configured SKU
-   Number
-   Min Options

For products \(Product2\):

-   Configuration Type
-   Has Configuration Attributes
-   Externally Configurable

For quote lines:

-   Configuration Id
-   BOM Data
-   Product
-   Incomplete
-   Dynamic Option ID
-   Quantity
-   List Unit Price
-   Option Level

For product options:

-   Read/Edit access in Object Permissions
-   Configuration Id
-   BOM Data

And if using Amendments, users also need the following:

Quote lines:

-   Committed Configuration Id
-   Action context
-   Upgraded subscription
-   Source

Subscriptions \(SBQQ\_\_Subscription\_\_c\):

-   Configuration Id
-   BOM Data

See [Granting user access in CPQ](granting_user_access_in_logik_io.md).

## Salesforce integration

-   Products in CPQ do not create quote lines in Salesforce CPQ

    When using CPQ with Salesforce CPQ, certain configuration requirements must be met in order for your products to get added to CPQ as quote lines. Here are the most common causes for products not creating quote lines in CPQ.

    -   The Product Id in CPQ is not equal to the Product Code field on the product record in Salesforce.

        This is contingent upon the “Product Id Field” tenant setting in the Admin. You can use either Product Code \(Product2.ProductCode\), Partner Id \(Product2.Id\), or External Id \(Product2.ExternalId\).

    -   The product record is not active in Salesforce.
    -   No pricebook entry has been assigned to the product record.
    -   The pricebook entry for the pricebook is different from the pricebook on the quote. The pricebook entry for the product is inactive.
    If you have confirmed none of these are true and a quote line is still not being created, then it is probable that the product sync that takes place between CPQ and Salesforce via the refresh token user has not occurred yet. This sync occurs via API every 30 minutes for test and demo environments and every 15 minutes for production. To determine when this sync last occurred, enter Salesforce and navigate to Setup → Bulk Data Load Jobs.

-   
**Parent Topic:**[CPQ reference](../reference/servicenow-cpq-reference.md)

