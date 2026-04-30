---
title: AWS Get IAM Login Profile action
description: Action that retrieves the user name for the specified Amazon Web Services \(AWS\) Identity Access Management \(IAM\) user.
locale: en-US
release: yokohama
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Cloud Action Library reference, Cloud Action Library, ITOM Cloud Accelerate, IT Operations Management]
---

# AWS Get IAM Login Profile action

Action that retrieves the user name for the specified Amazon Web Services \(AWS\) Identity Access Management \(IAM\) user.

## Roles and availability

-   **Subscription requirements**

    To use this action in custom flows, you must obtain an Integration Hub Enterprise subscription or an App Engine subscription. For more information, see [Request Integration Hub](https://www.servicenow.com/docs/access?context=request-ih-overview&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

-   **Role requirements**

    This action requires roles granted by delegated development or assigned to the user. For more information, see [User access to Flow Designer](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).


## Cloud permission

To execute this action, the caller must have the **iam:GetLoginProfile** cloud permission.

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

-   **Result**

    Data type: **True/False**

    Status of the action.

    -   **True**: Successful
    -   **False**: Failed

**Parent Topic:**[Cloud Action Library reference](cloud-action-library-reference.md)

