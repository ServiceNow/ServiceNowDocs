---
title: Configure Server CI creation during AWS cloud discovery
description: Create Windows Server or Linux Server configuration items \(CIs\) during AWS cloud discovery by enabling the sn\_itom\_pattern.aws\_cloud\_discovery\_populate\_server\_ci system property.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/configure-aws-server-ci-cloud-discovery.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-08-11"
reading_time_minutes: 2
keywords: [AWS cloud discovery, Server CI, Windows Server, Linux Server, system property, SSM]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Configure Server CI creation during AWS cloud discovery

Create Windows Server or Linux Server configuration items \(CIs\) during AWS cloud discovery by enabling the **sn\_itom\_pattern.aws\_cloud\_discovery\_populate\_server\_ci** system property.

## Before you begin

-   Verify that you have at least version 1.35.0 of Discovery and Service Mapping Patterns.
-   Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the relevant patterns.
-   Verify that AWS Systems Manager \(AWS SSM\) is enabled on the Amazon Elastic Compute Cloud \(Amazon EC2\) instances.
-   Verify SSM Agent execution context.
    -   For Linux: The SSM Agent must run as root to retrieve the serial number using `dmidecode`.
    -   For Windows: The SSM Agent must run as SYSTEM to retrieve the serial number using `Get-CimInstance Win32_BIOS`.

Role required: admin

## About this task

Before Discovery and Service Mapping Patterns version 1.35.0, Server CIs weren't created during AWS cloud discovery. Starting with version 1.35.0, the **sn\_itom\_pattern.aws\_cloud\_discovery\_populate\_server\_ci** property controls whether Server CIs are created. The default value is false and Server CIs aren't created. You can set the property to true to create Server CIs for SSM-enabled EC2 instances.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the **Name** column, search for `sn_itom_pattern.aws_cloud_discovery_populate_server_ci`.

3.  Select the **sn\_itom\_pattern.aws\_cloud\_discovery\_populate\_server\_ci** property.

4.  In the **Value** field, enter `true`.

    To stop creating Server CIs during AWS cloud discovery, enter `false`.

5.  Select **Update**.


## What to do next

Run AWS cloud discovery or wait for the next scheduled discovery run for the changes to apply.

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

**Related topics**  


[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

[AWS Linux Server pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-linux-server-pattern.md)

[AWS Windows Server pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-windows-server-pattern.md)

