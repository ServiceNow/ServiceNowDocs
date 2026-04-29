---
title: SCCM software revocation flow
description: The Revoke SCCM Application flow moves a user or device from an install collection to an uninstall collection to revoke software installed from Microsoft System Center Configuration Manager \(SCCM\).
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SCCM software revocation, CSD from SCCM, Client Software Distribution, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# SCCM software revocation flow

The Revoke SCCM Application flow moves a user or device from an install collection to an uninstall collection to revoke software installed from Microsoft System Center Configuration Manager \(SCCM\).

For the revocation subflow to run, the software package must have a status of [Client software distribution validation process](https://www.servicenow.com/docs/access?context=c_ClientSWDistValidProcess&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) and must be pre-configured for an appropriate uninstall collection. See [Revoke software deployed through the service catalog](../tasks/revoke-from-serv-cat.md) for configuration instructions. When an administrator initiates the revocation process, the system launches the Revoke SCCM Application subflow to move the user or device collection associated with installation to the appropriate SCCM uninstall collection. When the SCCM server performs a policy check, it finds the additions to the user or device uninstall collection and revokes the software package associated with that collection.

The subflow employs two custom actions in the [Microsoft SCCM Spoke](../concept/microsoft-sccm-spoke.md), Remove from User Collection and Remove from Device Collection, to remove either the user or the device from its original collection. The subflow then adds the user or device to the appropriate uninstall collection on the SCCM server with the Add to User Collection or Add to Device Collection activity.

**Note:** This subflow is triggered by the Revoke Client Software subflow.

**Parent Topic:**[SCCM software revocation](../concept/sccm-revocation-ihub.md)

