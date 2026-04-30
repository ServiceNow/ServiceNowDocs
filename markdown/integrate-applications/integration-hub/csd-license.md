---
title: Create licenses and counters for distributed software
description: Licenses and software counters are associated with the software model and must be created if you want to track the license for software deployed by client software distribution \(CSD\).Software deployed by Client Software Distribution \(CSD\) can be ordered from the service catalog by individual users or by approved users on behalf of others.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Client Software Distribution, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create licenses and counters for distributed software

Licenses and software counters are associated with the software model and must be created if you want to track the license for software deployed by client software distribution \(CSD\).

## Before you begin

Role required: sam or admin

You can create software licenses and counters in Software Asset Management for software items deployed from the service catalog by CSD. CSD depends on the software counter result to determine if the license is available for the requested software. If the license **Valuation** is greater than 0, and the license type is **Not allocated**, CSD assumes that the license is available for the software.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Software Licenses**.

2.  Add a new software license for the software model you used in CSD.

3.  Navigate to **Software Asset** &gt; **Reconciliation** &gt; **Software Counters**.

4.  Create a software counter for the software model you created.

5.  Run the counter to retrieve the software license information.


**Parent Topic:**[Client Software Distribution using Integration Hub](../concept/csd-integrationhub.md)

## Client software distribution ordering process

Software deployed by Client Software Distribution \(CSD\) can be ordered from the service catalog by individual users or by approved users on behalf of others.

Client Software Distribution catalog items have different options, depending on how ordering is configured.

### Lease start and end dates

All software deployed by CSD requires users to specify the beginning date for the lease. This is enforced by the Asset Lease Management plugin that is activated automatically with CSD. The system pre-populates the **Lease start** field with the current date and time.

If the catalog item is configured for revocation \(uninstall\), the form displays the **Lease end** field, which allows the requester to define an end date and time for the lease. The system validates user input in these fields to ensure that the dates selected define a future window. The **Lease end** field is not mandatory and can be left blank to order software with no end date.

**Note:** For systems deploying software from Microsoft System Center Configuration Management \(SCCM\), the **Lease end** field is only available if the [Define an SCCM configuration](https://www.servicenow.com/docs/access?context=t_ConfigureSCCMCollections&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) specifies an uninstall collection.

### Software offered only to the logged in user

If the [software catalog item](create-cat-item-ihub.md) is configured with the **Order on behalf of** check box cleared, the **User** field does not appear on the order form. The logged in user selects the device on which to deploy the software from the **Device to install this software on** field. Only those devices assigned to the logged in user appear in the list.

In this example, a user has logged into the service catalog to order Firefox for the assigned computer. User selects the machine from a list of devices and selects the date and time the lease should begin. This software is deployed through Microsoft System Center Configuration Management \(SCCM\), but does not have an uninstall collection configured and cannot be revoked automatically by the system. As a result, the **Lease end** field is not available.

![Ordering software as the logged in user](../images/CSDCatOrderLease2.png)

### Software ordered on behalf of another user

If the software catalog item is configured with the **Order on behalf of** check box selected, the **User** field appears on the form. The logged in user can select any user from this field. The **Device to install this software on** field only lists the devices assigned to the user selected in the **User** field. If an approval is required for software ordered on behalf of another user, the system automatically sends an approval request to the manager of the user receiving the software. The approval is skipped if the requester is the named user's manager.

In this example, a manager is ordering Google Chrome for a contractor. The manager selects the contractor from the **User** field and then chooses a computer from the list of devices assigned to the contractor. This software has an SCCM uninstall collection configured, which allows the manager to select an end date for the lease that coincides with the end of the user's contract. When the lease expires, SCCM automatically uninstalls the software from the device.

![Defining software lease window](../images/CSDCatOrderLease.png)

