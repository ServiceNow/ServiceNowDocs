---
title: Verify the SOX Content Pack in Audit Management
description: After importing the SOX Content Pack, verify and edit the entity types, entities, audit engagements, audit tasks, test templates, and test plans within the Audit Management application.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SOX content pack, GRC content packs, Common GRC features, Governance, Risk, and Compliance]
---

# Verify the SOX Content Pack in Audit Management

After importing the SOX Content Pack, verify and edit the entity types, entities, audit engagements, audit tasks, test templates, and test plans within the Audit Management application.

## Before you begin

Role required: Audit Admin \(sn\_audit.admin\)

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Entity Type**.

    A **SOX Processes** entity type is added and is used to generate the SOX entities:

    -   Accounts Receivable
    -   Accounts Payable
    -   Commissions
    -   Equity
    -   Entity Level
    -   Financial Reporting
    -   Fixed Assets
    -   General Ledger
    -   Human Resources
    -   In Scope Application
    -   Inventory
    -   ITGC
    -   Payroll
    -   Purchasing
    -   Revenue Recognition
    -   SAP
    -   SDLC
    -   Tax
    -   Travel and Expense
    -   Treasury
    ![Profiles](../image/SOX-profile-type.png)

2.  Under the Profile filters related list, a filter is added to query the SOX processes table for the generation of SOX profiles.![Profile Types](../image/SOX-profile-filter.png)

3.  Navigate to **Audit** &gt; **All Engagements**.

    The **SOX Audit** engagement has been added in the Scope state with the following fields set as empty:

    -   **Assigned to**
    -   **Auditor**
    -   **Approver**
    ![Engagement](../image/SOX-audit-engagement.png)

4.  Navigate to **Audit** &gt; **All Audit Tasks**.

5.  In the search bar, enter `SOX` in the **Name** field.

    **Note:** The names of all SOX-related audit tasks start with **SOX**.

    The SOX Audit tasks have been added with the following fields:

    -   **Type** is interview or walkthrough
    -   **Assigned to** is empty
    -   **Assigned parent \(engagement\)** is SOX Audit
    ![Audit Tasks](../image/SOX-audit-tasks.png)

6.  Navigate to **Audit** &gt; **Audit Testing** &gt; **Test Templates**.

    The SOX test templates have been added and assigned to policy statements.

    ![Test Templates](../image/SOX-test-templates.png)

7.  Navigate to **Audit** &gt; **Audit Testing** &gt; **Test Plans**.

    The SOX test plans have been generated for controls based on the test templates.

    ![Test Plans](../image/SOX-test-plans.png)


## Result

For information about the SOX Audit Dashboard, see [SOX Content Pack dashboard and reports](../concept/grc-SOX-compliance-content-pack.md).

**Parent Topic:**[Sarbanes-Oxley \(SOX\) Content Pack](../concept/sn-store-SOX-governance-risk-compliance.md)

