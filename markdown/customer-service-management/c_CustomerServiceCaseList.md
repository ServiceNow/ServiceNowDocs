---
title: Customer Service Cases list
description: The Cases list displays a list of customer service cases for the current user.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Customer Service Management]
---

# Customer Service Cases list

The Cases list displays a list of customer service cases for the current user.

Users with the sn\_customerservice\_agent or sn\_customerservice\_manager roles can view the Cases list in the Customer Service Management application. The default view of the Cases list includes the following columns:

-   **Number**
-   **Short description**
-   **Contact**
-   **Account**
-   **Channel**
-   **State**
-   **Priority**
-   **Assigned to**
-   **Updated**
-   **Case Report** \(add a column to access this table if needed\)

External customers can view a list of cases from the customer portal. For external users with the sn\_customerservice.customer or sn\_customerservice.customer\_admin roles, the Cases list displays a subset of case information, including:

-   **Number**
-   **Short description**
-   **Product**
-   **Priority**
-   **State**
-   **Updated**

For external users with the sn\_customerservice.partner or sn\_customerservice.partner\_admin roles, the **Account** column is also displayed.

## Cases displayed in the Case list by user role

The cases included in the Case list are determined by user role.

<table id="table_iqr_zfr_ns"><thead><tr><th>

User Role

</th><th>

Cases Included in Case List

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Internal roles

</td></tr><tr><td>

sn\_customerservice.customer\_admin

</td><td>

All cases

</td></tr><tr><td>

sn\_customerservice\_manager

</td><td>

All cases

</td></tr><tr><td>

sn\_customerservice\_agent

</td><td>

All cases

</td></tr><tr><td class="sub-head" colspan="2">

External roles

</td></tr><tr><td>

sn\_customerservice.customer\_admin

</td><td>

-   Cases created for the customer administrator's account
-   Cases created by contacts who have a contact relationship with the customer administrator's account

 **Note:** A [contact relationship](c_ContactRelationships.md) enables a contact with the customer role or customer admin role to manage the account for which the contact relationship has been established.

</td></tr><tr><td>

sn\_customerservice.customer

</td><td>

-   Cases created by the customer
-   Cases created by an agent for the customer

</td></tr><tr><td>

sn\_customerservice.partner\_admin

</td><td>

-   Cases created by the partner:
    -   For their own account
    -   For a customer account
-   Cases created for the partner administrator's account

</td></tr><tr><td>

sn\_customerservice.partner

</td><td>

-   Cases created by the partner
-   Cases created by an agent for the partner
-   Cases created for the same account
-   Cases created from a partner account

</td></tr></tbody>
</table>