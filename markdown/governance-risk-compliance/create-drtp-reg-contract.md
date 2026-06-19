---
title: Create a contract and enhance digital resilience data
description: Create a contract record in Digital resilience third-party registers where you add details of the contract such as vendor name, start and end dates, state, substate, and so on. You can then enhance its digital resilience information for compliance with DORA regulation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/create-drtp-reg-contract.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using Digital resilience third-party registers, Maintaining Digital resilience third-party registers, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create a contract and enhance digital resilience data

Create a contract record in Digital resilience third-party registers where you add details of the contract such as vendor name, start and end dates, state, substate, and so on. You can then enhance its digital resilience information for compliance with DORA regulation.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

The Digital resilience third-party registers include details about who within your organization is using externally outsourced ICT services, which functions and branches are using them, and who the third-party providers and their engagements are. The contracts link these two aspects together.

The contracts link both parties—those using the information and those providing it. Essentially, they bind legal entities, branches, and functions to third parties and third-party engagements.

You can navigate to the contracts from the Contracts menu item in Digital resilience third-party registers. Alternately, you can navigate to the legal entities record, open the Legal entities tab, and navigate to the contracts.

\[Omitted image "leg-ent-record-leg-ent-tab.png"\] Alt text: Legal entity tab.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Digital resilience third-party registers** &gt; **Contracts**.

2.  Select **New**.

    The Create New Contract form is displayed.

3.  On the form, fill in the fields.

    Specific information sub-head is shown in the Create New Contractual arrangement form. The Service provider type field controls which identification fields are displayed \(Third party, Third-party engagement, or Legal entity\).

    For description of the fields on the form, see [Create New Contract form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-contract-form.md).

4.  To submit the contract for review, select **Submit for Review**.

5.  Select **Save**.

6.  Navigate to Entity make using the service related list and select **New**.

    1.  Update the **LEI using service** field.

    2.  Add the branch ID for a branch and update the Function identifiers fields.

    3.  Select **Save**.

7.  To set up the digital resilience information for DORA regulation, navigate to the **Digital resilience information** tab and select **New**.

    The Create New Contractual arrangement form is displayed.

8.  On the form, fill in the fields.

    For more information, see [Create New Contractual arrangement form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-cont-arrange-form.md).

9.  Select **Save**.

    Before saving a contractual arrangement record, the system checks for duplicate records. A duplicate is detected when an existing record matches on the combination of the following 8 key fields:

    1.  Contractual arrangement reference number
    2.  Entity using the service \(LEI\)
    3.  ICT third-party service provider
    4.  Country of provision of the ICT services
    5.  Function identifier
    6.  Type of ICT services
    7.  Storage location
    8.  Processing location
    For the multi-select fields \(Function identifier, Type of ICT services, Storage location, Processing location\), any overlap between the new record and an existing record is treated as a match \(intersection logic, not exact match\). If both records have an empty multi-select field, they are also considered matching.

    If a duplicate is detected, the save is blocked and the following error message is displayed: `A duplicate contractual arrangement (Sys ID: {id}) already exists for this service provider. Check for overlaps in function, service type, or country before saving.`

    **Note:** When you update an existing record without changing the key fields, the duplicate check excludes the current record, so the save is not incorrectly blocked as a self-duplicate.

10. To view contracts for a legal entity, go to the legal entity's record, open the **Legal Entities** tab, and navigate to the Contracts related list.

    The Contracts related list for the legal entity is shown in the example.

    \[Omitted image "leg-ent-record-leg-ent-tab-contact-tab.png"\] Alt text: Contracts tab.\[Omitted image "contracts-tab-leg-ent.png"\] Alt text: Contracts tab.\[Omitted image "contratcs-form-leg-ent.png"\] Alt text: Form.

    This navigation simplifies tracking from the function or legal entity using these third parties.

    1.  In the form, select **More** and navigate to the **Digital resilience information** tab.

        For more information, see [Create New Contractual arrangement form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-cont-arrange-form.md).

    2.  Navigate to the Contract **Details** tab to view the details that are needed by the Digital Operational Resilience Act.

        \[Omitted image "contracts-dig-res-info-tab.png"\] Alt text: Resilience tab.\[Omitted image "contracts-dora-details.png"\] Alt text: Contracts resilience details.

        The information on the form specifies who uses the ICT service. If the entity signing the contract differs from the one using it, that detail goes on the form, along with the service provider. Essentially, the user and the provider are linked together. The following key details are captured:

        -   Data Storage:
            -   Is data stored at APS?
            -   Storage location
        -   Data Processing: Processing location
        -   Data Sensitivity and Resilience:
            -   Data sensitivity level
            -   Reliance on ICT service provider
        -   Contract Details:
            -   Function using the service
            -   Type of services
            -   Contract start and end dates
            -   Termination details \(if applicable\)
                -   Reason for termination
                -   Notice period for both financial entity and third party
        -   Assessments:
            -   Annual assessment mandate for contracts and third parties
            -   Contractual reference number \(links user, provider, etc.\)
        -   Critical Information for Digital Resilience:
            -   Data storage and processing locations
            -   Data sensitivity and service provider reliance
            -   Contract and termination details
            -   Annual assessments and contractual reference number
        -   Termination Clause: Notice period required for termination
            -   Notice period for the financial entity
            -   Notice period for the third party
        -   Contract Specifics:
            -   Function or department using the service
            -   Type of services provided
            -   Contract start date
            -   Contract end date
        -   Termination Information: Reason for termination \(if applicable\)
        -   Additional Context: These details are essential for the contracts and DORA \(Digital Operational Resilience Act\) Register of information perspective.
11. To edit the contract record, select it from the list and select **Edit**.

12. To export the contract record, select **Export**.

13. To delete the contract record, select it from the list and select **Delete**.


-   **[Create New Contract form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-contract-form.md)**  
On the Create New Contract form, fill in the fields.
-   **[Create New Contractual arrangement form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-cont-arrange-form.md)**  
On the Create New Contractual arrangement form, fill in the fields. For each contract, a separate form would be required.

**Parent Topic:**[Using Digital resilience third-party registers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/using-dg-registers.md)

