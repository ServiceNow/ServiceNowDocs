---
title: Configure iFrame embedding for Care Team Portal
description: For the Care Team Portal to successfully launch in Hyperspace via Hyperdrive, the portal must be configured to work within an iFrame.
locale: en-US
release: australia
product: Healthcare Operations Core
classification: healthcare-operations-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Embed Care Team Portal in Epic, Configure, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Configure iFrame embedding for Care Team Portal

For the Care Team Portal to successfully launch in Hyperspace via Hyperdrive, the portal must be configured to work within an iFrame.

## Before you begin

Role required: admin

## Procedure

1.  Set your scope to **Global** and elevate your role to **security\_admin**.

2.  Navigate to **All** &gt; **HTTP Response Headers** \(or type in sys\_response\_header.list\).

3.  Select the **Global** response header.

4.  Add the domain name for your Epic hyperspace instance to the list of values.

    For example, \*.yourdomain.com

5.  Ensure that **Active** is set to true.

6.  Select **Submit**.


## Result

![Proper domain indication on iFrame configuration for Epic.](../image/configureiframe.png)

