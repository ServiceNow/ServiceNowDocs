---
title: CAL - Azure VM Monitoring Metric Data action
description: Action that returns monitoring information for the specified Microsoft Azure Virtual Machine \(VM\).
locale: en-US
release: australia
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cloud Action Library reference, Cloud Action Library, ITOM Cloud Accelerate, IT Operations Management]
---

# CAL - Azure VM Monitoring Metric Data action

Action that returns monitoring information for the specified Microsoft Azure Virtual Machine \(VM\).

## Roles and availability

-   **Subscription requirements**

    To use this action in custom flows, you must obtain an Integration Hub Enterprise subscription or an App Engine subscription. For more information, see [Request Integration Hub](https://www.servicenow.com/docs/access?context=request-ih-overview&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

-   **Role requirements**

    This action requires roles granted by delegated development or assigned to the user. For more information, see [User access to Flow Designer](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US).


## Cloud permission

To execute this action, the caller must have the **Microsoft.Compute/virtualMachines/\{vmName\}/instanceView** cloud permission.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also select data pills using the pill picker.

-   **Credential Alias**

    Data type: **Record**

    Credential alias for the Microsoft Azure credential.

-   **Version**

    Data type: **String**

    Version of the Microsoft Azure API.

-   **VM**

    Data type: **Object.Array**

    URI of the VM resource.


## Outputs

You can use these outputs as inputs for other actions.

-   **Result**

    Data type: **String**

    The result variable contains the monitoring information for the specified Microsoft Azure VM.


**Parent Topic:**[Cloud Action Library reference](cloud-action-library-reference.md)

