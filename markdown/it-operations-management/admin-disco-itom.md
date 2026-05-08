---
title: Admin in ITOM Configuration Console
description: Administrators can configure Discovery settings, assign roles, manage credentials, and review Discovery schedules, errors, and anomalies through the ITOM Configuration Console.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 3
breadcrumb: [ITOM Configuration Console for Discovery, Now Assist for Setup \(ITOM Visibility\), Now Assist for Setup \(ITOM\), IT Operations Management]
---

# Admin in ITOM Configuration Console

Administrators can configure Discovery settings, assign roles, manage credentials, and review Discovery schedules, errors, and anomalies through the ITOM Configuration Console.

The following table describes the administrative tasks available in the Discovery module.

|Task|Description|Required Role|
|----|-----------|-------------|
|[Assign Discovery admins](../task/assign-disco-admin.md)|Assign or remove the discovery\_admin role from users to manage Discovery administration permissions.|admin|
|[MID Server user](../task/create-mid-server-user.md)|Create a dedicated user with the mid\_server role to authenticate the MID Server to your ServiceNow instance.|admin|
|[Deploy MID Server](../task/deploy-mid-server.md)|Use MID Server to securely connect ServiceNow behind your firewall, enabling data flow, automated discovery, and seamless integration.|admin|
|[Validate MID Server](../task/validate-mid-server.md)|Validate that your MID Servers are trusted to connect to your ServiceNow instance.|admin|
|[IP credentials](../task/create-ip-credentials.md)|Create IP credentials for Discovery to securely connect to devices in your environment.|discovery\_admin|
|[Cloud Credentials](../task/create-cloud-credentials.md)|Create cloud credentials to manage access to cloud-based applications.|discovery\_admin|
|[Quick discovery](../task/quick-disco.md)|Scan one or more IPs to see what's running in your environment without creating on going schedules.|discovery\_admin|
|Discovery schedules|Configure [IP-based](../../discovery/task/t-dawCreateNewDiscoSchedule.md) or cloud-based Discovery schedules in Discovery Admin Workspace. For cloud-based schedules, you can configure discovery for [AWS](../../discovery/task/create-AWS-schedule-DAW.md), [Azure](../../discovery/task/create-azure-schedule-DAW.md), [GCP](../../discovery/task/create-gcp-schedule-DAW.md), [Alibaba Cloud](../../discovery/task/create-alibaba-schedule-DAW.md), [IBM](../../discovery/task/create-ibm-schedule-DAW.md), [OCI](../../discovery/task/create-oci-schedule-DAW.md), [OpenStack](../../discovery/task/create-openstack-schedule-DAW.md), [VMware](../../discovery/task/create-vmware-schedule-DAW.md), and [oVirt](../../discovery/task/create-ovirt-schedule-DAW.md).|discovery\_admin|
|[Schedule review](../../discovery/concept/discovery-admin-workspace-schedules.md#)|Access the Schedules page in Discovery Admin Workspace to view and manage your Discovery schedules.|discovery\_admin|
|[Discovery errors](../../discovery/concept/discovery-admin-workspace-diagnostics.md)|Access the Diagnostics page in Discovery Admin Workspace to review errors found from your discoveries.|discovery\_admin|
|[Anomaly detection](../../discovery/concept/discovery-admin-workspace-diagnostics.md)|Access Diagnostics page in Discovery Admin Workspace to review anomalies found in your Discovery schedules.|discovery\_admin|

