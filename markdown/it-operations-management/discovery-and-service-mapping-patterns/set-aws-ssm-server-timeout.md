---
title: Set the AWS SSM command wait time
description: Increase the wait time for AWS Systems Manager \(AWS SSM\) commands to support Server CI creation on slow-responding EC2 instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/set-aws-ssm-server-timeout.html
release: brazil
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-09-17"
reading_time_minutes: 2
keywords: [AWS Cloud Discovery, SSM Server CI, MID Server properties, AWS Systems Manager]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Set the AWS SSM command wait time

Increase the wait time for AWS Systems Manager \(AWS SSM\) commands to support Server CI creation on slow-responding EC2 instances.

## Before you begin

-   Verify that the **sn\_itom\_pattern.aws\_cloud\_discovery\_populate\_server\_ci** system property is set to `true`. For more information, see [Configure Server CI creation during AWS cloud discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/configure-aws-server-ci-cloud-discovery.md).
-   Verify that you have at least version 1.35.0 of Discovery and Service Mapping Patterns.

Role required: discovery\_admin

## About this task

By default, the MID Server waits 30 seconds \(30000 ms\) before checking whether the Server CI is created on a Windows or Linux EC2 instance. If instances in your environment are slow to respond, Server CIs may not be created. Increase the **sn\_itom\_pattern.discover\_aws\_server\_command\_initial\_wait\_ms** MID Server property value to provide more time before the first status check.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Properties**.

2.  In the **Name** column, search for `sn_itom_pattern.discover_aws_server_command_initial_wait_ms`.

3.  Select the **sn\_itom\_pattern.discover\_aws\_server\_command\_initial\_wait\_ms** MID Server property.

4.  In the **Value** field, enter the wait time in milliseconds.

    The default value is `30000` \(30 seconds\). The property accepts any positive integer.

5.  Select **Update**.


## Result

The MID Server applies the updated wait time when running the next SSM commands during AWS Cloud Discovery Server CI creation.

## What to do next

Run AWS Cloud Discovery again to apply the change.

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

**Related topics**  


[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

[AWS Linux Server pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-linux-server-pattern.md)

[AWS Windows Server pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/aws-windows-server-pattern.md)

[Configure Server CI creation during AWS cloud discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery-and-service-mapping-patterns/configure-aws-server-ci-cloud-discovery.md)

