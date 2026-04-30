---
title: Contracts
description: A contract defines the terms and conditions along with pricing agreed for a product with the supplier​. An active contractual price determines if the pricing of a product or service is displayed on Shopping Hub.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Sourcing and Purchasing Automation, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Contracts

A contract defines the terms and conditions along with pricing agreed for a product with the supplier​. An active contractual price determines if the pricing of a product or service is displayed on Shopping Hub.

Use the purchasing view to view contract details in the Sourcing and Purchasing Automation module. You can also create a new contract with the contract\_manager role.

In addition to purchase requisitions, systematic creation of a contract occurs during a sourcing request or negotiation. This is configured accordingly in flow designer. The various scenarios for pre-purchase contract creation are:

-   Negotiation exists, created manually: Trigger contract creation, including NDA if required, against the negotiation when the state of the negotiation is Planned.
-   Negotiation exists, created systematically through third-party sourcing integration: Trigger contract creation, including NDA if required, against the negotiation when the state of the negotiation is Negotiation in Progress.
-   Negotiation does not exist: Trigger NDA contract creation, if required, against the sourcing request when the state of the sourcing request is Awaiting Supplier Response. A procurement specialist or contract team can manually create other contracts against the sourcing request before creating a purchase requisition. If contracts are not manually created against the sourcing request, they are systematically created against the awarded purchase requisition after approvals are complete.
-   New supplier created from manual sourcing or third-party sourcing integration: For third-party sourcing integration, trigger contract creation when a new purchase line is created for a new supplier. For manual sourcing, contract creation follows the manual negotiation creation or negotiation does not exist scenarios.

When a supplier is awarded, contracts that were created for the other suppliers are canceled, except NDAs. Contract metadata population remain as is.

In a contract, the following are the key fields:

<table id="table_wlb_5bb_hlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contract model

</td><td>

Type of the contract.

</td></tr><tr><td>

Supplier

</td><td>

Supplier that is billed for this contract.

</td></tr><tr><td>

Contract number

</td><td>

Unique identifier for the contract that the vendor assigns.

</td></tr><tr><td>

Name

</td><td>

Short description of the contract.

</td></tr><tr><td>

Parent contract

</td><td>

Parent contract or agreement, if any.

</td></tr><tr><td>

Start date

</td><td>

Date from which this contract is effective.

</td></tr><tr><td>

End date

</td><td>

Date on which the contract ceases to be effective.

</td></tr><tr><td>

State

</td><td>

Status of the contract. For example, **Draft**, **Active**, **Expired**, or **Canceled**.

</td></tr><tr><td>

Substate

</td><td>

Substate of the contract. For example, **Awaiting Review**, **Under Review**, **Approved**, or **Rejected**.

</td></tr><tr><td>

License quantity entitled

</td><td>

Number of licenses included in the contract. This field is available for Maintenance and Software License contracts.

</td></tr><tr><td>

Contract administrator

</td><td>

Person responsible for managing the contract and interacting with the vendor.

</td></tr><tr><td>

Approver

</td><td>

User who approves or rejects the contract.

</td></tr><tr><td>

Business owner

</td><td>

Internal user responsible for the product in the contract.

</td></tr><tr><td>

Agreement type

</td><td>

License classification of the contract.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the contract.

</td></tr><tr><td class="sub-head" colspan="2">

Purchasing

</td></tr><tr><td>

Purchasing entity

</td><td>

The purchasing entity associated with the contract.

</td></tr><tr><td>

Payment term

</td><td>

The agreed to time and conditions under which a payment to a supplier is made.

</td></tr><tr><td>

Incoterm

</td><td>

Determines who assumes the liability and when a fixed asset must be capitalized.

</td></tr><tr><td class="sub-head" colspan="2">

Financial

</td></tr><tr><td>

Invoice payment terms

</td><td>

Terms that explain how to pay the contract. For example, **Net Monthly Account** or **Net 30**.

