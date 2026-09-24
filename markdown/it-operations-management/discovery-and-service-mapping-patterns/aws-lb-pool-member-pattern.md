---
title: AWS LB Pool Member pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS Application Load Balancer \(LB\) pool members \(known in AWS as target group members\) in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-lb-pool-member-pattern.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-15"
reading_time_minutes: 2
keywords: [Amazon AWS LB Pool Member, AWS load balancer target discovery, AWS discovery, AWS patterns]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS LB Pool Member pattern-based discovery

Discovery and Service Mapping Patterns finds AWS Application Load Balancer \(LB\) pool members \(known in AWS as target group members\) in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/create-aws-service-accounts.md).

-   **Enable AWS Application Load Balancer target discovery**

    By default, the Amazon AWS - LB Pool Member\(LP\) pattern doesn't execute discovery. To enable the discovery of AWS Application Load Balancer targets, set the **sn\_itom\_pattern.discover\_aws\_app\_pool\_members** MID Server property to **true**. For more information, see [Enable AWS Application Load Balancer target discovery]().


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - LB Pool Member\(LP\) pattern.

<table id="table_ntq_x3y_p2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Target ID, depending on the target type. For example: Instance ID, IP address, Lambda ARN, or Application Load Balancer ARN.

</td></tr><tr><td>

Service port \[service\_port\]

</td><td>

The port on which the target is listening, if available.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Possible values are:-   Target ID
-   Target ID and target port, if available, in the following format: `<target ID>#<target port>`.

For example: `i-0123456789abcdef0#8080`


</td></tr><tr><td>

Comments \[comments\]

</td><td>

Comments related to the CI.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the target. Possible values are Operational or Non-Operational.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Installation status of the target. Possible values are Installed or Retired.

</td></tr><tr><td>

Pool \[pool\]

</td><td>

References the Load Balancer Pool \[cmdb\_ci\_lb\_pool\] table.

</td></tr></tbody>
</table>## CI relationships

The Amazon AWS - LB Pool Member\(LP\) pattern creates the following relationships and references to support AWS LB Pool Member discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Owns::Owned by|Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]|Pool \[pool\]|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

