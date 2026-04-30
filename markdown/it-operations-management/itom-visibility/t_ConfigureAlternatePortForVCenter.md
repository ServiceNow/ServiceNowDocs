---
title: Configure an alternate port for vCenter
description: You can specify an alternate port for the VMware - vCenter Datacenters probe.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2025-12-02"
reading_time_minutes: 1
keywords: [Configure vCenter, configure port vCenter]
breadcrumb: [Discovery for VMware vCenter, Discovery for VMware virtualization, Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Configure an alternate port for vCenter

You can specify an alternate port for the VMware - vCenter Datacenters probe.

## Before you begin

Role required: admin

## About this task

By default, vCenter discovery is initiated on these ports:

-   **vmapp6\_https**: 9443
-   **vmapp\_https**: 5480

When these ports are detected, the VMWare - vCenter Datacenters probe is triggered.

## Procedure

1.  Hard code the port information.

    1.  Navigate to **All** &gt; **Configuration** &gt; **VMware** &gt; **vCenter**.

    2.  Select the specific instance from the list of instances.

    3.  Edit the **URL** field to include the port.

        For example, `https://10.0.0.1:444`

    4.  Select **Update**.

2.  Specify an alternate port number for vCenter in the VMWare - vCenter Datacenters probe.

    1.  Navigate to **All** &gt; **Discovery Definition** &gt; **Probes**.

    2.  Open the **VMware - vCenter Datacenters** probe record.

    3.  In the **Probe Parameters** related list, select **New**.

    4.  In the **Name** field of the Probe parameter record, enter `vcenter_port`.

    5.  In the **Value** field, enter your alternate port number.

    6.  Select **Submit**.

3.  Activate the VMWare - vCenter Classify probe.

    **Important:** This configuration is only required when vCenter is on port 443.

    1.  Navigate to **All** &gt; **Discovery Definition** &gt; **Port Probes**.

    2.  Open the **http** port probe record.

    3.  In the **Trigger Probes** related list, select the **false** link for the **VMWare - vCenter Classify** classification probe.

    4.  Select the **Active** check box.

    5.  Select **Update**.

        The VMWare - vCenter Classify probe attempts to establish a connection between the MID Server and the vCenter instance. If the connection is successful, it triggers the VMWare - vCenter Datacenters probe.


**Parent Topic:**[Discovery for VMware vCenter](../concept/c_DiscoveryForVMwareVCenter.md)

