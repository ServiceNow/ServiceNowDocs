---
title: Configure the AWS WAF integration for mitigation controls monitoring
description: Determine if your virtual machines are protected with the AWS WAF integration for mitigation controls monitoring.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Exploit protection \(WAF\), Use mitigation controls, Security Posture Control, Security Operations]
---

# Configure the AWS WAF integration for mitigation controls monitoring

Determine if your virtual machines are protected with the AWS WAF integration for mitigation controls monitoring.

## Before you begin

Data is imported by two separate applications:

-   The Discovery and Service Mapping Patterns application imports the names and the default actions, allow or block, of the Web ACLs that you define in your AWS Service Account. The Discovery Pattern `Amazon AWS - Web ACL (LP)` is activated with the application.
-   The Mitigations Controls Monitoring application imports the actual Web ACL rules and the relationships between associated resources like an application load balancer. This extension is included as a part of the Mitigations Controls Monitoring application.

Verify you have completed the steps to define Web ACLs and rules and activated the required applications for the AWS WAF Integration described in [Exploit Protection \(WAF\) mitigation controls](../concept/spc-controls-policies-for-exploit-waf.md) prior to activating the applications.

Roles required:

-   admin for installation of plugins in your ServiceNow AI Platform® instance.
-   SPC Admin Group for configuration of integrations in the workspace.
-   AWS credentials for the AWS service account you want to use.

## Procedure

1.  Navigate to **All** &gt; **Security Posture Control Workspace** &gt; **Connectors and use cases setup** &gt; **SPC API Integrations tab**.

2.  Select the **AWS WAF** tile.

3.  Select one.

<table id="table_k5r_vyw_x2c"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**View service accounts**

</td><td>

View the available AWS service accounts that are configured in your instance.To create a new account:

1.  Select **View service accounts**.
2.  Select **New**.
3.  Fill in the fields.
    -   Name - Name of your AWS service account. This is the account you use for your Discovery schedule and credentials.
    -   Account id - Account ID for your AWS service account.
    -   Datacenter type - Select **AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]**
4.  Select **Submit**.


</td></tr><tr><td>

**Configure service account**

</td><td>

Configure an AWS service account in your instance.

</td></tr></tbody>
</table>4.  Create the Discovery schedule for the AWS service account you want to use.

    1.  Navigate to **All** &gt; **Discovery** &gt; **Home**.

    2.  Select **View Active Schedules**.

    3.  Select **Add Schedule**.

    4.  Select **Add Cloud Schedule** and fill in the fields.

<table id="table_i31_qcx_x2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider

</td><td>

AWS

</td></tr><tr><td>

Schedule name

</td><td>

Enter a unique name for your schedule to help you distinguish it from other AWS schedules.

</td></tr><tr><td>

Add Account

</td><td>

Select to create a Service Account.

</td></tr><tr><td>

Select Account

</td><td>

Select to edit an existing Service Account.

</td></tr><tr><td>

Account ID

</td><td>

Account ID for your AWS service account.

</td></tr><tr><td>

MID Selection Type

</td><td>

You must provide a MID Server. Select one:-   Auto-select MID Server
-   Specific MID Cluster
-   Specific MID Server
To import rules data for individual virtual machines with your MID Server, you must activate a MID Server property. To verify or set this property, navigate to **All** &gt; **MID Server** &gt; **Properties** &gt; **sn\_itom\_pattern.discover\_aws\_app\_pool\_members**. Set the Value to `true`.

</td></tr><tr><td>

Credentials

</td><td>

These are the Discovery credentials for your service account.

</td></tr><tr><td>

URL

</td><td>

 

</td></tr><tr><td>

Access Role Name

</td><td>

 

</td></tr><tr><td>

Select account for access

</td><td>

 

</td></tr></tbody>
</table>    5.  Select **Test Account**.

        You must have a successful validation before you can continue.

    6.  Select **Next**.

    7.  Select the datacenters you want to discover.

    8.  Select the **Discover VMs by IP address** toggle and select the MID Server you selected in step d from the list.

    9.  Select **Next**.

    10. Select how often and when you want to run your discovery.

    11. Select **Finish and Run**.

        After the discovery schedule you set has run, the discovery pattern **Amazon AWS - Web ACL \(LP\)** runs and the data from both applications is imported.


