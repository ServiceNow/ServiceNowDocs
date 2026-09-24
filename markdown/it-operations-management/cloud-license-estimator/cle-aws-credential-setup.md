---
title: Configure AWS credentials for Cloud License Estimator
description: Configure IAM user permanent credentials for an AWS account.There are several ways to configure AWS Service Accounts depending on the credentials and master accounts. Create an AWS account configuration to estimate the cloud resource count for licensing. Management accounts include all subscriptions under that account.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/cloud-license-estimator/cle-aws-credential-setup.html
release: brazil
product: Cloud License Estimator
classification: cloud-license-estimator
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Configure Cloud License Estimator, Cloud License Estimator, ITOM Visibility, IT Operations Management]
---

# Configure AWS credentials for Cloud License Estimator

Configure IAM user permanent credentials for an AWS account.

## Before you begin

Role required: admin

## About this task

You can configure IAM roles to generate temporary credentials using STS API for a specified account. When using IAM roles for temporary credentials, the Credential ID is optional in the configuration form. However, AWS service accounts require an IAM role to be configured in service accounts. At least one service account must have credentials to generate temporary credentials.

## Procedure

1.  Navigate to **Filter Navigator** &gt; **All** &gt; **ITOM Cloud License Estimator** &gt; **Home**.

2.  On the Home page, select **Go to Credentials** to open the **Credentials \(discovery\_credentials\)** page.

3.  Select **New** &gt; **AWS Credentials** and enter the requisite information.

    A **Credential ID** is generated, which is used when creating configurations.


**Parent Topic:**[Configure Cloud License Estimator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-license-estimator/configure-cloud-license-estimator.md)

**Related topics**  


[Configure Azure Credentials for Cloud License Estimator]()

## Configure AWS service accounts for Cloud License Estimator

There are several ways to configure AWS Service Accounts depending on the credentials and master accounts.

### Before you begin

Role required: admin

### About this task

You can configure service accounts with these options:

-   Configure a service account with permanent credentials. When an account is configured with permanent credentials, it is referred to as an accessor account. This account can be either a management account or member account.

-   Configure a management account with the IAM role.

-   Configure a member account with a custom IAM role. If the member account uses the default IAM Role \(OrganizationAccountAccessRole\) to generate temporary credentials, configuring a service account for the member account is not required.


### Procedure

1.  Navigate to **Filter Navigation** &gt; **All** &gt; **ITOM Cloud License Estimator** &gt; **Home**.

2.  Select the **Service Account List** icon.

3.  On the **Service account** page, select **Create New**.

4.  To configure a service account with permanent credentials, enter the following information:

    -   **Name**: Enter the AWS account name.

    -   **Cloud provider**: Select AWS.

    -   **Account ID**: Enter the AWS account ID.

    -   **Master account**: Select if this is a management account.

    -   **Credentials**: Select the AWS Credential ID created for permanent credentials.

    -   **Master account**: Leave blank if not applicable.

    -   **Accessor Account and Accessor role ARN**: Not applicable for permanent credentials.

5.  To configure a management account with the IAM role, enter the following information:

    -   **Name**: Enter the AWS account name.

    -   **Cloud provider**: Select AWS.

    -   **Account ID**: Enter the AWS account ID.

    -   **Master account**: Select if this is a management account.

    -   **Credentials**: Leave blank. No credentials are required for this account.

    -   **Master account**: Leave blank.

    -   **Accessor Account**: Select the account that has a trust relationship with this management account's IAM role.

    -   **Accessor role ARN:** Enter the full ARN of the IAM role.
6.  To configure a member account with a custom IAM role, enter the following information:

    -   **Name**: Enter the AWS account name.

    -   **Cloud provider**: Select AWS.

    -   **Account ID**: Enter the AWS account ID.

    -   **Master account**: Do not select this, as this is a member account.

    -   **Credentials**: Leave blank. No credentials are required for this account.

    -   **Master account**: Select the management account from the list.

    -   **Accessor Account**: Choose the account that has a trust relationship with this member account's IAM role. This can be either the management account or another member account.

    -   **Accessor role ARN:** Enter the full ARN of the IAM role.
7.  After providing the relevant information for your account type, select **Save**.


## Create an AWS account configuration and generate CLE reports

Create an AWS account configuration to estimate the cloud resource count for licensing. Management accounts include all subscriptions under that account.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Filter Navigation** &gt; **All** &gt; **ITOM Cloud License Estimator** &gt; **Home**.

2.  On the Home page, select **Create Configuration** to open the Create Configuration dialog.

3.  Enter the following details:

    -   **Name**: Enter a name for the configuration.
    -   **Cloud Provider**: Choose **AWS** from the list. If you choose the credential based option, additional fields appear.
    -   **Account ID**: Enter the AWS Account ID.
    -   **Management group**: Select this checkbox if the Account ID is a management account.
    -   **Credentials**: Select the AWS credentials configured for this account.
        -   **Config aggregator account**: Enter the Account ID where the aggregator is created.
        -   **Config aggregator name**: Enter the name of the AWS Config Aggregator.
        -   **Config aggregator region**: Enter the AWS Region where the aggregator is created.
    -   **Activate**: Enable this option.
4.  Select **Save and run license estimator**.

    The configuration is saved and the tool generates the report. You are redirected to the **Report** page where the status of the report generation can be tracked.

5.  From the **Report** page, select **Download resource report** to download a PDF of the report.


**Related topics**  


[Generate Cloud License Estimator reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-license-estimator/cle-generate-reports.md)

