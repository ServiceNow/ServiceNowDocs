---
title: Flows and subflows installed
description: These flows and subflows are installed with the Client Software Distribution plugin.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Components installed with CSD, Client Software Distribution, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Flows and subflows installed

These flows and subflows are installed with the Client Software Distribution plugin.

|Flow| |
|----|---|
|Order Client Software|Schedules the installation of an ordered application on the selected device. The request requires approvals based on the user input in the catalog item configuration.|
|Deploy Client Software|Deploys a software by executing provider-specific subflow. Creates catalog tasks if there is a failure in the execution of the provider subflow.|

|Subflow|Description|
|-------|-----------|
|Discover And Store SCCM Data|Retrieves lists of applications, collections, and deployments from SCCM servers using [Microsoft SCCM spoke](../concept/microsoft-sccm-spoke.md) actions. An administrator runs this subflow from a UI action in a [SCCM Server Instance record](../tasks/retrieve-sccm-data-ihub.md).|
|Deploy SCCM Application|Triggered by the Order Client Software flow to deploy software through SCCM server. This subflow adds either the user or the device into the SCCM collection.|
|Revoke Client Software|Begins the software revocation process for software deployed by an external provider. Administrators run this subflow from a UI action on the Requested Software record and the Installed Software Not Entitled record. This subflow triggers the appropriate provider subflow that performs the actual revocation. For example, this subflow triggers the Revoke SCCM Application subflow for applications in SCCM uninstall collections.|
|Revoke SCCM Application|Revokes SCCM applications that are members of an uninstall collection. The Revoke Client Software subflow triggers this subflow to revoke software deployed by an SCCM server. This subflow moves either the user or the device from the SCCM collection into the appropriate uninstall collection.|
|CSD Lease End Notification|Notifies user about the lease end date of the software and send link to extend lease end date.|
|CSD Deploy Software Post Processing|Performs post processing after the software deployment is successful. The Deploy Client Software flow triggers this subflow.|
|CSD Lease End Notification|Notifies user about the lease end date of the software and sends link to extend lease end date.|
|Prepare Revocation Data|Prepare data required for the revocation flow.|

**Parent Topic:**[Components installed with client software distribution](comp-installed-csd-ihub.md)

