---
title: Create a granular role module access policy for symmetric encryption
description: Create a granular role module access policy \(MAP\) to secure data while permitting users not assigned to a specific MAP to submit forms on a public record.
locale: en-US
release: zurich
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2025-09-04"
reading_time_minutes: 1
breadcrumb: [Configuring the Key Management Framework, Key Management Framework, Encryption]
---

# Create a granular role module access policy for symmetric encryption

Create a granular role module access policy \(MAP\) to secure data while permitting users not assigned to a specific MAP to submit forms on a public record.

## Before you begin

Role required: security\_admin

## Procedure

1.  Navigate to **All** &gt; **Key Management** &gt; **Module Access Policies** &gt; **All**.

2.  Select **New**.

3.  Enter a name for the policy.

4.  Select the **Crypto module** that you’ll be granting access to.

5.  Select the appropriate **Target role**.

6.  Select the Specify purpose box and enter the purpose details in the newly displayed fields as follows:![Module access policy purpose options.](../image/map_purpose.png)

7.  -   **Crypto spec**: Select the crypto spec to be used.
-   **Granular operation**: Select Symmetric Encryption from the drop-down list.
8.  Select the **Active** box.

9.  For **Result** select **Track**.


## Result

The granular role MAP enables a user that is not assigned to a MAP to submit public record forms while securing data.

**Parent Topic:**[Configuring the Key Management Framework](../concept/configure-kmf.md)

