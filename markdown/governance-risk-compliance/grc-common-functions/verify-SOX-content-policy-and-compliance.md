---
title: Verify the SOX Content Pack in Policy and Compliance Management
description: After importing the SOX Content Pack, verify and edit the profile types, profiles, policies, policy statements, controls, policies, indicator templates, and indicators, within the Policy and Compliance Management application.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [SOX content pack, GRC content packs, Common GRC features, Governance, Risk, and Compliance]
---

# Verify the SOX Content Pack in Policy and Compliance Management

After importing the SOX Content Pack, verify and edit the profile types, profiles, policies, policy statements, controls, policies, indicator templates, and indicators, within the Policy and Compliance Management application.

## Before you begin

Role required: Compliance Admin \(sn\_compliance.admin\)

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Scoping** &gt; **Entity Types**.

    A **SOX Processes** entity type is added and is used to generate the SOX profiles:

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
    ![Profile type record is pictured with the Profiles related list](../image/SOX-profile-type.png)

2.  If using the Kingston SOX contact pack, under the Entity filters related list, a filter is added to query the SOX processes table for the generation of SOX entities.

    ![Profile type record is pictured with the Profile Filters Related List](../image/SOX-profile-filter.png)

3.  Open an entity to see all the downstream controls.

    ![Profile record is pictured with the Profile Types Related List](../image/SOX-downstream-controls.png)

4.  Navigate to **Policy and Compliance** &gt; **Policies and Procedures** &gt; **Policies**.

    All SOX policies have been added in the Draft state:

    -   Accounts Payable Flowchart
    -   Accounts Receivable Standard Operating Procedures
    -   Commissions Standard Operating Procedures
    -   Entity Level Standard Operating Procedures
    -   Equity - Stock Based Compensation Standard Operating Procedures
    -   Financial Reporting - Standard Operating Procedure
    -   Fixed Assets Standard Operating Procedures
    -   General Ledger - Flowchart
    ![List of all policies is pictured](../image/SOX-draft-policies.png)

5.  Open a SOX policy record.

    Notice that there is no text in the policy. Create your own policy and initiate the policy lifecycle.

6.  Navigate to **Policy and Compliance** &gt; **Policies and Procedures** &gt; **Policy Statements**.

7.  In the search bar, enter `SOX` in the **Name** field.

    **Note:** The names of all SOX-related policy statements begin with **SOX**.

    -   All the SOX policy statements are created and assigned to SOX policies.
    -   The SOX Control Attestation is created and added to the policy statement.
    ![List of Policy Statements is pictured with all Policy Statement beginning with SOX in the Name](../image/SOX-policy-statements.png)

8.  Navigate to **Policy and Compliance** &gt; **Controls**.

9.  In the search bar, enter `SOX` in the **Name** field.

    **Note:** The names of all SOX-related controls begin with **SOX**.

    -   All the SOX controls are created for each entity.
    -   The SOX Control Attestation is added to all controls with no attestation respondents.
    ![A list of SOX Controls is pictured](../image/SOX-controls.png)

10. Navigate to **Policy and Compliance** &gt; **Indicators**.

    SOX Control Indicators were added and indicator templates were assigned to them.

    ![A list of SOX Indicators is pictured](../image/SOX-indicators-templates.png)


## Result

For information about the SOX Compliance Dashboard, see [SOX Content Pack dashboard and reports](../concept/grc-SOX-compliance-content-pack.md).

**Parent Topic:**[Sarbanes-Oxley \(SOX\) Content Pack](../concept/sn-store-SOX-governance-risk-compliance.md)

