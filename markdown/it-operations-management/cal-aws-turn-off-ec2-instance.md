---
title: AWS Turn Off EC2 Instance action
description: Action that stops the specified Amazon Web Services \(AWS\) Virtual Machine \(VM\).
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Cloud Action Library reference, Cloud Action Library, ITOM Cloud Accelerate, IT Operations Management]
---

# AWS Turn Off EC2 Instance action

Action that stops the specified Amazon Web Services \(AWS\) Virtual Machine \(VM\).

## Roles and availability

-   **Subscription requirements**

    To use this action in custom flows, you must obtain an Integration Hub Enterprise subscription or an App Engine subscription. For more information, see [Request Integration Hub](https://www.servicenow.com/docs/access?context=request-ih-overview&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

-   **Role requirements**

    This action requires roles granted by delegated development or assigned to the user. For more information, see [User access to Flow Designer](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).


## Cloud permission

To execute this action, the caller must have the **ec2:StopInstances** cloud permission.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also select data pills using the pill picker.

-   **Instances**

    Data type: **String**

    AWS instance ID. Enter the comma-separated list of AWS instance IDs.

    Example: i-1234567890abcdef0, i-1234567761abcdek1

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

    Data type: **True/False** Not supported.


## Outputs

You can use these outputs as inputs for other actions.

-   **Is Access Denied**

    Data type: **True/False**

    Server authorization status of the call.

    -   **True**: The server has authorized the call
    -   **False**: The server didn't authorize the call
-   **Error Message**

    Data type: **String**

    Error message returned for the failed call.

-   **Result**

    Data type: **True/False**

    Status of the action.

    -   **True**: Successful
    -   **False**: Failed
-   **Error code**

    Data type: **String**

    Client error code returned for the failed call.


**Parent Topic:**[Cloud Action Library reference](cloud-action-library-reference.md)

