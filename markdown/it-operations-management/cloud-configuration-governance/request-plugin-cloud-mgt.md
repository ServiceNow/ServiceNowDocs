---
title: Request the Cloud Provisioning and Governance application
description: The Cloud Provisioning and Governance application is available as a separate subscription and requires the Cloud Provisioning and Governance plugin \(com.snc.cloud.mgmt\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/cloud-configuration-governance/request-plugin-cloud-mgt.html
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Request the Cloud Provisioning and Governance application

The Cloud Provisioning and Governance application is available as a separate subscription and requires the Cloud Provisioning and Governance plugin \(com.snc.cloud.mgmt\).

## Before you begin

Role required: admin

## About this task

To purchase a subscription, contact your ServiceNow account manager. The account manager can arrange to have the plugin activated on your organization's production and subproduction instances, generally within a few days.

If you don't have an account manager, decide to delay activation after purchase, or want to evaluate the product on a subproduction instance without charge, follow these steps.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Select **Request plugin** to open the **Activate Plugin** form on Now Support.

3.  On the **Activate Plugin** form, provide the following information.

<table id="table_awx_bhf_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="target-instance"><td>

What is your target instance

</td><td>

Select the instance that you want to activate the plugin on.

</td></tr><tr><td>

Which plugin would you like to activate

</td><td>

Select the name of the plugin to activate.

 **Note:** If the plugin isn't listed, or if you're activating on an OEM or on-premise instance, select the **Plugin I'm looking for is not listed** check box. Enter the plugin name in the field that appears.

</td></tr><tr id="date-time"><td>

Select Maintenance Date and Time

</td><td>

Select the date and time to activate the plugin.

</td></tr></tbody>
</table>    For example, see the following form to activate the Event Management plugin on an instance named SNC Instance.

4.  Select **Submit**.

    After the maintenance window, the system installs the plugin on your instance. To confirm the installation, go to the Installed tab in the Application Manager.


**Related topics**  


[Day 1 setup guide for Amazon Web Services on Cloud Provisioning and Governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-configuration-governance/cloud-mgt-aws-setup-day-1.md)

[Day 1 setup guide for Microsoft Azure Cloud on Cloud Provisioning and Governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-configuration-governance/cloud-mgt-azure-setup-guide.md)

[Day 1 setup guide for Google Cloud through Cloud Services Catalog Terraform Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-configuration-governance/cloud-mgt-gcp-setup-day-1.md)

[Day 1 setup guide for VMware on Cloud Provisioning and Governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-configuration-governance/cloud-mgt-vmware-setup-guide.md)

