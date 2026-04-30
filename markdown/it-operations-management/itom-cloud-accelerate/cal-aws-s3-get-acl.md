---
title: CAL - AWS S3 Get ACL subflow
description: Subflow that retrieves the Access Control List \(ACL\) details for the specified Amazon Web Services \(AWS\) S3 bucket.
locale: en-US
release: yokohama
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Cloud Action Library reference, Cloud Action Library, ITOM Cloud Accelerate, IT Operations Management]
---

# CAL - AWS S3 Get ACL subflow

Subflow that retrieves the Access Control List \(ACL\) details for the specified Amazon Web Services \(AWS\) S3 bucket.

## Roles and availability

-   **Subscription requirements**

    To use this subflow in custom flows, you must obtain an Integration Hub Enterprise subscription or an App Engine subscription. For more information, see [Request Integration Hub](https://www.servicenow.com/docs/access?context=request-ih-overview&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

-   **Role requirements**

    This subflow requires roles granted by delegated development or assigned to the user. For more information, see [User access to Flow Designer](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).


## Cloud permission

To execute this subflow, the caller must have the **s3:GetBucketAcl** cloud permission.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also select data pills using the pill picker.

-   **Bucket Name**

    Data type: **String**

    Name of the AWS S3 bucket.

-   **Use MID**

    Data type: **True/False**

    Selection to indicate whether to use a MID Server to make the outbound calls.

-   **MID Server**

    Data type: **Record**

    MID Server for making the outbound calls.

-   **Credential Alias**

    Data type: **Record**

    Credential alias for the AWS credential.


## Outputs

You can use these outputs as inputs for other actions.

-   **Is Access Denied**

    Data type: **True/False**

    Server authorization status of the call.

    -   **True**: The server has authorized the call
    -   **False**: The server didn't authorize the call
-   **Bucket Region**

    Data type: **String**

    Datacenter where the specified AWS S3 bucket is hosted.

-   **Error Code**

    Data type: **String**

    Client error code returned for the failed call.

-   **Owner write**

    Data type: **True/False**

    The bucket owner can write into the bucket.

-   **Owner full control**

    Data type: **True/False**

    The owner has all the permissions for the bucket.

-   **Owner listing**

    Data type: **True/False**

    The bucket owner can list the contents of the bucket.

-   **Public write**

    Data type: **True/False**

    Anyone \(public access\) can write into the bucket.

-   **Public listing**

    Data type: **True/False**

    Anyone \(public access\) can list the contents of the bucket.

-   **Public full control**

    Data type: **True/False**

    Everyone \(public access\) has all the permissions.

-   **Auth Users Write**

    Data type: **True/False**

    Authenticated user groups \(users with an AWS account\) can write into the bucket.

-   **Auth Users Full Control**

    Data type: **True/False**

    Authenticated user groups \(users with an AWS account\) have all the permissions for the bucket.

-   **Owner Read ACL**

    Data type: **True/False**

    Owner of the bucket can read the bucket ACL.

-   **Owner Write ACL**

    Data type: **True/False**

    Owner of the bucket can write or update the bucket ACL.

-   **Public Read ACL**

    Data type: **True/False**

    Anyone \(public access\) can read the bucket ACL.

-   **Public Write ACL**

    Data type: **True/False**

    Anyone \(public access\) can write or update the bucket ACL.

-   **Auth Users Read ACL**

    Data type: **True/False**

    Authenticated user groups \(users with an AWS account\) can read the bucket ACL.

-   **Auth Users Write ACL**

    Data type: **True/False**

    Authenticated user groups \(users with an AWS account\) can write or update the bucket ACL.

-   **Auth Users Listing**

    Data type: **True/False**

    Authenticated user group \(users with an AWS account\) can list the contents of the bucket.

-   **Owner ID**

    Data type: **String**

    Canonical user ID of the AWS account.

-   **Owner Display Name**

    Data type: **String**

    Display name of the resource owner.

    For federated login, the subflow doesn't return any Owner Display Name.


**Parent Topic:**[Cloud Action Library reference](cloud-action-library-reference.md)

