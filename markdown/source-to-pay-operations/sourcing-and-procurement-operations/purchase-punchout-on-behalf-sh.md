---
title: Purchase punchout items on behalf of another user in Shopping Hub
description: Shoppers can purchase Level 1 \(L1\) and Level 2 \(L2\) punchout items on behalf of another user in Shopping Hub and Employee Center. The punchout supplier site uses that user's credentials and verifies punchout group membership for L1 suppliers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/purchase-punchout-on-behalf-sh.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-08-05"
reading_time_minutes: 6
keywords: [punchout, purchase on behalf, L1 punchout, L2 punchout, super shopper]
breadcrumb: [Shopping Hub, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchase punchout items on behalf of another user in Shopping Hub

Shoppers can purchase Level 1 \(L1\) and Level 2 \(L2\) punchout items on behalf of another user in Shopping Hub and Employee Center. The punchout supplier site uses that user's credentials and verifies punchout group membership for L1 suppliers.

## Key benefits

This functionality extends the existing purchase-on-behalf-of capability \(see [Purchase on behalf of another user in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-on-behalf-sh.md)\) to punchout purchases, and provides the following benefits:

-   A super shopper can select whether they are shopping for themselves or on behalf of another user. This selection occurs before starting an L1 punchout session or before completing checkout for an L2 punchout item.
-   Eligibility for the selected business owner is validated against the punchout groups configured for the punchout supplier before the shopper can proceed. A business owner who isn't eligible for a supplier's punchout catalog cannot be used to complete the purchase.
-   When a business owner is selected, that user's credentials and punchout group membership are used on the punchout supplier site. Any items or orders returned from the punchout site are placed in that user's cart.
-   If no business owner is selected, items are placed in the cart of the shopper who is currently logged in.
-   Purchasing on behalf of another user is supported from multiple locations. These include punchout search results, supplier and product cards, the Browse supplier page, L2 punchout product details, and L1 punchout entry points in Employee Center.

For step-by-step instructions on purchasing L1 and L2 punchout items on behalf of another user, see [Purchase an L1 punchout item on behalf of another user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-l1-punchout-on-behalf.md) and [Purchase an L2 punchout item on behalf of another user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-l2-punchout-on-behalf.md).

## How to configure

Role required: sn\_shop.procurement\_administrator

Plugin required: Shopping Hub \(sn\_spend\_uib\)

Purchasing punchout items on behalf of another user builds on two existing configurations. Ensure both are set up correctly before shoppers use this capability:

-   Configure the ShoppingHub Configuration record for **Purchase on behalf of**. This record determines which shoppers can use the "shop on behalf of" capability and which individuals or groups they can shop on behalf of. This configuration is used for purchasing on behalf of another user for standard supplier products. It also populates the list of users a shopper can select from when purchasing punchout items on behalf of another user. For configuration steps, see [Enable a shopper to purchase on behalf of another user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/config-shoppinghub-purchase-behalf.md).

    \[Omitted image "sh-config-behalf.png"\] Alt text: ShoppingHub Configuration form showing fields for individual shoppers and individuals to be shopped on behalf of.

-   Configure the **Punchout group** field on the Third-Party Registration record for each punchout supplier \(**All** &gt; **Procurement Integrations** &gt; **Setup** &gt; **Third-Party Registration**, then select the supplier\). Select the punchout group. For L1 punchout suppliers, only users who are members of the punchout group can purchase punchout items from that supplier, whether they are shopping for themselves or on behalf of another user. A shopper can select any business owner defined in the "Purchase on behalf" of ShoppingHub Configuration. However, the purchase proceeds only if the selected business owner is a member of the supplier's punchout group. If no business owner is selected, the shopper must be a member of the supplier's punchout group. For configuration steps, see [Configure punchout for third-party site purchases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/configure-supplier-punchout.md).

    **Note:** The punchout group membership requirement applies only to L1 punchout suppliers.

    \[Omitted image "sh-tp-punchout.png"\] Alt text: Third-Party Registration form for a punchout supplier, with the Punchout group field highlighted in the cXML connections related list.

    \[Omitted image "sh-tp-punch-users.png"\] Alt text: Group record named punchout, showing the Group Members tab with three members: Shirley Ross, Alan Edwards, and System Administrator.


## Eligibility validation at purchase time for L1 punchout suppliers

When a shopper selects a business owner, the system checks whether that user is a member of the punchout group configured for the selected supplier's Third-Party Registration record:

-   If the selected business owner is a member of the required punchout group, the shopper is redirected to the punchout supplier site \(L1\).
-   If the selected business owner is not a member of the required punchout group, the redirect or checkout is blocked and a validation message is displayed:

    `Selected user is not eligible for punchout with this supplier.`

    **Note:** The requirement for the target business owner to be a member of the supplier's punchout group applies only to L1 punchout suppliers.

    \[Omitted image "sh-on-behalf-error.png"\] Alt text: Dialog showing error message: Selected user is not eligible for punchout with this supplier.


This eligibility check does not affect punchout search or browse performance, and all shopper-facing messages support localization.

## How it works: L1 punchout

After a shopper selects a punchout product or service from a search results page, a supplier or product card, or the Browse supplier page, a dialog box opens. The dialog box titled **Which user are you shopping for?** appears before the shopper is redirected to the punchout supplier site.

In the dialog box, the shopper selects one of the following options:

-   **Myself** — the shopper's own credentials are used on the punchout supplier site.
-   **On behalf of another user** — the shopper then selects a business owner from the **On behalf of** list.

The shopper selects **Confirm** to proceed to the punchout supplier site, or **Cancel** to close the dialog box without starting a punchout session.

## How it works: L2 punchout

For an L2 punchout item, the shopper selects whether to purchase for themselves or on behalf of another user. This selection occurs when they select **Request to buy** or add the item to their cart. This replaces the separate redirect dialog box used for L1 punchout. If the shopper is purchasing on behalf of another user, they select the business owner from the same "Buy on Behalf of" list. This list is used for L1 punchout and standard supplier purchases.

## After the purchase

After the shopper returns from the punchout supplier site \(L1\) or completes checkout \(L2\), the resulting cart lines and purchase are associated with the selected business owner. As with standard supplier purchases, shoppers can use the filter on **My purchases** to view purchases made on behalf of other users. For more information, see [Purchase on behalf of another user in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-on-behalf-sh.md).

-   **[Purchase an L1 punchout item on behalf of another user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-l1-punchout-on-behalf.md)**  
Purchase items from a Level 1 \(L1\) punchout supplier site on behalf of another user. Select a business owner before the redirect so that items are placed in the correct user's cart.
-   **[Purchase an L2 punchout item on behalf of another user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-l2-punchout-on-behalf.md)**  
Select a business owner when you request to buy or add a Level 2 \(L2\) punchout item to your cart. This validates eligibility and attributes the resulting order to the correct user.

**Parent Topic:**[Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/shopping-hub-overview.md)

