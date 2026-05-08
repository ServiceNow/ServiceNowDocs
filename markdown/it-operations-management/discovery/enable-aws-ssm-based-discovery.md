---
title: Enable AWS SSM-based discovery
description: Configure Discovery to use AWS Systems Manager \(SSM\) Agent.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [AWS SSM discovery, Discovery for AWS, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Enable AWS SSM-based discovery

Configure Discovery to use AWS Systems Manager \(SSM\) Agent.

## Before you begin

Role required: discovery\_admin

## About this task

The AWS SSM Agent runs with root \(Linux\) or SYSTEM \(Windows\) privileges, meaning any command sent through it can execute with full system access. Due to this high level of access, SSM is turned off by default for security reasons. On Linux, you can configure non-root credentials to run Discovery commands more securely. On Windows, Discovery commands require SYSTEM-level access, so you must decide whether to enable this capability based on your security requirements. Enabling **glide.discovery.enable\_ssm** doesn't automatically activate SSM discovery on Windows. Unlike Linux, Windows lacks support for using a non-SYSTEM user, so for security reasons, you must explicitly enable the **glide.discovery.ssm.enable\_windows** property to use AWS SSM discovery on Windows devices.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  In the **Name** field, enter `glide.discovery.enable_ssm`.

3.  Double-click the **Value** field to perform inline editing.

4.  Enter `true`.

5.  Select the check mark \(![check mark icon](../../cloud-management-v2/image/icon-check-mark.png)\) icon.

6.  To enable AWS SSM-based discovery on Windows machines, repeat steps 2-5 for the **glide.discovery.ssm.enable\_windows** property.


## What to do next

Define fallback root behavior using the **mid.discovery.aws\_ssm.linux.fallback\_root\_user** property or create non-root credentials to execute Discovery commands using the AWS SSM Instance Users \[aws\_ssm\_instance\_user\_credentials\] table. For more information, see [Enable root fallback](../task/enable-root-fallback.md) and [Configure custom user credentials](../task/configure-custom-user-credentials.md).

