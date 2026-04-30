---
title: Create a contract
description: Create a contract with various contract models, which would act as a binding agreement between the two parties.
locale: en-US
release: zurich
product: Contract Management
classification: contract-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Contracts, Contract Management use, Contract Management, IT Asset Management]
---

# Create a contract

Create a contract with various contract models, which would act as a binding agreement between the two parties.

## Before you begin

Role required:

-   For Core UI and Hardware Asset Workspace: admin, contract\_manager
-   For Enterprise Asset Workspace: sn\_eam.enterprise\_admin, sn\_eam.enterprise\_asset\_manager
-   For Software Asset Workspace: sam\_admin, sam\_user

## About this task

If a contract has one or more associated rate cards, the fields on the Contract form can’t be edited.

## Procedure

1.  Open the list of contracts that are used across your deployment.

    -   If you’re using the Core UI, navigate to **All** &gt; **Contract** and select a contract type, such as **Insurance**, **Maintenance**, or **Service**, or select **All**.
    -   If you’re using Hardware Asset Workspace, navigate to the **Contract management** view and then select the **All contracts** tab.
    -   If you’re using Enterprise Asset Workspace, open the **Contract and lease management** view and then select the **All contracts** tab.
    -   If you’re using Software Asset Workspace, navigate to **License operations** &gt; **Contracts** &gt; **Software contracts** and select **New**.
2.  Select **New**.

3.  On the form, fill in the fields.

    Not all fields appear on all contract type forms.

<table id="table_xqw_rb1_hxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contract model

</td><td>

Model the contract is assigned to. For example **Lease**, **Maintenance**, **Warranty**, **Service Contract** **Software License**, or **Subscription**.

</td></tr><tr><td>

Vendor

</td><td>

Vendor responsible for the contract. This field is required when **Purchase Agreement** or **NDA** is selected from **Contract model**.

</td></tr><tr><td>

Contract number

</td><td>

Number assigned to the contract by the vendor \(required\).

</td></tr><tr><td>

Name

</td><td>

Name of the contract.

</td></tr><tr><td>

Parent contract

</td><td>

Parent contract of the new contract, if applicable. You can select a parent contract from the contract lookup list.

</td></tr><tr><td>

Start date

</td><td>

Date on which the contract takes effect. This field is required when **Purchase Agreement** or **NDA** is selected from **Contract model**.

</td></tr><tr><td>

End date

</td><td>

Date on which the contract expires. Leave the end date empty to create an open-ended contract. This field is required when **Purchase Agreement** or **NDA** is selected from **Contract model**.

</td></tr><tr><td>

State

</td><td>

Current state of the contract.-   Draft
-   Active
-   Expired
-   Canceled


</td></tr><tr><td>

Substate

</td><td>

Current substate of the contract.-   Awaiting Review
-   Under Review
-   Approved
-   Rejected


</td></tr><tr><td>

Contract administrator

</td><td>

Person responsible for managing the contract and interacting with the vendor.

</td></tr><tr><td>

Approver

</td><td>

User who approves or rejects the contract. This list is filtered to only show users with the itil role.

</td></tr><tr><td>

Business owner

</td><td>

User who manages the contract from a business perspective.

</td></tr><tr><td>

Agreement type

</td><td>

Agreement type of license:-   Enterprise
-   SaaS
-   Subscription
This field appears only when **Maintenance** and **Software License** is selected from **Contract model**.

</td></tr><tr><td>

Commitment

</td><td>

Amount committed to spend with this vendor during this time period, from the start to the end of the contract. This field appears only when **Purchase Agreement** is selected from **Contract model**.

</td></tr><tr><td>

Discount

</td><td>

Discount the vendor has agreed to provide.This field appears only when **Purchase Agreement** is selected from **Contract model**.

</td></tr><tr><td>

Process non-contractual SLAs

</td><td>

Option to process both contractual and non-contractual Service Level Agreements \(SLAs\). This field appears only when **Service Contract** is selected from **Contract model**.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the contract.

</td></tr><tr><td class="sub-head" colspan="2">

Financial section

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

Amount that has been paid on the contract to date.

</td></tr><tr><td>

Applicable taxes

</td><td>

Indicates if the contract is exempt from taxes or subject to sales tax.

</td></tr><tr><td>

Effective tax rate

</td><td>

Effective tax rate to apply to the total cost, if applicable. Effective tax rate is usually the average tax rate charged.

 This field appears only when **Sales** is selected from **Applicable taxes**.

</td></tr><tr><td>

Tax cost

</td><td>

Total cost of the tax.

 This field appears only when **Sales** is selected from **Applicable taxes**.

</td></tr><tr><td>

Total cost

</td><td>

Final cost of the contract after adjustments have been applied. If a contract has one or more rate cards, this field shows the combined value of all rate cards.

 This field appears only when **Sales** is selected from **Applicable taxes**.

