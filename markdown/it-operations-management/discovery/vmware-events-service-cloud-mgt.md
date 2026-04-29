---
title: Configure the VMware Events service to auto-update the CMDB
description: Configure events from the cloud environment to make the necessary updates to your CMDB without additional scanning. The VMware Events service can auto-update CI data in the CMDB whenever Cloud Provisioning and Governance makes a life-cycle state or configuration change to a VMware resource. As a result, the CI data in the CMDB is updated without having to wait for Discovery to run.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Discovery for VMware, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure the VMware Events service to auto-update the CMDB

Configure events from the cloud environment to make the necessary updates to your CMDB without additional scanning. The VMware Events service can auto-update CI data in the CMDB whenever Cloud Provisioning and Governance makes a life-cycle state or configuration change to a VMware resource. As a result, the CI data in the CMDB is updated without having to wait for Discovery to run.

## Before you begin

**Important:** You can configure the VMware event service to auto-update the CMDB for event-based discovery or configuration changes even if you haven't subscribed to and activated the Cloud Provisioning and Governance plugins.

-   You must have a cloud account with VMware, service accounts and associated logical datacenters.
-   The following Cloud Provisioning and Governance plugins must be activated \(Not mandatory for Cloud Discovery\):
    -   Cloud Provisioning and Governance \(com.snc.cloud.mgmt\)
    -   Cloud Provisioning and Governance Core \(com.snc.cloud.core\)
    -   Cloud API \(com.snc.cloud.api\)
    -   Cloud Config Management \(com.snc.config.mgmt\)
-   A MID Server must be available with **All** or **VMware** capabilities.
-   The vCenter datacenters are successfully discovery and associated data is populated.

Role required: sn\_cmp.cloud\_event\_integration

## About this task

When VMware Events sends an update, the instance processes the event and creates or updates the CI entry in the CMDB and the CI information in the Cloud User Portal. Each event is saved as a record in the Events table on your instance. Configure all event/alert rules from the vCenter.

To connect to a different MID Server or vCenter: Update the settings and then click the **Start** related link. The **Status** value changes to **Updating** and then to **Started**.

**Important:**

If you are on a domain separated instance, only those events that are updated to the CMDB and belong to your domain are visible. Events create configuration items \(CI\) in the same domain as the cloud service account they are mapped to. Events that are not associated to a service account are visible to all domains.

During event processing, the Cloud Event Scheduler identifies the domain of the service account and assigns to the event. If an error occurs in identifying the domain before processing, the event can sometimes stay unassigned and become visible to all domains. To prevent the failed events visibility to all domains, you can set the **sn\_cmp.error\_events.default\_domain** property to sys\_id of the service-provider domain so that the failed events appears only to the service-provider domain administrator.

## Procedure

1.  Navigate to the VMware Alert Configuration in one of the following ways:

    -   Use the `https://baseURL/ecc_agent_ext_context_vcenter` to navigate directly using the URL.
    -   On the **Cloud Admin Portal**, navigate to **Manage** &gt; **Alert Configurations**.
2.  On the **VMware** tab, click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|A unique name for the Event Collector record.|
    |Short description|A brief description of the record.|
    |Execute on|Select **Specific MID Server**|
    |MID Server|Select a MID Server.|
    |vCenter|Select the vCenter to monitor.|
    |Extension \[read only\]|The MID Server extension of this context. Updated when data collection starts.|
    |Status \[read only\]|The status of the data collection process, for example, Starting, Started, and so on.|
    |Executing on \[read only\]|The MID Server that is executing the event collector|

4.  Right-click in the header and select **Save**.

5.  Test the connection between the vCenter and the MID Server: Click **Test parameters**.

    A pop-up displays **Parameters verified** for success. The **Status** field does not change. To update a parameter \(for example, to change the MID Server or vCenter\), change the setting and then click **Update parameters**.

6.  Click the **Start** related link to start collecting events for vCenter.

    -   To confirm that the instance is receiving events, verify that the **Status** field displays **Started**.
    -   Click **Stop** to stop collecting events for a particular vCenter.
    -   Click **Restart** to restart event collection.
    vCenter events are being populated in **sn\_cmp\_cloud\_event** table.


## Result

-   If the vCenter has events in the Event Manager and the same events are configured, Cloud Provisioning and Governance gathers the events and take action on the CIs accordingly.
-   Identification and Reconciliation Engine \(IRE\) changes the CI state based on event payload received and the IRE cannot be customized.

