---
title: Life-cycle operations in Cloud Provisioning and Governance
description: Operations like Start/Stop, Deprovision, and ExecuteScript are called life-cycle operations or day-2 operations. When you request a life-cycle operation on a stack or resource, the system generates a change request. An approval policy specifies either that the change is auto-approved or that a user on the approver list must approve the change.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Perform a life-cycle operation on a stack or resource, Manage a stack, Cloud User Portal, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Life-cycle operations in Cloud Provisioning and Governance

Operations like Start/Stop, Deprovision, and ExecuteScript are called life-cycle operations or day-2 operations. When you request a life-cycle operation on a stack or resource, the system generates a change request. An approval policy specifies either that the change is auto-approved or that a user on the approver list must approve the change.

To perform an operation, you select a stack or resource and then click **Select Stack Operation** or **Select Resource Operation**. The list includes only appropriate operations for the selected resource or stack. Some operations are provided by configuration management systems like Ansible or Terraform.

## Operations in the base system

-   **Start**

    The Start operation starts selected VM. The resource status changes to On.

    No setting is required.

-   **Stop**

    The Stop operation stops the selected VM. The resource status changes to Off.

    No setting is required.

-   **Deprovision**

    The Deprovision operation terminates the selected stack and sends a notification to the stack owner.

    No setting is required.


## Virtual Machine 'Store Extension Interface' operations

Only Google Cloud Platform and IBM Cloud support the Virtual Machine Store Extension Interface operations. The Terraform Connector ServiceNow Store app supplies the operations.