</td></tr><tr><td>

Vendor account

</td><td>

Vendor account associated with the contract.

</td></tr><tr><td>

PO Number

</td><td>

Purchase order number assigned to the contract.

</td></tr><tr><td>

Cost center

</td><td>

Cost center that is financially responsible for the asset.

</td></tr><tr><td>

Has rate card

</td><td>

Check box to indicate whether the contract has an associated rate card.

</td></tr><tr><td class="sub-head" colspan="2">

Renewal section

</td></tr><tr><td>

Automatically renew

</td><td>

Indicates if the contract can be renewed or extended at the end of its term.

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

Type of cost adjustment applied to the contract.-   Fixed
-   Manual
-   CPI \(Consumer Price Index\)


</td></tr><tr><td>

Cost adjustment amount

</td><td>

Numerical increase or decrease in price of contract. To indicate a decrease in price, enter a negative number. Either a **Cost adjustment** or **Cost adjustment percentage** can be specified, but not both.

</td></tr><tr><td>

Cost adjustment percentage

</td><td>

Percentage increase or decrease in price of contract. To indicate a decrease in price, enter a negative percentage. Either a **Cost adjustment** or **Cost adjustment percentage** can be specified, but not both.

</td></tr><tr><td class="sub-head" colspan="2">

Terms and Conditions section

</td></tr><tr><td>

Terms and conditions

</td><td>

Specific legal information in the contract.

</td></tr></tbody>
</table>4.  Save the form.

    -   If you’re using Core UI, right-click the form header and select **Save**.
    -   If you’re using Hardware Asset Workspace, Software Asset Workspace, or Enterprise Asset Workspace, select **Save**.
5.  Continue entering information in the related lists or tabs that appear.

<table id="table_uwp_l2l_gs"><thead><tr><th>

Related list or tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assets Covered

</td><td>

Lists all assets covered by this contract.

</td></tr><tr><td>

Users Covered

</td><td>

Lists all users covered by this contract.

</td></tr><tr><td>

Contract used by

</td><td>

Lists all configuration items \(CI\) used in this contract.

</td></tr><tr><td>

Terms and Conditions

</td><td>

Lists all terms and conditions of this contract.

</td></tr><tr><td>

Expense Lines

</td><td>

Lists all expense lines in this contract.

</td></tr><tr><td>

Contract History

</td><td>

Displays the changes to the start and end dates of this contract and changes to the terms and conditions.

</td></tr><tr><td>

Approval History

</td><td>

Lists all approvals for this contract.

</td></tr><tr><td>

Service Offerings

</td><td>

Lists all service offerings from this vendor.

 Activate Service Portfolio Management to see this related list.

</td></tr><tr><td>

Service Commitments for Contracts

</td><td>

Lists all service commitments for this vendor's offerings.

 Activate Service Portfolio Management to see this related list.

</td></tr></tbody>
</table>6.  Perform one of the following actions.

    -   Select **Update** to save and exit the contract.
    -   Select **Submit for Review** to send a notification to the approver.

-   **[Create a software maintenance contract example](t_UseCaseCreateSWMaintContract.md)**  
One common use case for the Contract Management application is creating a contract to track maintenance payments for enterprise software. You can use this example to learn how to create a software maintenance contract.
-   **[Add an asset to a contract](t_AddAnAssetToAContract.md)**  
You can associate contracts with specific assets, including software licenses.
-   **[Add a user to a contract](t_AddAUserToAContract.md)**  
A contract can cover specific users. For example, you may use a contract to hire a group of temporary workers.
-   **[Add a configuration item to a contract](t_AddAConfigurationItemToAContract.md)**  
Contracts can be associated with configuration items. You can link a contract with configuration items to clarify what the contract legally covers.
-   **[Add a document to a contract](t_AddADocumentToAContract.md)**  
Contracts can be associated with documents. Linking a contract to related documents helps keep all relevant information about a contract together and easily accessible.

**Parent Topic:**[Contracts](../concept/c_Contracts.md)

**Related topics**  


[Adjust a contract](t_AdjustAContract.md)

[Verify contract administrator assignment for notification](t_SendAContractNotification.md)

[Send the contract for approval](t_SendTheContractForApproval.md)

[Terms and conditions](../concept/c_TermsAndConditions.md)

[Create a contract rate card](t_ContractRateCardsAndExpenseLines.md)

[Monitor a contract](t_MonitoringContracts.md)

[Models](../../product-catalog/concept/c_Models.md)

[Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-landing-page&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)

[Add a commitment to a service offering](https://www.servicenow.com/docs/access?context=define-SPM2-service-commitments&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)

[Contract renewal workflow](../concept/cont-renew-wf.md)

[Contracts](../concept/c_Contracts.md)

