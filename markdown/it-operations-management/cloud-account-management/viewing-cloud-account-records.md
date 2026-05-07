---
title: Viewing cloud account records
description: The Cloud account records page is a comprehensive dashboard that provides information to help you manage a cloud account.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Viewing Cloud Account Management dashboards, Using Cloud Account Management in Cloud Workspace, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Viewing cloud account records

The Cloud account records page is a comprehensive dashboard that provides information to help you manage a cloud account.

## Before you begin

Role required: sn\_itom\_cam.cw\_admin

## Procedure

1.  Access **Cloud Workspace**.

    As an admin, you can access the Cloud Accounts page using one of the following.

    -   Navigate to **All** &gt; **Cloud Workspace**
    -   Navigate to **Workspaces** &gt; **Cloud Workspace**
2.  Select **Manage and Configure**.

3.  Select the account name to view the details of the corresponding account.

    The details provided for the account are listed in the following table.

<table id="table_o15_wjy_33c"><thead><tr><th>

Tabs

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Overview

</td><td>

This section provides the following critical information about the account: -   **Total assets**: The total number of assets associated with the account.
-   **Last month spend**: Actual spend on your service accounts for the previous month.

**Note:** This field appears only if the Cloud Cost Management workspace plugin is enabled.

-   **Critical configuration violations**: The number of critical configuration violations.
-   **Critical security findings**: The total number of critical security findings.
-   **Account details**: Critical information about the account including cloud provider, created date, alias, cost center, business unit, application service, department, cloud org, and cloud account group.
-   **People responsible for the account**: The individuals or teams responsible for managing the account such as the account owner, email group, and primary and secondary teams.
-   **Tags**: The discovered tag key-value pairs from the cloud provider.
-   **Certification**: The certification status, last certification date, last certified by, and certification due date of the account.


</td></tr><tr><td>

Assets

</td><td>

Assets discovered in the cloud account.

</td></tr><tr><td>

Configuration violations

</td><td>

Violations associated with the cloud account.

</td></tr><tr><td>

Security findings

</td><td>

Cloud account misconfigurations and critical host findings.

</td></tr><tr><td>

Costs \(appears only if Cloud Cost Management Workspace plugin is enabled\)

</td><td>

This section provides critical budgeting information for the cloud account:-   **Last month spend**: Actual spend on your service accounts for the previous month.
-   **Monthly budget**: Valid budget of your cloud assets for that month.
-   **Monthly Variance**: Difference between the monthly budget and last month spends, indicating whether spending was over or under the approved budget.
-   **YTD annual spend**: The cumulative total expenditure from the start of the current year until date.
-   **Monthly spend chart**: A rolling 13-month visualization that plots actual spend against a constant budget line, enabling trend analysis over time.


</td></tr></tbody>
</table>
