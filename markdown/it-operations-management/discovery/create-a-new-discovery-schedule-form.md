---
title: Create a new discovery schedule form reference
description: The Create a new discovery schedule form displays information related to the schedule and the target cloud provider. The Create a new discovery schedule form is available in the Cloud Discovery Workspace.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Discovery reference, Discovery, ITOM Visibility, IT Operations Management]
---

# Create a new discovery schedule form reference

The Create a new discovery schedule form displays information related to the schedule and the target cloud provider. The Create a new discovery schedule form is available in the Cloud Discovery Workspace.

For instructions on this procedure, see [Create a discovery schedule in Cloud Discovery Workspace](../task/cloud-operations-disco-create-schedule.md).

<table id="id_uym_wnr_gwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Discovery schedule name

</td><td>

Name of the discovery schedule.

</td></tr><tr><td>

Cloud provider

</td><td>

Name of the cloud provider that hosts the resources you want to discover.

</td></tr><tr><td>

MID selection types

</td><td>

MID Server or MID cluster that you want to use to discover the cloud resources.The following options are available:

-   Auto-Select MID Server: Discovery automatically selects an appropriate MID Server.
-   Specific MID Cluster: Discovery uses the MID cluster specified in the MID cluster field.
-   Specific MID Server: Discovery uses the MID Server specified in the MID Server field.

If the selected MID Server is a part of a MID cluster, the jobs are equally distributed among all the MID Servers of that cluster.


 This field appears only when one of the following values is selected from the cloud provider field:

-   AWS
-   Azure
-   Google
-   Alibaba Cloud

</td></tr><tr><td>

MID clusters

</td><td>

MID clusters you want to use with the Cloud Discovery schedule.This field appears only when the Specific MID Cluster value is selected from the MID selection types field.

</td></tr><tr><td>

Credential-less discovery

</td><td>

Option to use credential-less discovery.To view and filter the MID Servers that can assume an IAM role to discover the cloud resources, move the **Credential-less discovery** toggle to the right.

</td></tr><tr><td>

MID Servers

</td><td>

MID Servers you want to use with use with the Cloud Discovery schedule.This field appears only when the Specific MID Server value is selected from the MID selection types field.

</td></tr></tbody>
</table>**Parent Topic:**[Discovery reference](discovery-references.md)

