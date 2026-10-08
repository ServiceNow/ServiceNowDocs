---
title: AWS SSM Cloud Agents pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS Systems Manager \(SSM\) agents on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/aws-ssm-cloud-agents-pattern.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 2
keywords: [Amazon AWS SSM Cloud Agents, AWS Systems Manager, AWS SSM agent, AWS discovery, AWS patterns, SSM Cloud Agents pattern]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS SSM Cloud Agents pattern-based discovery

Discovery and Service Mapping Patterns finds AWS Systems Manager \(SSM\) agents on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## SSM data model

The Amazon AWS - SSM Cloud Agents \(LP\) pattern introduces the following CI class that extends an existing CMDB class.

|CI class|Extends from|
|--------|------------|
|Cloud System Management Agent \[cmdb\_ci\_cloud\_system\_management\_agent\]|Virtual Machine Object \[cmdb\_ci\_vm\_object\]|

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/create-aws-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - SSM Cloud Agents \(LP\) pattern.

<table id="table_cmdb_ci_cloud_system_management_agent"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cloud Agent Type \[cloud\_agent\_type\]

</td><td>

Type of cloud agent. The value is set to **AWS SSM**.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the SSM agent:-   **Installed**: The agent is currently running.
-   **Absent**: The agent is not currently running.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

Address of the virtual machine \(VM\) instance.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the VM instance that the SSM agent is running on.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

ID of the VM instance.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the agent service.Possible values are Operational or Non-Operational.

</td></tr><tr><td>

Operating System Platform \[operating\_system\_platform\]

</td><td>

Operating system type of the VM instance.

</td></tr><tr><td>

Resource Type \[resource\_type\]

</td><td>

Type of resource managed by SSM.Possible values are EC2Instance or ManagedInstance.

</td></tr><tr><td>

Version \[version\]

</td><td>

Version of the SSM agent.

</td></tr></tbody>
</table>## CI relationships

The Amazon AWS - SSM Cloud Agents \(LP\) pattern creates the following relationships to support AWS SSM Cloud Agents discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud System Management Agent \[cmdb\_ci\_cloud\_system\_management\_agent\]|Runs on::Runs|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

