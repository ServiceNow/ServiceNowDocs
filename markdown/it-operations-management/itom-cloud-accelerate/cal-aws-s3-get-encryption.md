---
title: CAL - AWS S3 Get Encryption subflow
description: Subflow that returns the default encryption configuration for an Amazon Web Services \(AWS\) S3 bucket.
locale: en-US
release: australia
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cloud Action Library reference, Cloud Action Library, ITOM Cloud Accelerate, IT Operations Management]
---

# CAL - AWS S3 Get Encryption subflow

Subflow that returns the default encryption configuration for an Amazon Web Services \(AWS\) S3 bucket.

## Roles and availability

-   **Subscription requirements**

    To use this subflow in custom flows, you must obtain an Integration Hub Enterprise subscription or an App Engine subscription. For more information, see [Request Integration Hub](https://www.servicenow.com/docs/access?context=request-ih-overview&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

-   **Role requirements**

    This subflow requires roles granted by delegated development or assigned to the user. For more information, see [User access to Flow Designer](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US).


## Cloud permission

To execute this subflow, the caller must have the **s3:GetEncryptionConfiguration** cloud permission.

## Inputs

Provide a value for each input that your subflow needs. To add dynamic values, you can also select data pills using the pill picker.

-   **Bucket Name**

    Data type: **String**

    Name of the AWS S3 bucket.

-   **Credential Alias**

    Data type: **String**

    Credential alias for the AWS credential.

-   **Use Mid**

    Data type: **True/False**

    Selection to indicate whether to use a MID Server to make the outbound calls.

-   **MID Server**

    Data type: **Record**

    MID Server for making the outbound calls.


## Outputs

You can use these outputs as inputs for other subflows.

-   **Is Access Denied**

    Data type: **True/False**

    Server authorization status of the call.

    -   **True**: The server has authorized the call
    -   **False**: The server didn't authorize the call
-   **Is Encrypted**

    Data type: **True/False**

    Encryption status of the AWS resource.

-   **Bucket Region**

    Data type: **String**

    Datacenter of the AWS S3 bucket.

-   **KMS Masterkey Id**

    Data type: **String**

    Customer AWS Key Management Service \(KMS\) key ID used for the default encryption.

-   **Encryption Algorithm**

    Data type: **String**

    Server-side encryption algorithm used for the default encryption.

-   **Bucket Key Enabled**

    Data type: **String**

    Specifies whether Amazon S3 uses an S3 Bucket Key with server-side encryption using KMS \(SSE-KMS\) for new objects in the bucket.

-   **Error Code**

    Data type: **String**

    Client error code returned for the failed call.


**Parent Topic:**[Cloud Action Library reference](cloud-action-library-reference.md)

