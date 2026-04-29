---
title: Configuring External Key Management Service
description: Set up External Key Management Service \(EKMS\) to control the encryption of your ServiceNow data using your Amazon Web Service Key Management System \(AWS KMS\).
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [External Key Management Service, Field Encryption, Encryption]
---

# Configuring External Key Management Service

Set up External Key Management Service \(EKMS\) to control the encryption of your ServiceNow data using your Amazon Web Service Key Management System \(AWS KMS\).

## Configuration Overview

Configuring External Key Management Service \(EKMS\) involves installing the plugin, connecting to AWS KMS, and setting up encryption for specific fields. Complete these tasks to establish external key management for your ServiceNow data.

## Configuration Workflow

1.  Activate the EKMS plugin and assign required user roles
2.  Configure the AWS KMS key definition with connection credentials
3.  Create cryptographic modules that use external key wrapping
4.  Specify which table fields should be encrypted
5.  Set up access policies to control data visibility
6.  Test encryption and access control to verify the configuration

## Prerequisites

Before configuring EKMS, verify that you have:

-   AWS KMS access through your organization's request process
-   Created or identified an AWS KMS key
-   Identity and Access Management \(IAM\) user credentials with KMS permissions
-   IAM user configured with at least these permissions: kms:DescribeKey, kms:Encrypt, and kms:Decrypt
-   admin, security\_admin, and sn\_kmf.cryptographic\_manager roles in ServiceNow

-   **[Activate External Key Management Service](../task/ekms-activate-external-key-management.md)**  
Install the External Key Management Service \(EKMS\) plugin and configure user permissions to enable external key management functionality.
-   **[Configure an external key definition](../task/ekms-configure-external-key-definition.md)**  
Configure your external encryption key to use in External Key Management Service \(EKMS\).
-   **[Create a cryptographic module with external key wrapping](../task/ekms-create-crypto-module.md)**  
Create a cryptographic module that uses external Amazon Web Services Key Management System \(AWS KMS\) key wrapping to encrypt ServiceNow data.
-   **[Create Encrypted Field Configurations](../task/ekms-create-encrypted-field-config.md)**  
Configure specific fields to be encrypted using your External Key Management Service \(EKMS\) cryptographic module with external Amazon Web Services Key Management System \(AWS KMS\) key wrapping.
-   **[Set up Module Access Policies](../task/ekms-set-up-maps.md)**  
Configure module access policies in External Key Management Service \(EKMS\) to control who can view encrypted data in clear text.
-   **[Test an external key definition](../task/ekms-test-external-key-definition.md)**  
Test your external encryption key to use in External Key Management Service \(EKMS\).

**Parent Topic:**[External Key Management Service](ekms-external-key-management.md)

**Related topics**  


[External Key Management Service](ekms-external-key-management.md)

[Activate External Key Management Service](../task/ekms-activate-external-key-management.md)

[Configure an external key definition](../task/ekms-configure-external-key-definition.md)

[Create a cryptographic module with external key wrapping](../task/ekms-create-crypto-module.md)

[Create Encrypted Field Configurations](../task/ekms-create-encrypted-field-config.md)

