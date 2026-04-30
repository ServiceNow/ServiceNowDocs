---
title: Client software distribution ordering process
description: Software deployed by CSD 2.0 can be ordered from the service catalog by individual users or by approved users on behalf of others.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Client Software Distribution 2.0 application, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Client software distribution ordering process

Software deployed by CSD 2.0 can be ordered from the service catalog by individual users or by approved users on behalf of others.

CSD 2.0 catalog items have different options, depending on how ordering is configured.

## Lease start and end dates

All software deployed by CSD 2.0 requires users to specify the beginning date for the lease.

If the catalog item is configured for revocation \(uninstall\), the form displays the **Lease end** field, which allows the requester to define an end date and time for the lease. The system validates user input in these fields to ensure that the dates selected define a future window. The **Lease end** field is not mandatory and can be left blank to order software with no end date.

## Software offered only to the logged in user

If the software catalog item is configured with **Access Type** as **Restricted**, the **User** field does not appear on the order form. The logged in user selects the device on which to deploy the software from the **Device to install this software on** field. Only those devices assigned to the logged in user appear in the list.

In this example, a user has logged into the service catalog to order Google Chrome for the assigned computer. User selects the machine from a list of devices and selects the date and time the lease should begin.

![Ordering software as the logged in user.](../../integrationhub/images/CSDCatOrderLease2.png)

## Software ordered on behalf of another user

If the software catalog item is configured with **Access Type** as **Delegated**, the **User** field appears on the form. The logged in user can select any user from this field. The **Device to install this software on** field only lists the devices assigned to the user selected in the **User** field. If an approval is required for software ordered on behalf of another user, the system automatically sends an approval request to the manager of the user receiving the software. The approval is skipped if the requester is the named user's manager.

In this example, a manager is ordering Google Chrome for a contractor. The manager selects the contractor from the **User** field and then chooses a computer from the list of devices assigned to the contractor. This software has a Microsoft Endpoint Configuration Manager uninstall collection configured, which enables the manager to select an end date for the lease that coincides with the end of the user's contract. When the lease expires, Microsoft Endpoint Configuration Manager automatically uninstalls the software from the device.

![Defining software lease window.](../../integrationhub/images/CSDCatOrderLease.png)

**Note:**

-   For Jamf, the device must have its serial number populated in the device table.
-   For Microsoft Endpoint Configuration Manager, the name must be populated.

![Required fields.](../image/csd2-ordering.png)

**Parent Topic:**[Client Software Distribution 2.0 application](../concept/csd-app-2.md)

