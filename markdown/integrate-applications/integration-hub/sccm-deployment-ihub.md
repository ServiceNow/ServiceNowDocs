---
title: SCCM deployment process
description: Order an SCCM application from a client software distribution \(CSD\) catalog item in the service catalog triggers the Order Client Software flow.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Client software distribution from SCCM, Client Software Distribution using Integration Hub, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# SCCM deployment process

Order an SCCM application from a client software distribution \(CSD\) catalog item in the service catalog triggers the Order Client Software flow.

This process deploys an SCCM application to a user or device through a service catalog order:

1.  If the **Skip approval** check box is cleared in the software catalog item, the Order Client Software flow sends the catalog request to the requesting user's manager for approval.
2.  If the **Check license compliance** check box is selected in the software catalog item, the flow performs a software license check. If there is no license available, the flow creates a catalog task to procure more licenses and assigns the task to the CSD Administrators group.
3.  The Order Client Software flow triggers the Deploy SCCM Application flow as a subflow. This subflow adds either the user or the device to the SCCM collection using the Add to User Collection or Add to Device Collection actions in the [Microsoft SCCM Spoke](../concept/microsoft-sccm-spoke.md).
4.  If the software configuration specifies **SCCM uninstall collection** in the software catalog item, the Deploy SCCM Application subflow checks if the user or device exists in the uninstall collection. The flow uses the Is Device in Collection or Is User in Collection in the [Microsoft SCCM Spoke](../concept/microsoft-sccm-spoke.md). If the user or device exists in the uninstall collection, the flow removes the device or user. The subflow uses the Remove from Device Collection or Remove from User Collection action in the [Microsoft SCCM Spoke](../concept/microsoft-sccm-spoke.md) before adding it to the SCCM install collection.

**Parent Topic:**[Client software distribution from SCCM](../concept/csd-from-sccm-ihub.md)

