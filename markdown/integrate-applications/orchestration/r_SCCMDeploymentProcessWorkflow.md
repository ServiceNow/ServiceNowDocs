---
title: SCCM deployment
description: Ordering an SCCM application from a client software distribution \(CSD\) catalog item in the service catalog triggers the Order Client Software workflow.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Client software distribution from SCCM, Client Software Distribution, Orchestration applications, Classic Orchestration, Data and Automation]
---

# SCCM deployment

Ordering an SCCM application from a client software distribution \(CSD\) catalog item in the service catalog triggers the Order Client Software workflow.

This process deploys an SCCM application to a user or device through a service catalog order:

1.  If the **Skip approval** check box is cleared in the software catalog item, the Order Client Software workflow sends the catalog request to the requesting user's manager for approval.
2.  If the **Check license compliance** check box is selected in the software catalog item, the workflow performs a software license check. If there is no license available, the workflow creates a catalog task to procure more licenses and assigns the task to the Client Software Distribution Administrators group.
3.  The Order Client Software workflow triggers the Deploy SCCM Application workflow as a subflow. This workflow adds either the user or the device to the SCCM collection using the [Add to User Collection](../../../administer/orchestration-activities/reference/r_AddToUserCollectionActivity.md) or [Add to Device Collection](../../../administer/orchestration-activities/reference/r_AddToDeviceCollectionActivity.md) SCCM activity.
4.  If the software configuration specifies SCCM uninstall collection in the software catalog item, the Deploy SCCM Application workflow checks if the user or device exists in the uninstall collection. The workflow uses the Is Device in Collection or Is User in Collection SCCM activity. If the user or device exists in the uninstall collection, the workflow removes the device or user. The workflow uses the Remove from Device Collection or Remove from User Collection SCCM activity before adding it to the SCCM install collection.

**Parent Topic:**[Client software distribution from SCCM](../concept/c_CSDFromAnSCCMHost.md)

