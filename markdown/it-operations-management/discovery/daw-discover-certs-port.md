---
title: Run Certificate Discovery via port scans in Discovery Admin Workspace
description: Configure a certificate port probe in the Discovery Admin Workspace, so Discovery collects certificates from devices with secure ports open during your existing IP-based Discovery schedules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/daw-discover-certs-port.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Visibility to TLS certificates, Configure, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Run Certificate Discovery via port scans in Discovery Admin Workspace

Configure a certificate port probe in the Discovery Admin Workspace, so Discovery collects certificates from devices with secure ports open during your existing IP-based Discovery schedules.

## Before you begin

Confirm the following:

-   Discovery Admin Workspace v1.20.0 is installed.
-   Certificate Inventory and Management v4.2.4 is installed.
-   The ServiceNow AI Platform is running on the Brazil, Australia, or Zurich release starting with Patch 8.

Role required: discovery\_admin

## About this task

Port scan discovery reuses your existing IP-based Discovery schedules. Whenever Discovery finds a device with one of the listed ports open, it reads and collects the certificate served on that port. Use this method when certificates are served on secure ports across your network.

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules**.

2.  Select **New Discovery** from the header of any tab on the Schedules page.

3.  Select **Certificate discovery** and select **Continue**.

4.  Select **Discover via port scans**, then select **Continue**.

    The Certificate Port Probe page displays with a list of ports to scan for certificates.

5.  Select the **Active** check box to enable the port probe.

6.  Add ports to scan for certificates.

    -   To add an existing IP service, select **Add** or **Add** &gt; **From existing IP services**. In the Add from existing Ports dialog, select the check box next to each port to add, then select **Save**.
    -   To add a new IP service, select **Add** &gt; **New IP services**. In the Add a new IP service dialog, complete the IP Service fields and select **Add**.
    To remove a port, select it and then select **Remove**.

7.  Select **Save**.

    Discovery collects certificates from devices that have one of the listed ports open during your IP-based Discovery schedules.


