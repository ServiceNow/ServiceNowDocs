---
title: Configure the process for creating medical devices included in in-service requests
description: Use scripted extension points to decide what medical devices are created after an in-service request for a medical device is submitted.
locale: en-US
release: zurich
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Set medical devices in-service, Configure, Healthcare Computerized Maintenance Management System, Clinical Device Management, Healthcare and Life Sciences]
---

# Configure the process for creating medical devices included in in-service requests

Use scripted extension points to decide what medical devices are created after an in-service request for a medical device is submitted.

## Before you begin

**Important:** Healthcare Computerized Maintenance Management System is now deprecated and no longer supported or available for new activation. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](../concept/clinical-device-mgmt-overview.md).

Set the application scope to Healthcare Computerized Maintenance Management System using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

Role required: admin

## About this task

The Healthcare Computerized Maintenance Management System \(Healthcare CMMS\) application installs the `sn_hcls_cmms.CreateDevicesForOnboardCase` script, the `CreateDevicesForOnboardCase` script include, and the `CreateDevicesForOnboardCase` extension point.

The `sn_hcls_cmms.CreateDevicesForOnboardCase` script is preconfigured to set the medical devices in-service request form available by default within the application. Before creating a medical device in-service request case, the application runs the `sn_hcls_cmms.CreateDevicesForOnboardCase` script and uses the following submission workflow logic to create records and avoid duplication of records:

1.  Create a medical device if the serial number of the device doesn't exist.
2.  Create a medical device model if one doesn't exist or associate the medical device with an existing model as included in the medical device in-service request form.
3.  Create work orders for the initial inspection of medical devices.
4.  Set the state of the devices to **Installed** when the medical device in-service case is set to **Closed complete**.

Using extension points makes it easier to integrate customizations without actually altering the base code. You can extend standard base functionality using customized scripts. For more information, see [Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

An implementation is available in the base system for scripted extension points. You can modify the data and add additional fields.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** column, search for and click **sn\_hcls\_cmms.CreateDevicesForOnboardCase**.

3.  On the Extension Point form, select a script include to use the `CreateDevicesForOnboardCase` extension point by creating and registering a custom script include.

    You can refer to the CreateDevicesForOnboardCase script include provided with the application to create a custom script include to set the medical device in-service cases. For more information, see [Registering custom script includes against the scripted extension points](https://www.servicenow.com/docs/access?context=impl-scripted-ext-pts-custom-code&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

4.  Customize the submission workflow logic of your medical device in-service request form by adding the `createDevices`,`checkForDuplicateDevices`, `checkForDuplicateDevicesForNewModel`, `associateToExistingModel`, `createModel`, `createInspectionWorkOrders`, `installDevices`, and `cancelDevices` methods to your script include that implements the `CreateDevicesForOnboardCase` extension point.

    You can create multiple implementations for an extension point and provide an order number for each implementation. The implementation that has the lowest order number is executed first.

<table id="table_fkq_ww3_jtb"><thead><tr><th>

Customization

</th><th>

Implementation

</th></tr></thead><tbody><tr><td>

Create a medical device only when the selected model contains a device with a unique serial number.

</td><td>

Include the `createDevices` method of the `CreateDevicesForOnboardCase` extension point in the implementation.

</td></tr><tr><td>

When selecting an existing medical device model, check whether the serial numbers of the medical devices included in the medical device in-service request exist.

</td><td>

Include the `checkForDuplicateDevices` method of the `CreateDevicesForOnboardCase` extension point in the implementation.

</td></tr><tr><td>

When adding a new medical device model, check whether the serial numbers of the medical devices included in the medical device in-service request exist.

</td><td>

Include the `checkForDuplicateDevicesForNewModel` method of the `CreateDevicesForOnboardCase` extension point in the implementation.

</td></tr><tr><td>

Check whether any existing medical device model of the same name, serial number, and manufacturer included in the medical device in-service request exists and associate the model of the medical device with the medical device in-service case.

</td><td>

Include the `associateToExistingModel` method of the `CreateDevicesForOnboardCase` extension point in the implementation.

</td></tr><tr><td>

Create a medical device model with the name, serial number, manufacturer, and description as included in the medical device in-service request and associate the medical device model with the medical device in-service case.

</td><td>

Include the `createModel` method of the `CreateDevicesForOnboardCase` extension point in the implementation.

</td></tr><tr><td>

Create work orders for the initial inspection of each medical device included in the medical device in-service case.

</td><td>

Include the `createInspectionWorkOrders` method of the `CreateDevicesForOnboardCase` extension point in the implementation.

</td></tr><tr><td>

Set the status of medical devices that are associated with the medical device in-service case to **Installed**.

</td><td>

Include the `installDevices` method of the `CreateDevicesForOnboardCase` extension point in the implementation.

</td></tr><tr><td>

Set the status of medical devices that are associated with the medical device in-service case to **Canceled**.

</td><td>

Include the `cancelDevices` method of the `CreateDevicesForOnboardCase` extension point in the implementation.

</td></tr></tbody>
</table>5.  On the Extension Point form, click **Update**.


