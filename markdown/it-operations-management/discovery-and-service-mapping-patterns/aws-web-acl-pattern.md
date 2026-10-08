---
title: AWS web ACL pattern-based discovery
description: Discovery and Service Mapping Patterns finds AWS web access control lists \(web ACLs\) on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/aws-web-acl-pattern.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 2
keywords: [Amazon AWS Web ACL, AWS WAF, AWS web access control list, AWS discovery, AWS patterns, Web ACL pattern]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS web ACL pattern-based discovery

Discovery and Service Mapping Patterns finds AWS web access control lists \(web ACLs\) on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

**Note:** Security Operations users can leverage the integration with Discovery to import web ACL rules and load balancers with attached web ACLs. For more information on setting ACL rules and using the Mitigation Controls Monitoring app, see [Configure the AWS WAF integration for mitigation controls monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/spc-install-config-aws-waf.md).

## AWS web ACL data model

The Amazon AWS - Web ACL \(LP\) pattern introduces the following CI class that extends an existing CMDB class.

|CI class|Extends from|
|--------|------------|
|Web ACL \[cmdb\_ci\_web\_acl\]|Virtual Machine Object \[cmdb\_ci\_vm\_object\]|

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/create-aws-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - Web ACL \(LP\) pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the web ACL.|
|Object ID \[object\_id\]|Unique ID for the web ACL from AWS.|
|Description \[short\_description\]|Description of the web ACL provided by AWS.|
|Default Action \[default\_action\]|Default action when no rules in the web ACL match. The value is **allow** or **deny**.|

**Note:** Security Operations users can leverage the integration with Discovery to import web ACL rules and load balancers with attached web ACLs. For more information on setting ACL rules and using the Mitigation Controls Monitoring app, see [Configure the AWS WAF integration for mitigation controls monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/spc-install-config-aws-waf.md).

## CI relationships

The Amazon AWS - Web ACL \(LP\) pattern creates the following relationships to support Amazon AWS Web ACL discovery.

|CI|Relationship|CI|
|---|------------|---|
|Web ACL \[cmdb\_ci\_web\_acl\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

