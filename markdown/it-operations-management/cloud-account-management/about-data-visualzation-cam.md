---
title: About data visualization in Cloud Account Management
description: The Cloud Account Management overview dashboard gives a clear view of all cloud accounts and their compliance status. Cloud Account Management pulls data from Cloud Configuration Governance to create a simple, visual overview of compliance. As an admin, you can take the necessary actions for the reported vulnerabilities.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# About data visualization in Cloud Account Management

The Cloud Account Management overview dashboard gives a clear view of all cloud accounts and their compliance status. Cloud Account Management pulls data from Cloud Configuration Governance to create a simple, visual overview of compliance. As an admin, you can take the necessary actions for the reported vulnerabilities.

## Data visualization process

The workflow for creating a scan configuration for data visualization.

1.  Select policy sets:

    -   Choose a predefined policy set or customize policies to specify what to scan for account vulnerabilities.
    -   Cloud Account Management provides default policies for AWS, Azure, and GCP, which you can adjust to meet specific compliance or security requirements.
2.  Select accounts: Identify the accounts to scan by selecting either a management account \(which includes all its member accounts\) or individual member accounts.

3.  Define a scan schedule or execute an on-demand scan: Set up a scan schedule or run an on-demand scan to evaluate vulnerabilities based on the selected policies for the specified accounts.

4.  Daily scans:

    -   Conduct daily scans to identify vulnerabilities and compliance issues in accounts.
    -   These scans generate reports on violations, severity levels, and account aliases, providing a detailed view of account compliance.
5.  Track costs:

    -   Cloud Account Management integrates with the Cloud Cost Management Workspace to track budgets and usage of each account.
    -   Confirm Cloud Cost Management Workspace version 8.1 or above is installed, and billing is configured.

To set up data visualization, see [Set up scan configuration for data visualization](../task/set-up-data-visualization.md).

