---
title: Create Azure policies for metric collection
description: Create your own policies to enable Azure to collect the metrics for the resources that have policies that don’t come with the base system. The Azure Metrics Collector check brings the metrics to the agent through the Azure Metrics Batch API.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configuring Agent Client Collector Monitoring, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Create Azure policies for metric collection

Create your own policies to enable Azure to collect the metrics for the resources that have policies that don’t come with the base system. The Azure Metrics Collector check brings the metrics to the agent through the Azure Metrics Batch API.

## Before you begin

-   Ensure that the configuration Items \(CIs\) that you want to collect the metrics for are included in the CMDB. CIs are typically populated during Discovery.
-   Ensure that the **sn\_agent.multi\_ci\_dev\_mode** property is set to **true** on the **System Properties** page \(**All** &gt; **System Properties** &gt; **All Properties**\).

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Policies**.

2.  Select **New**.

3.  Select the application scope icon ![Application scope icon.](../image/application-scope-icon.png) and verify that you are in the Agent Client Collector Monitoring scope.

4.  In the **Name** field, enter a name for the policy.

5.  Configure a filter that determines which CIs are to be monitored by the policy by selecting the **Monitored CIs** tab and the **Monitored CI type by filter** check box, as described in the following table.

<table id="table_jgt_rqc_nzb"><thead><tr><th>

Option

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Monitored CI type

</td><td>

Select the CI type to be monitored.The CI type must match the resource that you entered in the .json script file that contains the metrics to be monitored.

</td></tr><tr><td>

&lt;Filter fields&gt;

</td><td>

Configure the conditions that must be met for the resources in the specified Monitored CI type to be monitored.Ensure that you set the following conditions:

-   **Object ID** = &lt;name of the resource entered in the .json script file that contains the metrics to be monitored&gt;
-   **State** = Available

The Available state indicates that resources must be available to be monitored.

</td></tr><tr><td>

Preview

</td><td>

Select to view the number of resources that match the specified condition.The number of matching results appears next to the **Preview** button. Select the result to view all CI records that match the condition.

</td></tr></tbody>
</table>6.  Add the Azure Metrics Collector check to the policy.

    1.  On the **Checks** tab, locate the **Azure Metrics Collector** check in the **Available** cell.

    2.  Select the right arrow button to move the check to the **Selected** cell.

7.  Configure a proxy server to access the Azure metrics.

    1.  On the **Proxy Settings** tab, select **Single proxy agent**.

    2.  In the **Proxy agent** field, select the proxy agent to execute the policy and retrieve the Azure metrics.

8.  Configure the credentials for the policy.

    1.  Select the **Credentials** tab.

    2.  In the **Credential name** field, select the **azure\_metrics\_collector**.

9.  Select **Save**.

10. Add secure parameters to the check instance.

    1.  In the policy's **Check Instances** section, select the **Azure Metrics Collector** check instance.

    2.  On the **Check Secure Parameters** tab, select **New**.

    3.  Add the secure check parameters that are described in the following table.

        |Name|Order value|
        |----|-----------|
        |cred\_tenant\_id|1|
        |cred\_client\_id|2|
        |cred\_secret\_key|3|

        Ensure that the **Active** check box is selected for each parameter.

    4.  Select **Update**.

11. Add the `.json` configuration file to the check instance.

    The file sends the list of Azure resources to the agent.

    1.  Select the Azure Metrics Collector check instance.

    2.  Select the **Check Parameters** subtab.

    3.  Select **New**.

    4.  On the form, fill in the fields.

<table id="table_g5c_hf2_nzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for the `.json` file to be added to the instance's configuration files \(**Agent Client Collector** &gt; **Configuration Files**\).

</td></tr><tr><td>

Value

</td><td>

String that indicates the name of the `.json` file.For example: `acc_azure_vm_metrics_config.json`

</td></tr><tr><td>

Flag

</td><td>

Value that you enter \(**-c**\) to indicate that the check retrieves the name of the configuration file. The configuration file contains a namespace and a list of metrics. The value must indicate the name of the file that was uploaded to the list of configuration files \(**Agent Client Collector** &gt; **Configuration Files**\), in `.json` format. For example: `acc_azure_vm_metrics_config.json`.

</td></tr></tbody>
</table>        Ensure that the **Active**, **Mandatory**, and **Value required** check boxes are selected.

    5.  Select **Submit**.

12. Create a `.json` file that indicates the metrics that you want your policy to monitor.

    The following example displays a `.json` file for retrieving load-balancer metrics.

    ![Azure metrics .json file.](../image/azure-metrics-json.png)

    Add the `.json` file to the list of configuration files at **Agent Client Collector** &gt; **Configuration Files**.

13. Create a .json file to indicate the resources that you want your policy to monitor.

    1.  On the **Proxy Settings** tab, select **Multi-CI Mode**.

    2.  Copy a script from one of the Azure cloud policies that comes with the base system.

        -   Cloud policies that come with the base system are described in [Create Azure policies for metric collection](create-policies-azure.md).
        -   The script is located in the **Config file creation script** field of the policy's **Proxy Settings** tab.
    3.  Paste the script into the **Config file creation script** field of your policy.

    4.  At the end of the script, configure the **resource\_id**, **region**, and **sys\_id** parameters with the values of the CI that you want the policy to monitor.

14. Select **Save** and then publish the policy by selecting **Publish**.


## Result

The configured policy retrieves the resources and their metrics from the specified Azure CI and sends them to the agent.

