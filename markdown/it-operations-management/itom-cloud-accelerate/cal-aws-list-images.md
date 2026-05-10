---
title: AWS List Images action
description: Action that describes the specified images \(AMIs, AKIs, and ARIs\) available to you or all of the images available to you.
locale: en-US
release: australia
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cloud Action Library reference, Cloud Action Library, ITOM Cloud Accelerate, IT Operations Management]
---

# AWS List Images action

Action that describes the specified images \(AMIs, AKIs, and ARIs\) available to you or all of the images available to you.

## Roles and availability

-   **Subscription requirements**

    To use this action in custom flows, you must obtain an Integration Hub Enterprise subscription or an App Engine subscription. For more information, see [Request Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/request-ih-overview.md).

-   **Role requirements**

    This action requires roles granted by delegated development or assigned to the user. For more information, see [User access to Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/user-access-flow-designer.md).


## Cloud permission

To execute this action, the caller must have the **ec2:DescribeImages** cloud permission.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also select data pills using the pill picker.

-   **Location**

    Data type: **String**

    Name of the datacenter.

-   **Use MID**

    Data type: **True/False**

    Selection to indicate whether to use a MID Server to make the outbound calls.

-   **MID Server**

    Data type: **Record**

    MID Server for making the outbound calls.

-   **Version**

    Data type: **String**

    Version of the AWS API.

-   **Limit**

    Data type: **Integer**

    Number of pages to return per call.

-   **Next Token**

    Data type: **String**

    Starting page token.

-   **Credential Alias**

    Data type: **Record**

    Credential alias for the AWS credential.

-   **Filters**

    Data type: **Object**

    A filter name and value pair that is used to return a specific list of results from the describe operation. Filters can be used to match a set of resources based on criteria such as tags, attributes, or IDs.


## Outputs

You can use these outputs as inputs for other actions.

-   **Result**

    Data type: **Object**

    A complex object containing information about the images.


**Parent Topic:**[Cloud Action Library reference](cloud-action-library-reference.md)

