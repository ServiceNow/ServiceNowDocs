---
title: Store the Azure service principal credentials in the instance
description: To securely access data on your provider account, the Discovery process must present appropriate credentials. To make the credentials available to Discovery, you first create Azure service principal credentials in the Azure Portal. You then securely store the credentials in a service account in your instance.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Day 1 setup guide for Microsoft Azure Cloud on Cloud Provisioning and Governance, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Store the Azure service principal credentials in the instance

To securely access data on your provider account, the Discovery process must present appropriate credentials. To make the credentials available to Discovery, you first create Azure service principal credentials in the Azure Portal. You then securely store the credentials in a service account in your instance.

## Before you begin

Role required:

-   Azure Portal Active Directory \(AD\) administrator
-   Cloud Provisioning and Governance: admin or sn\_cmp.cloud\_admin, discovery\_admin

## Procedure

1.  [Create a Microsoft Azure service principal](azure-create-serv-princ-cloud-mgt-1.md) and open the text file that you created during the procedure.

2.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Credentials**.

3.  Click **New** and then select **Azure Service Principal**.

4.  Specify the following values on the Azure Service Principal form:

<table id="table_m3f_bqm_wcb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the service principal to register with the instance. For example, `Azure service principal credentials`.

</td></tr><tr><td>

Authentication Method

</td><td>

Select **Client Secret**.The **Secret key** field appears when you select **Client Secret**.

 **Note:** **Client Assertion** is not supported.

</td></tr></tbody>
</table>5.  Copy/paste values from the `Azure-Credentials.txt` text file into the remaining fields.

    ![Azure credentials](../../discovery/image/azure-copy-to-service-principal.png)

6.  Select the appropriate **EA credential** from the list, select the **Active** check box, and then click **Save** to create the record.

7.  Click the **Discover Subscriptions** related link to find all subscriptions that are associated with the Azure service principal.

    The instance creates a service account for each discovered subscription.The **Azure Subscriptions** related list displays all subscriptions that are associated with the Azure service principal.

8.  Click a subscription to view the service account that was created for the subscription.

9.  Click a discovery status entry in the **Credential Discovery Status** list to view the associated discovery log.

    Each time that you click **Discover Subscriptions**, the instance generates a new discovery status and lists the status in the **Credential Discovery Status** list.


