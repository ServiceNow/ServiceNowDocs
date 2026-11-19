---
title: Viewing cloud account records
description: The Cloud account records page is a comprehensive dashboard that provides information to help you manage a cloud account.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/cloud-account-management/viewing-cloud-account-records.html
release: brazil
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2026-11-19"
reading_time_minutes: 3
breadcrumb: [Viewing Cloud Account Management dashboards, Use, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
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
2.  Select **Manage and Configure** &gt; **Cloud accounts** &gt; **Accounts**.

3.  Select the account name to view the details of the corresponding account.

    The account status shows whether the account is managed or unmanaged. A managed account is created or onboarded through Cloud Account Management. An unmanaged account is discovered in the cloud but isn't yet managed by Cloud Account Management. To onboard an unmanaged account, see [Add an unmanaged cloud account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/add-unmanaged-account-cam.md).

<table id="table_o15_wjy_33c"><thead><tr><th>

Tabs

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Overview

</td><td>

This section provides the following critical information about the account: -   **Total assets**: The total number of assets associated with the account.
-   **Last month spend**: Actual spend on your service accounts for the previous month. The trend indicator compares last month's spend with the spend of the month before it. For example, in October, the indicator compares September spend with August spend.

**Note:** This field appears only if the Cloud Cost Management workspace plugin is enabled.

-   **Critical configuration violations**: The number of critical configuration violations.This field appears only if the Cloud Configuration Governance content pack is installed.
-   **Critical security findings**: The total number of critical security findings. This field appears only if the Security Operations integration for Cloud Workspace is installed.
-   **Security findings by risk rating**: A chart of the security findings for the account, grouped by risk rating such as Critical, High, and Medium. This chart appears only if the Security Operations integration for Cloud Workspace is installed.
-   **Account details**: Critical information about the account including cloud provider, created date, alias, cost center, business unit, application service, department, cloud org, and cloud account group.
-   **People responsible for the account**: The individuals or teams responsible for managing the account such as the account owner, email group, and primary and secondary teams.
-   **Tags**: The discovered tag key-value pairs from the cloud provider.
-   **Certification**: The certification status, last certification date, last certified by, and certification due date of the account.


</td></tr><tr><td>

Assets

</td><td>

Assets discovered in the cloud account.For details about viewing assets, see [Viewing cloud assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/viewing-cloud-assets.md).

</td></tr><tr><td>

Configuration violations

</td><td>

Violations associated with the cloud account.This tab appears only if the Cloud Configuration Governance content pack is installed.

</td></tr><tr><td>

Security findings

</td><td>

Cloud account misconfigurations and critical host findings.This tab appears only if the Security Operations integration for Cloud Workspace is installed.

</td></tr><tr><td>

Costs \(appears only if Cloud Cost Management Workspace plugin is enabled\)

</td><td>

This section provides critical budgeting information for the cloud account:-   **Last month spend**: Actual spend on your service accounts for the previous month.
-   **Monthly budget**: Valid budget of your cloud assets for that month.
-   **Monthly Variance**: Difference between the monthly budget and last month spends, indicating whether spending was over or under the approved budget.
-   **YTD annual spend**: The cumulative total expenditure from the start of the current year until date.
-   **Monthly spend chart**: A rolling 13-month visualization that plots actual spend against a constant budget line, enabling trend analysis over time.
-   **View details**: Opens the Cloud Cost Management home page for more detailed cost analysis. This button is only available to users with sn\_clin\_core.insights\_user role.
The **Costs** tab is available to users with the sn\_itom\_cam.cw\_admin or sn\_itom\_cam.account\_manager role. Account managers see cost data only for the accounts that they own or whose primary or secondary team they're a member of.

</td></tr></tbody>
</table>    **Note:** The spend, variance, and assessment data on this page is refreshed daily at 00:00 GMT.


**Parent Topic:**[Viewing Cloud Account Management dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/about-cam-dashboard.md)

**Related topics**  


[Viewing the cloud accounts page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/viewing-cloud-accounts-page.md)

