---
title: CAL - Resolve Credential Alias subflow
description: Subflow that returns the credentials alias for the mentioned credential.
locale: en-US
release: australia
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cloud Action Library reference, Cloud Action Library, ITOM Cloud Accelerate, IT Operations Management]
---

# CAL - Resolve Credential Alias subflow

Subflow that returns the credentials alias for the mentioned credential.

## Roles and availability

-   **Subscription requirements**

    To use this subflow in custom flows, you must obtain an Integration Hub Enterprise subscription or an App Engine subscription. For more information, see [Request Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/request-ih-overview.md).

-   **Role requirements**

    This subflow requires roles granted by delegated development or assigned to the user. For more information, see [User access to Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/user-access-flow-designer.md).


## Cloud permission

You don't need any cloud permission to execute this action.

## Inputs

Provide a value for each input that your subflow needs. To add dynamic values, you can also select data pills using the pill picker.

-   **Service Account**

    Data type: **Record**

    Service account for which a suitable credential alias is sought.


## Outputs

You can use these outputs as inputs for other subflows.

-   **Credential Alias**

    Data type: **Record**

    Credential alias for the AWS credential.

-   **Error**

    Data type: **String**

    If the underlying Cloud Action Library \(CAL\) action fails to return a credential alias, it returns an error message that explains the reason behind the failure. The Error variable contains the error message returned by the underlying CAL action.


**Parent Topic:**[Cloud Action Library reference](cloud-action-library-reference.md)

