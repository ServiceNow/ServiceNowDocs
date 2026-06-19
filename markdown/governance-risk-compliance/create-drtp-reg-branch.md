---
title: Create a branch and enhance digital resilience data
description: Create a branch record in Digital resilience third-party registers. You can then enhance its digital resilience information for compliance with DORA regulation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/create-drtp-reg-branch.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Digital resilience third-party registers, Maintaining Digital resilience third-party registers, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create a branch and enhance digital resilience data

Create a branch record in Digital resilience third-party registers. You can then enhance its digital resilience information for compliance with DORA regulation.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

A legal entity may operate multiple branches across various cities or countries, all of which can be documented on the form.

\[Omitted image "tpr-leg-ent-branches.png"\] Alt text: Branches.

If a new branch is launched, its information is also required for regulatory reporting.

When a valid LEI is entered, the system performs a real-time lookup on the GLEIF \(Global Legal Entity Identifier Foundation\) database at gleif.org. The lookup resolves the entity hierarchy by returning:

-   Direct parent entity LEI and name
-   Ultimate parent entity LEI and name
-   Registered country of the branch entity
-   Relationships such as Parent, Subsidiary, or Branch

It eliminates the need for manual lookup and ensures that branch records contain accurate, regulator-compliant entity identification data aligned with the DORA Register of Information requirements.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Digital resilience third-party registers** &gt; **Branches**.

2.  Select **New**.

    The Create New Branch form is displayed.

3.  On the form, fill in the fields.

    Users typically fill in the following details of the branch:

    -   Branch name and its description
    -   Owner's details
    -   Tagging of business units and departments for reporting purpose
    -   Specifying the branch as a head office or as a different branch other than the head office
    -   ID of the branch and its originating country
    The number for the branch is auto-generated. Once the branch details are complete, the information is ready to be captured in the information register.

    For more information, see [Create New Branch form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-branch-form.md).

4.  Select **Save**.

    When a valid LEI is entered in the Identification code of the branch field, the system validates it against the GLEIF database in real time. On successful validation, the Name of the branch, Country of the branch, and LEI of the financial entity head office fields are automatically populated with data returned from GLEIF.

    The digital resilience information for the branch is shown in the example.

    \[Omitted image "branch-form.png"\] Alt text: Branch.

5.  To edit the branch record, select it from the list and select **Edit**.

6.  To export the branch record, select **Export**.

7.  To delete the branch record, select it from the list and select **Delete**.


## What to do next

Specify the functions that are associated with a branch. For more information, see [Create a function and enhance digital resilience data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-drtp-reg-function.md).

-   **[Create New Branch form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-new-branch-form.md)**  
On the Create New Branch form, fill in the fields.

**Parent Topic:**[Using Digital resilience third-party registers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/using-dg-registers.md)

