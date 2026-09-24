---
title: AWS discover Organization pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS Cloud Organizations in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-discover-organization-pattern.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-15"
reading_time_minutes: 1
keywords: [Amazon AWS discover Organization, AWS Organizations discovery, AWS discovery, AWS patterns]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS discover Organization pattern-based discovery

Discovery and Service Mapping Patterns finds AWS Cloud Organizations in your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the AWS discovery prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - discover Organization pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The unique identifier \(ID\) of the management account of an organization.|
|Object ID \[object\_id\]|The unique ID of the management account of an organization.|
|Root ID \[root\_id\]|The unique ID of an organization.|
|Master Email \[master\_email\]|The email address associated with the AWS account designated as the management account for the organization.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

