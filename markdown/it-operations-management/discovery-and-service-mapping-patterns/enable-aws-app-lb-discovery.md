---
title: Enable AWS Application Load Balancer target discovery
description: Enable the sn\_itom\_pattern.discover\_aws\_app\_pool\_members MID Server property to discover AWS Application Load Balancer targets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/enable-aws-app-lb-discovery.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [AWS LB Pool Member, AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Enable AWS Application Load Balancer target discovery

Enable the **sn\_itom\_pattern.discover\_aws\_app\_pool\_members** MID Server property to discover AWS Application Load Balancer targets.

## Before you begin

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Amazon AWS - LB Pool Member\(LP\) pattern.

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Mid Server** &gt; **Properties**.

2.  In the **Name** field, search for `sn_itom_pattern.discover_aws_app_pool_members`.

3.  Select the **sn\_itom\_pattern.discover\_aws\_app\_pool\_members** property.

4.  In the **Value** field, enter `true`.

5.  Select **Update**.


**Parent Topic:**[AWS LB Pool Member pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-lb-pool-member-pattern.md)

**Related topics**  


[AWS LB Pool Member pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-lb-pool-member-pattern.md)

[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

