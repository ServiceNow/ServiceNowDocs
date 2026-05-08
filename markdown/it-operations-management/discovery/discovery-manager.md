---
title: Create Discovery schedules for cloud resources
description: Create schedules for discovering cloud resources using service accounts or IP ranges.Specify your cloud provider and select the service account to discover. You can include one or all available sub-accounts on a schedule. Provide the credentials for the cloud service account and test the connection. Cloud Discovery displays the list of available datacenters when you validate the service account. Specify which datacenters you want to discover through the schedule.You can discover virtual machines \(VMs\) during discovery of the cloud resources. Cloud Discovery performs a deep discovery of the virtual machines identified by the cloud schedule, using the IP addresses of the VMs.The final phase in the Discovery Manager wizard creates the schedule that triggers discovery of the cloud resources.Configure the Cloud Discovery to auto-refresh the list of sub-accounts and datacenters before each scheduled discovery. If Cloud Discovery identifies any new sub-accounts or datacenters, it adds them to the Configuration Management Database \(CMDB\) and includes them in the discovery schedule.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-27"
reading_time_minutes: 13
breadcrumb: [Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Create Discovery schedules for cloud resources

Create schedules for discovering cloud resources using service accounts or IP ranges.

## Discovery Manager interface

Use the Cloud Discovery Schedule Configuration interface to input the information that you need to access your service accounts and sub-accounts. You can specify the credentials to validate the selected accounts. Test the connections to your accounts and then create schedules to discover the cloud resources in your selected datacenters.

The following private and public cloud platforms support VMware Discovery:

-   Alibaba Cloud
-   Amazon Web Services \(AWS\)
-   Google Cloud Platform \(GCP\)
-   IBM Cloud
-   Microsoft Azure
-   OpenStack
-   Oracle Cloud Infrastructure \(OCI\)
-   oVirt
-   VMware

**Note:** The term "sub-accounts" is used generically in the Cloud Discovery Schedule Configuration interface. Its meaning varies by cloud provider:

-   In AWS, sub-accounts refer to member accounts under a management account.
-   In Microsoft Azure, the equivalent is a subscription.
-   In Google Cloud Platform \(GCP\), Cloud Discovery targets projects.

Progress indicator

As you complete each configuration phase, the tabs at the top of the Discovery Manager track your progress. A check mark indicates a completed phase. A dark underline marks the current phase. The tabs are interactive, you can move to a phase by clicking that tab.

![Discovery Manager progress indicator](../image/CloudDiscoProgressBar.png)

## Discovery Manager label customization

The Service Account Field Options \[service\_account\_field\_options\] table contains fields to modify the labels in Discovery Manager. These fields enable you to customize the Discovery Manager to handle new service providers or to alter existing labels to meet internal policies. For example, the Microsoft Azure account ID label is Microsoft Azure Subscription GUID by default. You can change it to Subscription ID, Account ID, or anything else based on your needs.

## Select a service account and test your credentials

Specify your cloud provider and select the service account to discover. You can include one or all available sub-accounts on a schedule. Provide the credentials for the cloud service account and test the connection.

### Before you begin

Before you attempt to configure Cloud Discovery, you must have at least one validated MID Server with a status of **Up**. The MID Server must reach the IP ranges that you intend to discover. You can install the MID Server by using Use MID Server guided setup or by manually downloading and running the installer. For details, see the MID Server installation instructions for Linux and Windows. Ensure to configure the MID Server used for Cloud Discovery with the Cloud Management capability.

Role required: discovery\_admin

### About this task

The ServiceNow® Cloud Discovery wizard begins with the account selection and testing phase. To prevent long waits or unexpected timeouts, use the **cdu.record.watcher.timeout** system property to define the maximum waiting period for these Cloud Discovery configuration processes:

-   Service account validation
-   Member account discovery
-   Discovery of logical datacenters

The default timeout value is 300000 milliseconds or 5 minutes.

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Home**.

2.  Select **Discover Cloud Resources** in the Welcome screen.

    **Note:** The Welcome screen contains a link to the [Discovery Quick Start](discovery-quick-start.md#). This wizard is designed to quickly set up a basic Discovery. You can use Quick Start to evaluate Discovery or to explore new network devices, but the guide is not intended for discovering cloud resources.

    If the system cannot detect an appropriate MID Server, you're prompted to install and configure a MID Server by using the MID Server Guided Setup. This notification is also displayed if an existing MID Server is not available because it is upgrading.

    ![MID Server setup link](../image/QS_NoMIDFound2.png)

3.  In the Basic Info pane of the Discovery Manager, select the name of your cloud provider in the **Provider** field, such as **AWS** or **Azure**.

    The wizard displays a count of the validated and available MID Servers in the MID Servers pane.

4.  If you're using AWS, Azure, GCP, or Alibaba Cloud you can specify the MID Server selection type in the **MID Selection Type** field.

    **Note:** AWS and Azure selection is only available after migration to pattern-based Discovery. For more information, see [Migrate from CAPI to Patterns](../task/migrate-from-capi-to-pattern.md).

    The following options are available:

    -   **Auto-Select MID Server**: The wizard automatically uses an appropriate MID Server.
    -   **Specific MID Server**: The wizard uses the MID Server specified in the **MID Server** field. To filter and view MID Servers that are configured to assume an IAM role for discovering cloud resources, select the **Credential-Less Discovery** option.
    ![MID server selection.](../image/MIDSelection.png)

5.  If no MID Server has the Cloud Management capability, select **Configure MID Servers** and configure one appropriately.

    1.  Navigate to **MID Servers** &gt; **Capabilities**.

    2.  From the MID Server Capabilities list, select **Cloud Management**.

        You can also select **ALL**, which includes Cloud Management by default.

    3.  In the MID Servers related list, select **Edit** and then add your MID Servers to the capability.

    4.  Select **Save**.

        Your MID Servers are ready to communicate with your cloud service accounts.

6.  In the **Schedule Name** field, enter a unique and descriptive name for the schedule.

7.  In the Service Account pane, choose whether you want to add an account or select an existing account.

    If you select an existing account, the system auto-completes the form with the available information. If you add an account, you must provide the account ID, credentials, and URL, if applicable. For VMware, you must specify the URL.

    -   The [AWS account ID](../../cloud-management-v2-setup/task/aws-first-cld-and-srvc-accts.md) is the account ID.
    -   The [Azure account ID](../../cloud-management-v2-setup/task/azure-service-account-cloud-mgt.md) is the Azure Subscription GUID.
    -   The [GCP account ID](../../cloud-management-v2-setup/task/gcp-first-cld-and-srvc-accts.md) is the project ID.
    -   The [VMware account ID](../../cloud-management-v2-setup/task/vmware-create-creds-cloud-mgt.md) is the virtual machine instance UUID.
    -   The [Alibaba Cloud account ID](../task/set-up-alibaba-cloud-service-account.md) is the Compartment ID.
    **Note:** VMware discovery can run without a service account. To discover VMware resources, configure the schedule to run on the IP address of the vCenter server.

8.  Select the credentials for this cloud service account or add new credentials.

    1.  To add a credential, select the plus icon \(**+**\).

    2.  Select the appropriate cloud credential type from the list.

    3.  Complete the form and select **Save**.

        **Note:** You can configure AWS to generate temporary credentials for service accounts. This capability eliminates the need to define some credentials on the instance, and it can increase security on your member accounts \(sub-accounts\). For details, see [Access setup for AWS service accounts](../../it-operations-management/concept/access-aws-accounts.md).

9.  To validate the account with the provided details, select **Test Account**.

    Messages in the header bar notify you of the validation results. If you specified a management account and the connection test was successful, then the wizard displays a selection screen for any members accounts \(sub-accounts\) that are associated with the management account. By default, all current member accounts are selected for the schedule and cannot be moved to the Available list.

    **Note:**

    If the validation process does not return any sub-accounts or any sub-accounts that you added recently, select **Refresh Members** or rerun the validation process. If validation times out repeatedly, increase the timeout interval in the **cdu.record.watcher.timeout** MID Server property.

    ![Selecting what sub-accounts to include in the schedule.](../image/CloudDiscoSubAccounts.png)

10. To select specific sub-accounts for the schedule, deactivate the auto-select feature.

    By default, all sub-accounts are selected. To disable the feature and to permit the selection of specific datacenters to discover, slide the toggle switch to the left.

    ![Disabling the auto-select feature for sub-accounts.](../image/CloudDiscoDeselectSubAccounts.png)

11. To exclude a sub-account, drag the sub-account from the Selected list to the Available list.

12. Select **Next**.


## Select a cloud provider datacenter to discover

Cloud Discovery displays the list of available datacenters when you validate the service account. Specify which datacenters you want to discover through the schedule.

### Before you begin

Role required: discovery\_admin

### Procedure

1.  To select the datacenters to discover, click the **Select Datacenters** phase in the Discovery Manager tab bar.

    By default, all datacenters associated with the service account are selected for the Cloud Discovery schedule.

    **Note:**

    -   If no datacenters appear, select **Refresh Datacenters** or re-run the account validation. If validation times-out repeatedly, increase the timeout interval in the **cdu.record.watcher.timeout** MID Server property.
    -   You can configure Cloud Discovery to auto-refresh the list of sub-accounts and datacenters before each scheduled discovery. For more information, see [Enable auto-refreshing of sub-accounts and datacenters](discovery-manager.md#).
2.  To select specific datacenters for the schedule, deactivate the auto-select feature by moving the **Discover all datacenters listed below** toggle switch to the left.

3.  Move the datacenters you want to discover from the **Available** list to the **Selected** list.

4.  Select the next phase in the tab bar.

    If required, you can configure IP ranges to discover virtual machines \(VM\), or move to the schedule phase and complete Cloud Discovery setup.


## Enable discovery of virtual machines

You can discover virtual machines \(VMs\) during discovery of the cloud resources. Cloud Discovery performs a deep discovery of the virtual machines identified by the cloud schedule, using the IP addresses of the VMs.

### Before you begin

All MID Servers you intend to use for Cloud Discovery must be validated, have a status of **Up**, and they can access the IP ranges in the cloud provider account.

**Important:** The upgrade process from Madrid to New York deactivates the existing Cloud Discovery schedules. Ensure to re-activate any schedules in the Discovery Manager that might have been deactivated during an upgrade from Madrid . These schedules have a **Run** status of **undefined** in the Discovery Schedule \[discovery\_schedule\] table.

Role required: discovery\_admin

### About this task

You do not need to configure IP ranges for the MID Servers used with Cloud Discovery. Cloud Discovery automatically selects the IP addresses of the virtual machines in the datacenters you selected in the wizard.

### Procedure

1.  To discover the VMs that are part of the current schedule, click the **Discover Virtual Machines \(optional\)** phase in the Discovery Manager tab bar.

    By default, VM discover is active.

    **Note:** To learn more about the working of **Discover Virtual Machines \(optional\)** in Cloud Discovery, see the KB article [How does the "Discover Virtual Machine" \(optional\) work in Cloud Discovery](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0870860).

2.  Select the MID Server to use.

    The following options are available:

    -   **Auto-Select**: Discovery selects an appropriate MID Server automatically.
    -   **Specific MID Cluster**: Discovery uses the named MID Server cluster.
    -   **Specific MID Server**: Discovery uses the named MID Server.
    ![Configure VMs to discover](../image/CloudDiscoVMs.png)

3.  To disable VM discovery, move the **Discover VMs by IP address** toggle switch to the left.

    The **MID Selection Type** field disappears.

4.  Select the **Create Schedule** phase in the tab bar.


## Set the run time for a Cloud Discovery schedule

The final phase in the Discovery Manager wizard creates the schedule that triggers discovery of the cloud resources.

### Before you begin

Role required: discovery\_admin

### About this task

You can also access the schedule phase of the Discovery Manager from the Discovery Schedule form. Navigate to **Discovery** &gt; **Discovery Schedules** and select **Cloud Discovery** in the schedules list.

### Procedure

1.  To configure the Cloud Discovery schedule, select **Create Schedule** in the Discovery Manager tab bar.

    By default, the schedule is active.

2.  Configure when and how often the schedule should run and define a timeout threshold if you want to restrict Cloud Discovery to a specific duration.

    ![Cloud Discovery schedule](../image/CloudDiscoSchedule.png)

3.  To deactivate the schedule, toggle the **Active** switch to the left.

4.  Complete the Cloud Discovery scheduling process by selecting one of the following options:

    -   **Finish and Run**: Runs Discovery immediately, using the current configuration. All subsequent cloud discoveries run on the schedule you provided.
    -   **Finish**: Exits the wizard and runs Cloud Discovery on the schedule you provided.

### What to do next

Open the [Discovery Home page](discovery-home-page.md#) or [Discovery Admin Workspace Schedules](discovery-admin-workspace-schedules.md#) page and view the results of your Discovery.

## Enable auto-refreshing of sub-accounts and datacenters

Configure the Cloud Discovery to auto-refresh the list of sub-accounts and datacenters before each scheduled discovery. If Cloud Discovery identifies any new sub-accounts or datacenters, it adds them to the Configuration Management Database \(CMDB\) and includes them in the discovery schedule.

### Before you begin

Role required: discovery\_admin

### About this task

Cloud Discovery can automatically refresh the list of sub-accounts and datacenters covered in a discovery schedule, subject to the fulfilment of the following criteria:

-   The cloud provider is Amazon Web Services \(AWS\), Microsoft Azure, or Google Cloud Platform \(GCP\)
-   The **glide.discovery.cdu.auto\_refresh\_sub\_accounts\_and\_ldcs** property to `true`.
-   The Cloud Discovery schedule is created for a management account.
-   The Cloud Discovery schedule is configured to discover the resources of all the sub-accounts and datacenters of the management account.

**Note:** The term "sub-accounts" is used generically in the Cloud Discovery Schedule Configuration interface. Its meaning varies by cloud provider:

-   In AWS, sub-accounts refer to member accounts under a management account.
-   In Azure, the equivalent is a subscription.
-   In Google Cloud Platform \(GCP\), Cloud Discovery targets projects.

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Search for the following system property record, and then open the record.

    **glide.discovery.cdu.auto\_refresh\_sub\_accounts\_and\_ldcs**

3.  On the form, change the Value field to `true`.

4.  Select **Update**.