-   **Virtual Machine Store Extension Interface.ExecuteScript**

    The ExecuteScript operation runs a script on the selected Windows or Linux VM. For example, a script might install an application on a resource. See [KB0756431](https://support.servicenow.com/nav_to.do?uri=%2Fkb_knowledge.do%3Fsys_id%3Db37a29021b033748ada243f6fe4bcbda%26sysparm_record_target%3Dkb_knowledge%26sysparm_record_row%3D1%26sysparm_record_rows%3D1%26sysparm_record_list%3Dsys_created_by%253Djavascript:gs.getUserName()%255Eworkflow_stateNOT%2BINpublished%252Cobsolete%255EORDERBYDESCnumber) for detailed instructions.

    **Note:** To run the ExecuteScript operation, a VM must include credentials. Linux VMs inherit management key credentials when they are provisioned. For Windows VMs, use the InfuseKey operation to add credentials to the VM.

    In the pop-up, specify:

    -   **ScriptType**: Shell and PowerShell scripts are supported.
    -   **Script**: Name of the script.
-   **Virtual Machine Store Extension Interface.InfuseKey**

    For Windows VMs, the InfuseKey operation adds key credentials \(public and private key pair values\) to the VM.

    As a result, you can view the credentials on the Properties list of the Windows VM and can use the credentials to perform VM operations. For instructions on generating a key, see [Create an SSH key](../task/cloudmgt-create-ssh-key.md).

    To add key credentials to a Windows VM:

    1.  Select the Windows VM.
    2.  In the **Select Resource Operation** list, select **Virtual Machine Store Extension Interface.InfuseKey**.
    3.  In the pop-up, specify the key to use in the **UserKey** field and then click **OK**.
-   **Virtual Machine Store Extension Interface.Execute Job Template**

    Ansible supplies the Execute Job Template operation. The operation enables you to attach a node to an Ansible server and execute a package on that VME. For example, a script might install an application on a resource. In the pop-up, specify:

<table id="table_og2_t5f_rhb"><tbody><tr><td>

WorkloadConfigProviderType

</td><td>

 

</td></tr><tr><td>

WorkloadConfigProvider

</td><td>

 

</td></tr><tr><td>

Inventory

</td><td>

 

</td></tr><tr><td>

HostGroup

</td><td>

The list includes all possible applications \(called groups in Ansible\), not just the applications that the configuration management provider supports. Therefore, if users select an unsupported application, the provisioning fails.

</td></tr><tr><td>

ApplicationProfile

</td><td>

Select the application profile to execute on the selected resource.

</td></tr></tbody>
</table>    -   **ScriptType**: For Google Cloud Platform, **Shell** is supported.
    -   **Script**: Name of the script.
-   **Virtual Machine Store Extension Interface.Resize**

    The Resize operation changes the **Size** setting for a VM \(called **HardwareType** in the CI definition\). In the pop-up, specify the new size in the **HardwareType** field.

    ![Resize operation](../image/resize-operation-popup.png "Resize operation")


## 'Compute Security Group Store Extension Interface' operations

The Compute Security Group Store Extension Interface operations are supported for IBM Cloud only. The Terraform ServiceNow Store app supplies the operations.

-   **Compute Security Group Store Extension Interface.Deprovision**

    The Deprovision operation terminates the selected compute security group resource and sends a notification to the owner.

    No setting is required.

    The **Status** of the network interface changes to **Terminated**. In the Stack Health section of the home page, the status of the stack indicates that some resources are down.


## 'Load Balancer Store Extension Interface' operations

-   **Load Balancer Store Extension Interface.Deprovision**

    The Deprovision operation terminates the selected load balancer and sends a notification to the stack owner.

    No setting is required.

    The **Status** of the load balancer changes to **Terminated**. In the Stack Health section of the home page, the status of the stack indicates that some resources are down.


## 'Network Store Extension Interface' operations

-   **'Network Store Extension Interface.Deprovision**

    The Deprovision operation terminates the selected network store and sends a notification to the stack owner.

    No setting is required.

    The **Status** of the network store changes to **Terminated**. In the Stack Health section of the home page, the status of the stack indicates that some resources are down.


## 'Storage Volume Store Extension Interface' operations

The Storage Volume Store Extension Interface operations are supported for IBM Cloud only. The Terraform ServiceNow Store app supplies the operations.

-   **Storage Volume Store Extension Interface.Create Snapshot**

    The Create Snapshot operation generates a read-only copy of the specified volume.

    In the pop-up, specify the **SnapshotName** to use as the label for the snapshot.

    The snapshot is saved in the \[cmdbci.ci\_storage\_vol\_snapshot\_list\] table.

    If approval is not required, the system immediately takes the snapshot. If approval is required, there may be a delay while an admin approves the change. You receive email when the admin approves. After the admin approves, return to the VM Instance form and click the **Proceed with Change** related link.

    **Note:** If the VM is running, the VM is shut down at the start of the snapshot process and then restarted when the process finishes. The system auto-deletes the oldest snapshot when the **Snapshot eviction policy** limit is exceeded.

-   **Storage Volume Store Extension Interface.Restore From Snapshot**

    The Restore From Snapshot operation restores the image from the specified snapshot.

    Select the **SnapshotID** to use to restore the volume.

-   **Storage Volume Store Extension Interface.Delete Snapshot**

    The Delete Snapshot operation deletes the selected snapshot.

-   **Storage Volume Store Extension Interface.Attach**

    The Attach operation attaches a VM to the selected volume.

    1.  Select the volume to attach. The **Status** of the volume must be **Available**.
    2.  Select the **Storage Volume Store Extension Interface.Attach** operation.
    3.  In the **NodeId** field on the pop-up, select the **Instance ID** of the server to attach to the volume.

        The status of the volume changes from Available to In Use.

-   **Storage Volume Store Extension Interface.Detach**

    The Detach operation detaches a VM from the selected volume.

    1.  Select the volume to attach. The Status of the volume must be In Use.
    2.  Select the **Storage Volume Store Extension Interface.Detach** operation.
    3.  In the **NodeId** field on the pop-up, select the **Instance ID** of the host to detach from the volume.

        If this VM is the last or the only VM that is detached, then the status of the volume changes from In Use to Available.

-   **Storage Volume Store Extension Interface.Deprovision**

    The Deprovision operation terminates the selected volume and sends a notification to the stack owner.

    No setting is required.

    -   The billing item for the storage resource is removed.
    -   The **Status** of the volume changes to **Terminated**. In the Stack Health section of the home page, the status of the stack indicates that some resources are down.
    -   For IBM Cloud: The storage volume is available in the IBM Cloud Console for an extended period to enable the user to reclaim the storage volume.

