---
title: Create secret for the Amazon SNS spoke
description: Create a client secret to authorize requests from Amazon SNS.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Create secret for the Amazon SNS spoke

Create a client secret to authorize requests from Amazon SNS.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scripts - Background**.

2.  Enter this command in the **Run script \(JavaScript executed on server\)** text field:

    `gs.info(GlideSecureRandomUtil.getSecureRandomString(32));`

3.  Click **Run Script**.

4.  Copy and record the generated value for later use.

    ![Client Secret or Authorization Key](../image/auth-token.png)