</td></tr><tr><td>

Payment schedule

</td><td>

Schedule that defines when to make payments. For example, **Monthly** or **Annually**.

</td></tr><tr><td>

Payment amount

</td><td>

Amount paid for this contract so far.

</td></tr><tr><td>

Applicable taxes

</td><td>

Tax applicable for this contract. Select from **Exempt** or **Sales**.

</td></tr><tr><td>

Effective tax rate

</td><td>

Tax rate applicable to the total cost.This field is visible only if the applicable taxes is selected as **Sales**.

</td></tr><tr><td>

Tax cost

</td><td>

Total tax on the contract.This field is visible only if the applicable taxes is selected as **Sales**.

</td></tr><tr><td>

Total cost

</td><td>

Final cost of the contract after adjustments have been applied. If a contract has one or more rate cards, this field shows the combined value of all rate cards.

</td></tr><tr><td>

Vendor account

</td><td>

Account of the vendor with which the contract is associated.

</td></tr><tr><td>

PO Number

</td><td>

Purchase order associated with this contract.

</td></tr><tr><td>

Cost center

</td><td>

Cost center that is financially responsible for the asset.

</td></tr><tr><td>

Has rate card

</td><td>

Determines if the contract has an associated rate card.

</td></tr><tr><td class="sub-head" colspan="2">

Renewal

</td></tr><tr><td>

Automatically renew

</td><td>

Indicates if the contract can be renewed at the end of its term.

</td></tr><tr><td>

Options

</td><td>

Duration of the contract renewal or extension. For example, 1 year.

</td></tr><tr><td>

Renewal start date

</td><td>

Date on which the contract renewal or extension takes effect.

</td></tr><tr><td>

Renewal end date

</td><td>

Date on which the contract renewal or extension ends.

</td></tr><tr><td>

Cost adjustment type

</td><td>

Type of cost adjustment applied to the contract: **Fixed**, **Manual**, or **CPI** \(consumer price index\).

</td></tr><tr><td>

Cost adjustment amount

</td><td>

Numerical increase or decrease in price of contract. To indicate a decrease in price, enter a negative number. Either a **Cost adjustment** or **Cost adjustment percentage** can be specified, but not both.

</td></tr><tr><td>

Cost adjustment percentage

</td><td>

Percentage increase or decrease in price of contract. To indicate a decrease in price, enter a negative percentage. Either a **Cost adjustment** or **Cost adjustment percentage** can be specified, but not both.

</td></tr><tr><td class="sub-head" colspan="2">

Terms and conditions

</td></tr><tr><td colspan="2">

Specific legal information in the contract.

</td></tr></tbody>
</table>The following are the related lists of a contract:

|Related list|Description|
|------------|-----------|
|Child Contracts|Lists any child contracts that exist for this contract.|
|Expense Lines|Lists all expense lines for this contract.|
|Assets Covered|Lists all assets covered by this contract.|
|CIs Covered|Lists all configuration items \(CI\) used in this contract.|
|Service Offerings|Lists all service offerings from this vendor. Activate Service Portfolio Management to see this related list.|
|Approval History|Lists all approvals for this contract.|
|Contract History|Displays the changes to the start and end dates of this contract and changes to the terms and conditions.|
|Purchase Requisitions|Lists all the purchase requisitions associated with this contract.|
|Purchase Orders|Lists all the purchase orders associated with this contract.|
|Supplier Products Covered|Lists all the supplier products covered under this contract.|
|Pre-payments|Provides information of the pre-payment details such as the amount and the payment date for this contract.|

## Contract exception rules

Contract exception rules specify conditions in which a contract record is not created even if there is a corresponding contract type mapped to a model category. A procurement administrator​ can configure these rules from decision tables which are in the administration section of the Sourcing and Purchasing Automation module.

**Parent Topic:**[Sourcing and Purchasing Automation](purchase-experience-workflow.md)

