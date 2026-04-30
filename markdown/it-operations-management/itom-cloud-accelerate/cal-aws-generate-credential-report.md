---
title: CAL - AWS Generate Credential Report subflow
description: Subflow that lists all users in your account and the status of their various credentials, including passwords, access keys, and MFA devices.
locale: en-US
release: zurich
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Cloud Action Library reference, Cloud Action Library, ITOM Cloud Accelerate, IT Operations Management]
---

# CAL - AWS Generate Credential Report subflow

Subflow that lists all users in your account and the status of their various credentials, including passwords, access keys, and MFA devices.

## Roles and availability

-   **Subscription requirements**

    To use this subflow in custom flows, you must obtain an Integration Hub Enterprise subscription or an App Engine subscription. For more information, see [Request Integration Hub](https://www.servicenow.com/docs/access?context=request-ih-overview&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

-   **Role requirements**

    This subflow requires roles granted by delegated development or assigned to the user. For more information, see [User access to Flow Designer](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).


## Cloud permission

To execute this subflow, the caller must have the **Iam:GetCredentialReport** and **Iam:GenerateCredentialReport**cloud permission.

## Inputs

Provide a value for each input that your subflow needs. To add dynamic values, you can also select data pills using the pill picker.

-   **Credential Alias**

    Data type: **Record**

    Credential alias for the AWS credential.

-   **Use Mid**

    Data type: **True/False**

    Selection to indicate whether to use a MID Server to make the outbound calls.

-   **Mid Server**

    Data type: **Record**

    MID Server for making the outbound calls.

-   **Api Version**

    Data type: **String**

    Version of the AWS API.


## Outputs

You can use these outputs as inputs for other subflows.

-   **Error**

    Data type: **String**

    Description of the error returned by the AWS endpoint.

-   **credential\_report\_list**

    Data type: **Array.Object**

    Complex object containing all fields of the credential report.


**Parent Topic:**[Cloud Action Library reference](cloud-action-library-reference.md)

