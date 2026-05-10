---
title: Enable root fallback
description: Enable the fallback root user property to allow AWS SSM discovery to run commands as root on Linux systems when alternate user credentials aren’t configured.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [AWS SSM discovery, Discovery for AWS, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Enable root fallback

Enable the fallback root user property to allow AWS SSM discovery to run commands as root on Linux systems when alternate user credentials aren’t configured.

## Before you begin

Confirm that AWS SSM Agent discovery is enabled. For more information, see [Enable AWS SSM-based discovery](../concept/enable-aws-ssm-based-discovery.md).

Role required: discovery\_admin

## About this task

When the **glide.discovery.enable\_ssm** property is enabled, AWS SSM Discovery on Linux defaults to using the root user for command execution. If you prefer not to configure alternate user credentials on your EC2 instances, you must enable the **mid.discovery.aws\_ssm.linux.fallback\_root\_user** MID Server property to allow fallback to root execution. When enabled, it automatically creates a record in the AWS SSM Instance Users \[aws\_ssm\_instance\_user\_credentials\] table with the user name root. However, if you leave this property set to **false**, you must configure non-root credentials to run Discovery commands. For more information, see [Configure custom user credentials](configure-custom-user-credentials.md).

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **All Properties**.

2.  In the **Name** field, enter `mid.discovery.aws_ssm.linux.fallback_root_user`.

3.  Double-click the **Value** field to perform inline editing.

4.  Enter `true`.

5.  Select the check mark \(![check mark icon](../../cloud-management-v2/image/icon-check-mark.png)\) icon.


## Result

A new record is added to the AWS SSM Instance Users \[aws\_ssm\_instance\_user\_credentials\] table with the user name "root".

