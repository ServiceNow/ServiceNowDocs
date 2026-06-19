---
title: Admin in ITOM Configuration Console
description: Administrators can configure Discovery settings, assign roles, manage credentials, and review Discovery schedules, errors, and anomalies through the ITOM Configuration Console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/admin-disco-itom.html
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-06-19"
reading_time_minutes: 3
breadcrumb: [ITOM Configuration Console for Discovery, Discovery setup, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Admin in ITOM Configuration Console

Administrators can configure Discovery settings, assign roles, manage credentials, and review Discovery schedules, errors, and anomalies through the ITOM Configuration Console.

The following table describes the administrative tasks available in the Discovery module.

|Task|Description|Required Role|
|----|-----------|-------------|
|[Assign Discovery admins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/assign-disco-admin.md)|Assign or remove the discovery\_admin role from users to manage Discovery administration permissions.|admin|
|[Create a MID Server user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-mid-server-user.md)|Create a dedicated user with the mid\_server role to authenticate the MID Server to your ServiceNow instance.|admin|
|[Deploy MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/deploy-mid-server.md)|Use MID Server to securely connect ServiceNow behind your firewall, enabling data flow, automated discovery, and seamless integration.|admin|
|[Validate MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/validate-mid-server.md)|Validate that your MID Servers are trusted to connect to your ServiceNow instance.|admin|
|[IP credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-ip-credentials.md)|Create IP credentials for Discovery to securely connect to devices in your environment.|discovery\_admin|
|[Cloud Credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-cloud-credentials.md)|Create cloud credentials to manage access to cloud-based applications.|discovery\_admin|
|[Quick discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/quick-disco.md)|Scan one or more IPs to see what's running in your environment without creating on going schedules.|discovery\_admin|
|Discovery schedules|Configure [IP-based](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/t-dawCreateNewDiscoSchedule.md) or cloud-based Discovery schedules in Discovery Admin Workspace. For cloud-based schedules, you can configure discovery for [AWS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-AWS-schedule-DAW.md), [Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-azure-schedule-DAW.md), [GCP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-gcp-schedule-DAW.md), [Alibaba Cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-alibaba-schedule-DAW.md), [IBM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-ibm-schedule-DAW.md), [OCI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-oci-schedule-DAW.md), [OpenStack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-openstack-schedule-DAW.md), [VMware](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-vmware-schedule-DAW.md), and [oVirt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-ovirt-schedule-DAW.md).|discovery\_admin|
|[Schedule review](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/discovery-admin-workspace-schedules.md)|Access the Schedules page in Discovery Admin Workspace to view and manage your Discovery schedules.|discovery\_admin|
|[Discovery errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/discovery-admin-workspace-diagnostics.md)|Access the Diagnostics page in Discovery Admin Workspace to review errors found from your discoveries.|discovery\_admin|
|[Anomaly detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/discovery-admin-workspace-diagnostics.md)|Access Diagnostics page in Discovery Admin Workspace to review anomalies found in your Discovery schedules.|discovery\_admin|

