---
title: Configure AWS credentials on a CyberArk vault
description: Configure your CyberArk vault with the AWS credentials to be retrieved for use by your instance.Configure your CyberArk vault with the AWS credentials to be retrieved for use by your instance.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CyberArk integration configuration, CyberArk credential storage integration, External credential storage, Get started with credentials, Connections and Credentials, Access Management]
---

# Configure AWS credentials on a CyberArk vault

Configure your CyberArk vault with the AWS credentials to be retrieved for use by your instance.

## Before you begin

Role required: admin

## About this task

Store the credentials as an Account on the CyberArk vault. When you configure access to the vault on your instance, the name you give to the Account must also be used as the credential ID.

**Note:** The procedure that follows references CyberArk Password Vault v14.2.1. If you are using a different version, set up configuration as per official CyberArk Password Vault documentation.

## Procedure

1.  In CyberArk, go to **Accounts** &gt; **Accounts &amp; Requests** &gt; **Accounts View** &gt; **Add Account**.

2.  Select system type: **Cloud Service**.

3.  Assign to platform: **Amazon Web Services - AWS - Access Keys**.

4.  Store in Safe: Select a safe from the list.

5.  Define properties: Enter the following information:

    |Field|Value|
    |-----|-----|
    |AWS IAM Username|Enter the AWS Access Key, as provided by AWS.|
    |AWS Access Key Secret \(optional\)|Enter the AWS Secret Access Key, as provided by AWS.|
    |Customize account name|Toggle slider to enter a custom name for this key.|
    |AWS Access Key ID|Enter the AWS Access Key again, as provided by AWS.|
    |AWS Account ID Number|Enter the AWS Access Key again, as provided by AWS.|
    |AWS Account Alias Name \(optional\)|Enter an alias name for the account.|

6.  Choose **Add**.


## What to do next

If you have not done so already, create a credential identifier on your instance to configure access to the CyberArk vault. For more details, see [Configure access to external credential storage for AWS](../../credentials/concept/external_cred_storage_configuration.md#).

**Parent Topic:**[CyberArk integration configuration](../../credentials/concept/c_CyberArkIntegrationConfiguration.md)

## Configure AWS Credentials on a CyberArk Vault using Classic UI

Configure your CyberArk vault with the AWS credentials to be retrieved for use by your instance.

### Before you begin

Role required: admin

### About this task

CyberArk Password Vault v14.2.1 includes both Accounts View and Accounts View \(Classic UI\) configuration options to store the credentials as an Account. When you configure access to the vault on your instance, the name you give to the Account must also be used as the credential ID.

**Note:** The procedure that follows references CyberArk Password Vault v14.2.1. If you are using a different version, set up configuration as per official CyberArk Password Vault documentation.

### Procedure

1.  In CyberArk, go to **Accounts** &gt; **Accounts &amp; Requests** &gt; **Accounts View \(Classic UI\)** &gt; **Add Account**.

2.  Enter the following information:

    |Field|Value|
    |-----|-----|
    |Device Type|Select **Cloud Service**.|
    |Platform Name|Select **Amazon Web Services - AWS - Access Keys**.|
    |AWS IAM Username|Enter the AWS Access Key, as provided by AWS.|
    |AWS Access Key ID|Enter the AWS Access Key again, as provided by AWS.|
    |AWS Account ID Number|Enter the AWS Access Key again, as provided by AWS.|
    |AWS Access Key Secret|Enter the AWS Secret Access Key, as provided by AWS.|
    |Name|Enter a custom name for this key.|

3.  Choose **Save**.


### What to do next

If you have not done so already, create a credential identifier on your instance to configure access to the CyberArk vault. For more details, see [Configure access to external credential storage for AWS](../../credentials/concept/external_cred_storage_configuration.md#).

