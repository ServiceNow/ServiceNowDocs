---
title: Onboarding case type
description: Agents can use the onboarding case type to capture the details when onboarding customers for a product or service.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Customer service case types, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Onboarding case type

Agents can use the onboarding case type to capture the details when onboarding customers for a product or service.

The onboarding case type includes a playbook that provides step-by-step guidance through the lifecycle of the onboarding process.

Onboarding cases use the ONB prefix in the case number. For example, ONB0001007. Onboarding cases appear in the Onboarding Cases module in the following lists:

-   My Onboarding Cases
-   All Onboarding Cases
-   Unassigned Onboarding Cases
-   Escalated Onboarding Cases

When creating a case, agents can select **Customer Onboarding** from the list of available case types.

## Creating onboarding cases for new or existing customers

Customer service agents can create cases to onboard new customers or to onboard existing customers for new products.

The onboarding case form includes the **New customer** check box. Agents can enable this check box to display the New Customer Information section on the Case form. This form section includes fields that you can use to collect information and create a customer record.

**Note:** A new customer doesn’t have an existing account, contact, or consumer record.

If an existing case already has the **Account** and **Contact** or **Consumer** fields populated, then the **New customer** check box is turned off.

When saving an onboarding case:

-   If the **New customer** check box is enabled, the **Account** and **Contact** or **Consumer** fields aren't required to save the case.
-   If the **New customer** check box is inactive, the **Account** and **Contact** or **Consumer** fields are required to save the case.

## New Customer Information form section

The New Customer Information form section includes fields that agents can use to collect information. This information is then used to create a customer record. These fields include:

-   Customer Type: either Business or Individual
-   Business Name: Required when the customer type is Business
-   User Name: Required when the customer type is Individual
-   Phone number
-   Email

## Additional members

The onboarding case type includes the **Additional Members** related list on the Case form. Agents can use this related list to create the users or business entities that should be included in the onboarding case.

Additional members can be any of the following:

-   Accounts
-   Contacts
-   Consumers

Agents select information from the following fields when adding a member to an onboarding case:

-   Type: the type of user to be added. For example, a joint owner or a beneficiary or a sub-account.
-   Name: the name of the contact or consumer or account.

**Note:** If using the onboarding playbook, the user is also added to the Member Information card in the Add additional members step of the Initiate stage.

## Onboarding case type stages and states

An onboarding case moves through several stages and states as the agent works to case resolution.

An onboarding case has six stages:

-   Initiate
-   Pre approval
-   Data capture
-   Due diligence
-   Resolve
-   Close

As an onboarding case moves through the stages listed earlier and toward a resolution, the case status is updated. Stage and status are related to each other as described in the following table.

<table id="table_e1t_dct_qlb"><thead><tr><th>

Stage

</th><th>

Status

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Initiate

</td><td>

New

</td><td>

An onboarding case is created in the **Initiate** stage with a status of **New**. An onboarding case can only be in the **New** state during the Initiate stage.

</td></tr><tr><td>

Initiate

</td><td>

Open

</td><td>

The state of an onboarding case state changes to **Open** when the case is assigned to an agent.

</td></tr><tr><td>

Pre approval

</td><td>

-   Open
-   Awaiting Info

</td><td>

In the Pre-Approval stage, an onboarding case can be in either the **Open** or **Awaiting Info** states.The case moves to the **Awaiting Info** state when an agent selects **Request Info**.

</td></tr><tr><td>

Data capture

</td><td>

-   Open
-   Awaiting Info

</td><td>

In the Data Capture stage, an onboarding case can be in either the **Open** or **Awaiting Info** states. The case moves to the **Awaiting Info** state when an agent clicks **Request Info**.

</td></tr><tr><td>

Due diligence

</td><td>

-   Awaiting Info
-   Under Review

</td><td>

In the Due Diligence stage, an onboarding case can be in the **Awaiting Info** or **Under Review** states.The case moves to the **Awaiting Info** state when an agent selects **Request Info**.

 The case moves to the **Under Review** state when an agent selects **Submit for Review**.

</td></tr><tr><td>

Resolve

</td><td>

-   Review Complete
-   Resolved

</td><td>

In the Resolve stage, an onboarding case can be in either the **Review Complete** or **Resolved** states.The case moves to the **Review Complete** state when an agent clicks **Review Complete**.

 The case moves to the **Resolved** state when an agent selects **Propose Solution**.

</td></tr><tr><td>

Close

</td><td>

Closed

</td><td>

The case is closed.

</td></tr></tbody>
</table>