---
title: AWS Events pattern-based discovery
description: Discovery uses event patterns to update Amazon AWS Cloud component data in near real-time. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery-and-service-mapping-patterns/aws-events-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 3
keywords: [AWS Events, Amazon AWS Events, AWS event discovery, AWS patterns]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Events pattern-based discovery

Discovery uses event patterns to update Amazon AWS Cloud component data in near real-time. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the AWS discovery prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

## Verify the REST API permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

## Events discovered by Discovery during horizontal discovery

Discovery uses patterns to find events created for Amazon AWS Cloud components. If there are events that indicate the change of state in one of the Amazon AWS Cloud components, it triggers discovery of Amazon AWS Cloud components using the patterns.

|Pattern|CI|
|-------|---|
|Amazon AWS Application and Network LBs Events|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Amazon AWS Classic LB Events|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Amazon AWS Network Events|Cloud Network \[cmdb\_ci\_network\]|
|Amazon AWS Security Group Events|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|
|Amazon AWS Storage Events|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Amazon AWS Subnet Events|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|
|Amazon AWS Virtual Server Events|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

**Related topics**  


[AWS Application and Network LB pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/aws-application-network-lb-pattern.md)

[AWS Classic Load Balancer pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/aws-classic-lb-pattern.md)

[AWS Network pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/aws-network-pattern.md)

[AWS Security Group pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/aws-security-group-pattern.md)

[AWS Storage pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/aws-storage-pattern.md)

[AWS subnet pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/aws-subnet-pattern.md)

[AWS virtual server pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/aws-virtual-server-pattern.md)

