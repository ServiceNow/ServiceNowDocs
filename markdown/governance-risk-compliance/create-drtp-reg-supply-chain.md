---
title: Create a supply chain and enhance digital resilience data
description: Create an Information and Communication Technology \(ICT\) service supply chain record in Digital resilience third-party registers. Add details of the supply chain such as type of the ICT services, Legal Entity Identifier \(LEI\) of the entity that provides the ICT services, and so on. You can then enhance its digital resilience information for compliance with DORA regulation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/create-drtp-reg-supply-chain.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Digital resilience third-party registers, Maintaining Digital resilience third-party registers, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create a supply chain and enhance digital resilience data

Create an Information and Communication Technology \(ICT\) service supply chain record in Digital resilience third-party registers. Add details of the supply chain such as type of the ICT services, Legal Entity Identifier \(LEI\) of the entity that provides the ICT services, and so on. You can then enhance its digital resilience information for compliance with DORA regulation.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

Before saving an ICT service supply chain record, the system checks for duplicates. A duplicate is detected when an existing supply chain row at the same rank shares the same Identification code of the recipient of sub-contracted ICT services and the same Type of ICT services. If a duplicate is detected, the save is blocked and an error message identifies the conflicting record. Update either the recipient identification code, the type of ICT services, or the rank to resolve the conflict.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Digital resilience third-party registers** &gt; **Contracts** and select the desired contract.

2.  In the **ICT service supply chains** tab on the Contract form, select **New**.

    The Create New ICT service supply chain form is displayed.

    The example shows the ICT service supply chains tab on a contract record listing existing supply chain entries.

    \[Omitted image "contract-ict-service-supply-chains-tab.png"\] Alt text: ICT service supply chains tab on a contract record listing existing supply chain entries.

    Each row is a supply chain with its rank, type of ICT services, recipient identification code, service provider type and identification code of the ICT third-party service provider.

3.  On the form, fill in the fields.

    For more information, see [Create New ICT service supply chain form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-supply-chain-form.md).

4.  Select **Save**.

5.  To set up the digital resilience information for DORA regulation, navigate to the **Digital resilience information** tab and select **New**.

6.  On the form, fill in the fields.

7.  Select **Save**.

    The Identification code of the recipient of sub-contracted ICT services field is automatically kept in sync with the linked ICT third-party service provider's identification code. If you update the provider's identification code, the supply chain records at all ranks are updated automatically to show the current code value.

    Cascading delete and cascading update apply to all ranks \(Rank 1 and higher\) in the supply chain.

8.  To edit the supply chain record, select it from the list and select **Edit**.

9.  To export the supply chain record, select **Export**.

10. To delete the supply chain record, select it from the list and select **Delete**.


-   **[Create New ICT service supply chain form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-supply-chain-form.md)**  
On the Create New ICT service supply chain form, fill in the fields.

**Parent Topic:**[Using Digital resilience third-party registers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/using-dg-registers.md)

