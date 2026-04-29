---
title: Create the credential and service account that will access your VMware data
description: To securely access data on your provider account, the Discovery process must present appropriate credentials. To make the credentials available to Discovery, you first create an account in the VMware Console. You then securely store the credentials in a service account in your instance.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Day 1 setup guide for VMware on Cloud Provisioning and Governance, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create the credential and service account that will access your VMware data

To securely access data on your provider account, the Discovery process must present appropriate credentials. To make the credentials available to Discovery, you first create an account in the VMware Console. You then securely store the credentials in a service account in your instance.

## Before you begin

Roles required:

-   VMware Console administrator
-   Cloud Provisioning and Governance: admin or sn\_cmp.cloud\_admin

## About this task

Cloud providers often use different names for accounts, regions, and credential settings. Because the ServiceNow application supports several cloud providers, the app uses general-purpose names for the settings.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Credentials**.

2.  On the **Credentials** tab, click **New**, select **VMware Credentials**, fill in the form, and then click **Submit**.

    |Field|Input value|
    |-----|-----------|
    |Name|Unique and meaningful name for the credentials \(for example, `Cloud Management VMware Credentials`\`\).|
    |Active|Select the check box to enable the credential for use.|
    |User name|User name for access to your vSphere account.|
    |Password|Password for access to your vSphere account.|

3.  Navigate to **Cloud Admin Portal** &gt; **Manage** &gt; **Service Accounts**, click **New**, enter a unique and meaningful **Name** \(for example, `Cloud Provisioning Service Account`\), and then fill in the form.

<table id="table_f43_sps_tdb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Account ID

</td><td>

There are two methods for determining the value:-   If you have access to the managed object browser for the vCenter \(MOB\): The Account ID is the instance UUID. Open the MOB and then click **Content** &gt; **About**. Paste the value of the **instanceUuid** property in the **Account ID** field.
-   If you do not have access to the MOB, enter a temporary alphanumeric text such as `5ca3033a-1290-4a02-8221-2c5f2f29be8b` in the **Account ID** field. In a step that follows this table, you create the actual value and then return to this form to replace the temporary text with the actual value.


</td></tr><tr><td>

Discovery credentials

</td><td>

Name of the credentials that you created in the preceding step. `Cloud Provisioning VMware Credentials` in the example.

</td></tr><tr><td>

Datacenter URL

</td><td>

Full URL of the vCenter, for example: `https://<IP address>/sdk`.

</td></tr><tr><td>

Datacenter Type

</td><td>

Select **VMware vCenter datacenter \[cmdb\_ci\_vcenter\_datacenter\]**.

</td></tr><tr><td>

Datacenter discovery status

</td><td>

Auto-generated value: Status and timestamp of the last execution of Discovery on the datacenter.

</td></tr><tr><td>

**Should pull events**

</td><td>

Enables Cloud Provisioning and Governance to collect events from resource types in VMware vCenter datacenter in the `sn_cmp_cloud_event_list`.

</td></tr></tbody>
</table>4.  Click the **Discover Datacenters** related link.

    Using the credential, Discovery accesses the vCenter at the specified URL to discover VMware datacenters.

5.  If you used the instance UUID value in the **Account ID** field, click **Submit** and skip the remaining steps in this procedure.

    The system creates the service account and displays the list of all service accounts.

6.  On the Cloud Admin Portal, navigate to **Operate** &gt; **Trails**.

7.  On the **Cloud API Trail** tab, find the entry with the **Method name** value of **ListDatacenters** and **Provider name** value of **vmware-compute** \(typically the most-recent entry\).

    Open the entry.

8.  On the **CAPI Trail Logs** related list, open the **route\_result** entry.

9.  In the **Log value** text box, copy the **locationId** value.

    This value is the **Account ID** that you will paste into the form in the next step.

    ![Copy the locationId so you can paste it into the form](../image/locationId-on-capi-trail.png)

10. On the instance, navigate to **Cloud Admin Portal** &gt; **Manage** &gt; **Service Accounts** and then click the service account that you created earlier \(`Cloud Provisioning Service Account` in the example\).

11. Paste the **locationId** value \(that you copied from the **CAPI Trail Log** form\) in the **Account ID** field on the form and then click **Update**.

12. Click **Submit**.

    The system creates the service account and displays the list of all discovered datacenters.


**Related topics**  


[Discovery for VMware](../../discovery/concept/vmware-cloud-discovery.md)

