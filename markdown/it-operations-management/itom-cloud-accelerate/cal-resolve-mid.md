---
title: CAL - Resolve MID subflow
description: Subflow that returns a suitable MID Server based on the specified MID Server selection criteria.
locale: en-US
release: yokohama
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Cloud Action Library reference, Cloud Action Library, ITOM Cloud Accelerate, IT Operations Management]
---

# CAL - Resolve MID subflow

Subflow that returns a suitable MID Server based on the specified MID Server selection criteria.

## Roles and availability

-   **Subscription requirements**

    To use this subflow in custom flows, you must obtain an Integration Hub Enterprise subscription or an App Engine subscription. For more information, see [Request Integration Hub](https://www.servicenow.com/docs/access?context=request-ih-overview&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

-   **Role requirements**

    This subflow requires roles granted by delegated development or assigned to the user. For more information, see [User access to Flow Designer](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).


## Cloud permission

You don't need any cloud permission to execute this action.

## Inputs

Provide a value for each input that your subflow needs. To add dynamic values, you can also select data pills using the pill picker.

-   **Service Account**

    Data type: **Record**

    Service account for which a suitable MID Server is sought.


## Outputs

You can use these outputs as inputs for other subflows.

-   **Mid Server**

    Data type: **Record**

    Resolved MID Server.

-   **Error**

    Data type: **String**

    Error encountered during identification of the MID Server.


**Parent Topic:**[Cloud Action Library reference](cloud-action-library-reference.md)

