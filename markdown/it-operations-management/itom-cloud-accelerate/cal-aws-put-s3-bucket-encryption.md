---
title: AWS Put S3 Bucket Encryption action
description: Action that configures the default encryption and Amazon Web Services \(AWS\) S3 Bucket Key for an existing bucket.
locale: en-US
release: australia
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cloud Action Library reference, Cloud Action Library, ITOM Cloud Accelerate, IT Operations Management]
---

# AWS Put S3 Bucket Encryption action

Action that configures the default encryption and Amazon Web Services \(AWS\) S3 Bucket Key for an existing bucket.

## Roles and availability

-   **Subscription requirements**

    To use this action in custom flows, you must obtain an Integration Hub Enterprise subscription or an App Engine subscription. For more information, see Request Integration Hub.

-   **Role requirements**

    This action requires roles granted by delegated development or assigned to the user. For more information, see User access to Flow Designer.


## Cloud permission

To execute this action, the caller must have the **s3:PutEncryptionConfiguration** cloud permission.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also select data pills using the pill picker.

-   **Bucket Name**

    Data type: **String**

    Name of the AWS S3 bucket.

-   **Credential Alias**

    Data type: **Record**

    Credential alias for the AWS credential.

-   **Location**

    Data type: **String**

    Name of the datacenter.

-   **Use MID**

    Data type: **True/False**

    Selection to indicate whether to use a MID Server to make the outbound calls.

-   **MID Server**

    Data type: **Record**

    MID Server for making the outbound calls.

-   **Gov Cloud**

    Data type: **True/False**

    Not supported.


## Outputs

You can use these outputs as inputs for other actions.

-   **Is Access Denied**

    Data type: **String**

    Server authorization status of the call.

    -   **True**: The server has authorized the call
    -   **False**: The server didn't authorize the call
-   **Bucket Region**

    Data type: **String**

    Datacenter where the specified AWS S3 bucket is hosted.

-   **Error Code**

    Data type: **String**

    Client error code returned for the failed call.

-   **Result**

    Data type: **True/False**

    Status of the action.

    -   **True**: Successful
    -   **False**: Failed
-   **Redirected**

    Data type: **String**

    If the AWS S3 bucket is not available in the specified datacenter, the **Bucket Region** variable specifies the datacenter of the AWS S3 bucket.

-   **Error Message**

    Data type: **String**

    Error message returned for the failed call.


**Parent Topic:**[Cloud Action Library reference](cloud-action-library-reference.md)

