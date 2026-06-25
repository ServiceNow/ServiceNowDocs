---
title: Create a supply chain and enhance digital resilience data
description: Create an Information and Communication Technology \(ICT\) service supply chain record in Digital resilience third-party registers using Third-party Risk Management. You can then configure details of the supply chain such as the type of the ICT services, Legal Entity Identifier \(LEI\) of the entity that provides the ICT services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-drtp-reg-supply-chain.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-05-15"
reading_time_minutes: 3
keywords: [DORA, supply chain, ICT services, digital resilience, LEI, Register of Information]
breadcrumb: [Use digital resilience third-party registers, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create a supply chain and enhance digital resilience data

Create an Information and Communication Technology \(ICT\) service supply chain record in Digital resilience third-party registers using Third-party Risk Management. You can then configure details of the supply chain such as the type of the ICT services, Legal Entity Identifier \(LEI\) of the entity that provides the ICT services.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_assessor

## About this task

Rank 1 ICT service supply chain records are generated automatically when you save a Contractual Arrangements – Specific Information record. The Type of ICT services value on the Specific Information record determines which supply chain records are created. If you update that value, the Rank 1 supply chain records update automatically. If you remove a value, the corresponding Rank 1 and higher supply chain records are deleted automatically. Use this task to create Rank 2 and higher supply chain records manually, or to view and edit existing supply chain records. For more information, see [Create a contract and enhance digital resilience data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-drtp-reg-contract.md).

LEI codes on supply chain records are validated against the GLEIF database during Register of Information reporting. For more information, see [Validate Legal Entity Identifier codes for DORA reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-valid-lei.md). To generate a Register of Information package, see [Generate a register of information package](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-drtp-roi-packages.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**, select the list icon \[Omitted image "ws-list-icon.png"\] Alt text: and then navigate to **Digital resilience third-party registers**.

2.  Select **Contracts** and then select the contract record you want to associate a supply chain record with.

3.  Navigate to the ICT service supply chains related list and select **New**.

4.  On the form, fill in the fields.

    For descriptions of all these fields, see [Create New Contractual arrangement form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-create-new-cont-arrange-form.md).

5.  Select **Save**.

6.  To edit the supply chain record, complete the following.

    1.  Navigate to **Supply chains** and select the check box of the record you want from the list.

    2.  Select **Edit** and update the fields as required.

    3.  Select **Update**.

7.  To export supply chain records, complete the following.

    1.  Navigate to **Supply chains** and select the check box of the record you want from the list.

    2.  Select **Export**.

    3.  Select the **File Type**.

        Available choices are:

        -   **Excel**
        -   **CSV**
        -   **JSON**
        -   **PDF**
    4.  Select the **Delivery Type**.

        Available choices are:

        -   **Download**
        -   **Email**

**Related topics**  


[Create a contract and enhance digital resilience data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-drtp-reg-contract.md)

[Generate a register of information package](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-drtp-roi-packages.md)

[Validate Legal Entity Identifier codes for DORA reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-valid-lei.md)

