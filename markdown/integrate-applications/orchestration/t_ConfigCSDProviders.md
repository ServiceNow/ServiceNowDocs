---
title: Configure client software distribution providers
description: Identify the provider and specify the workflows and extension points for a customized software distribution process.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Client software distribution extension framework, Client Software Distribution, Orchestration applications, Classic Orchestration, Workflow Data Fabric]
---

# Configure client software distribution providers

Identify the provider and specify the workflows and extension points for a customized software distribution process.

## Before you begin

Perform the development tasks described in the CSD Extension Implementation Guide before attempting this procedure.

Role required: sn\_client\_sf\_dist.csd\_admin, admin

## Procedure

1.  Navigate to **All** &gt; **Client Software Distribution** &gt; **Extensions** &gt; **Providers**.

2.  Click **New**.

3.  Complete the form using the fields in the table.

    ![Provider information](../../../administer/integrationhub/images/sccm-provider-ihub.png)

<table id="table_hsl_qkt_nv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name of the provider.

</td></tr><tr><td>

Provider server table

</td><td>

Table name of the provider server. You must create this table as an extension of the Configuration Item \[cmdb\_ci\] table. For example, you might call your table Casper Server Instance \[cmdb\_ci\_casper\_server\_instance\].

</td></tr><tr><td>

Discovery flow

</td><td>

Flow that discovers the provider server and returns the data from that server back to the instance. This is the flow you create with custom activities that query the provider server.

</td></tr><tr><td>

Software configuration table

</td><td>

Table name of the software configuration for this provider. You create this table as an extension of the Client Software Distribution Software Configuration \[sn\_client\_sf\_dist\_software\_config\] table. For example, you might create a table called Casper Software Configuration \[sn\_client\_sf\_dist\_casper\_sf\_config\].

</td></tr><tr><td>

Deployment extension key

</td><td>

The **SetDeploymentData** key provided with CSD. This key sets up the data for the software ordering and deployment workflow.

</td></tr><tr><td>

Deployment flow

</td><td>

Flow that deploys software from the provider server. This is the flow you created with custom activities that tells the provider where to deploy an application requested from the service catalog.

</td></tr><tr><td>

Revocation extension key

</td><td>

The **SetRevocationData** key provided with CSD. This key sets up the data for installation revocation.

</td></tr><tr><td>

Revocation flow

</td><td>

Flow that revokes an installation from a provider server. This is the flow you created with custom activities that tells the provider which application to remove from a device.

</td></tr><tr><td>

Use Flow

</td><td>

Option to use Integration Hub flows for client software distribution. When this option isn't selected, Orchestration workflows are used for client software distribution.**Note:**

</td></tr></tbody>
</table>
**Parent Topic:**[Client software distribution extension framework](../concept/c_CSDExtensionFramework.md)

