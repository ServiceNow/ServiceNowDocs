---
title: Configure client software distribution providers
description: Identify the provider and specify the flows, subflows. and extension points for a customized software distribution process.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CSD extension framework, Client Software Distribution, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure client software distribution providers

Identify the provider and specify the flows, subflows. and extension points for a customized software distribution process.

## Before you begin

Perform the development tasks described in the CSD Extension Implementation Guide before attempting this procedure.

Role required: sn\_client\_sf\_dist.csd\_admin, admin

## Procedure

1.  Navigate to **All** &gt; **Client Software Distribution** &gt; **Extensions** &gt; **Providers**.

2.  Click **New**.

3.  Complete the form using the fields in the table.

    ![Provider information for Casper integration](../images/CasperProvider.png)

    |Field|Description|
    |-----|-----------|
    |Name|Descriptive name of the provider.|
    |Provider server|Table name of the provider server. You must create this table as an extension of the Configuration Item \[cmdb\_ci\] table. For example, you might call your table Casper Server Instance \[cmdb\_ci\_casper\_server\_instance\].|
    |Discover And Store SCCM Data subflow|Subflow that discovers the provider server and returns the data from that server back to the instance. This is the subflow you create with custom activities that query the provider server.|
    |Software configuration|Table name of the software configuration for this provider. You create this table as an extension of the Client Software Distribution Software Configuration \[sn\_client\_sf\_dist\_software\_config\] table. For example, you might create a table called Casper Software Configuration \[sn\_client\_sf\_dist\_casper\_sf\_config\].|
    |Deployment extension key|The **SetDeploymentData** key provided with CSD. This key sets up the data for the software ordering and deployment flow.|
    |Deploy Client Software flow|Flow that deploys software from the provider server. This is the flow you created with custom activities that tells the provider where to deploy an application requested from the service catalog.|
    |Revocation extension key|The **SetRevocationData** key provided with CSD. This key sets up the data for installation revocation.|
    |Revoke SCCM Application subflow|Subflow that revokes an installation from a provider server. This is the subflow you created with custom activities that tells the provider which application to remove from a device.|


**Parent Topic:**[Client software distribution extension framework](../concept/csd-ext-framewrk.md)

