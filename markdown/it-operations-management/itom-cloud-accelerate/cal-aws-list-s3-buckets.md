---
title: CAL - AWS List S3 Buckets action
description: Action that returns a list of all the Amazon Web Services \(AWS\) buckets owned by the authenticated sender of the request.
locale: en-US
release: yokohama
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Cloud Action Library reference, Cloud Action Library, ITOM Cloud Accelerate, IT Operations Management]
---

# CAL - AWS List S3 Buckets action

Action that returns a list of all the Amazon Web Services \(AWS\) buckets owned by the authenticated sender of the request.

## Roles and availability

-   **Subscription requirements**

    To use this action in custom flows, you must obtain an Integration Hub Enterprise subscription or an App Engine subscription. For more information, see [Request Integration Hub](https://www.servicenow.com/docs/access?context=request-ih-overview&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

-   **Role requirements**

    This action requires roles granted by delegated development or assigned to the user. For more information, see [User access to Flow Designer](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).


## Cloud permission

To execute this action, the caller must have the **s3:ListBucket** cloud permission.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also select data pills using the pill picker.

-   **Credential Alias**

    Data type: **Record**

    Credential alias for the AWS credential.

-   **Next Token**

    Data type: **String**

    Starting page token.

-   **Use MID**

    Data type: **True/False**

    Selection to indicate whether to use a MID Server to make the outbound calls.

-   **MID Server**

    Data type: **Record**

    MID Server for making the outbound calls.

-   **Limit**

    Data type: **Integer**

    Number of pages to return per call.


## Outputs

You can use these outputs as inputs for other actions.

-   **Result**

    Data type: **Object**

    A complex object containing information about the images owned by the authenticated sender of the request.


**Parent Topic:**[Cloud Action Library reference](cloud-action-library-reference.md)

