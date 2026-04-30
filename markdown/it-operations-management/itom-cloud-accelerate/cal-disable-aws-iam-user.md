---
title: Disable AWS IAM User action
description: Action that deletes the password for the specified IAM user, which terminates the user's ability to access Amazon Web Services \(AWS\) services through the AWS Management Console.
locale: en-US
release: zurich
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Cloud Action Library reference, Cloud Action Library, ITOM Cloud Accelerate, IT Operations Management]
---

# Disable AWS IAM User action

Action that deletes the password for the specified IAM user, which terminates the user's ability to access Amazon Web Services \(AWS\) services through the AWS Management Console.

## Roles and availability

-   **Subscription requirements**

    To use this action in custom flows, you must obtain an Integration Hub Enterprise subscription or an App Engine subscription. For more information, see [Request Integration Hub](https://www.servicenow.com/docs/access?context=request-ih-overview&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

-   **Role requirements**

    This action requires roles granted by delegated development or assigned to the user. For more information, see [User access to Flow Designer](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).


## Cloud permission

To execute this action, the caller must have the **iam:DeleteLoginProfile** cloud permission.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also select data pills using the pill picker.

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

-   **IAM Account**

    Data type: **String**

    AWS IAM user name.


## Outputs

You can use these outputs as inputs for other actions.

-   **Is Access Denied**

    Data type: **String**

    Server authorization status of the call.

    -   **True**: The server has authorized the call
    -   **False**: The server didn't authorize the call
-   **error\_code**

    Data type: **String**

    Client error code returned for the failed call.

-   **result**

    Data type: **True/False**

    Status of the action.

    -   **True**: Successful
    -   **False**: Failed
-   **error\_message**

    Data type: **String**

    Error message returned for the failed call.


**Parent Topic:**[Cloud Action Library reference](cloud-action-library-reference.md)

