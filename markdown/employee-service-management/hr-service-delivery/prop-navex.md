---
title: Configure properties
description: Configure properties to ensure that data is properly mapped between the Navex EthicsPoint system and the ServiceNow system.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up Employee Relations integration with Navex Ethicspoint, Employee Relations integration with Navex Ethicspoint, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure properties

Configure properties to ensure that data is properly mapped between the Navex EthicsPoint system and the ServiceNow system.

## Before you begin

Role required: sn\_hr\_navex\_ep.admin

## Procedure

1.  Navigate to **ER Navex Integration** &gt; **Administration** &gt; **Properties**.

2.  Configure the following properties:

<table id="table_aqh_ycr_xsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tier Id in Navex EthicsPoint

</td><td>

Tier ID that contains the Navex EthicsPoint instance.

</td></tr><tr><td>

Comma-separated Ready to Pull Status Ids in Navex EthicsPoint

</td><td>

Status IDs that are to be pulled from Navex EthicsPoint instance into ServiceNow instance. For example, status IDs of Open, Closed, or Review.

</td></tr><tr><td>

Comma-separated list of closed status ids in Navex EthicsPoint

</td><td>

Status IDs of closed cases that are pulled from Navex EthicsPoint instance into ServiceNow instance.

</td></tr><tr><td>

Comma-separated Primary Issue Type Ids in Navex EthicsPoint

</td><td>

Primary issue type case IDs that are pulled from Navex EthicsPoint instance into ServiceNow instance. For example, primary issue type of a case can be misconduct, discrimination, or accounting.

</td></tr><tr><td>

HR Service used for the case imported from Navex EthicsPoint

</td><td>

HR service to which you want to associate the employee relation case.

</td></tr><tr><td>

Pull attachments. Please configure MID Server if you want to pull the attachments.

</td><td>

Option to pull cases along with the attachments from Navex EthicsPoint instance into ServiceNow instance.To use this feature, you must enable the MID Server. For more information, see [Configure MID Server network connectivity](https://www.servicenow.com/docs/access?context=c_MIDServerConnectionPrerequisites&version=xanadu&pubname=xanadu-servicenow-platform&section=t_ConfigMIDSvrConnecPrereq&ft:locale=en-US)

</td></tr><tr><td>

Pull the attachments from the case file. \(Make sure that the mid server is on, when this is used\)

</td><td>

Option to provide the **Sync attachments** button on cases that are that are already pulled from Navex EthicsPoint instance into ServiceNow instance. The **Sync attachments** button can be used to pull attachments of cases at a later point in time.To use this feature, you must enable the MID Server. For more information, see [Configure MID Server network connectivity](https://www.servicenow.com/docs/access?context=c_MIDServerConnectionPrerequisites&version=xanadu&pubname=xanadu-servicenow-platform&section=t_ConfigMIDSvrConnecPrereq&ft:locale=en-US)

</td></tr></tbody>
</table>3.  Click **Save**.


