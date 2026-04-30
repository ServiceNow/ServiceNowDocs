---
title: Upload your Code Signing configuration file to your protected instance
description: Upload the configuration file generated on your trusted instance.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Code Signing, Code Signing, Platform Security]
---

# Upload your Code Signing configuration file to your protected instance

Upload the configuration file generated on your trusted instance.

## Before you begin

Roles required:

-   admin
-   security\_admin
-   codesigning\_admin

    **Note:** The codesigning\_admin role can be assigned using the process detailed in [Assign the Code Signing Administrator Role](cse-assign-roles.md).

-   sn\_kmf.cryptographic\_manager

You also need the configuration file generated in the steps detailed in [Configure Code Signing Enterprise on your trusted instance](cse-turn-on-cse.md).

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets**.

2.  Select **Import Update Set from XML** at the bottom of the Retrieved **Update Sets** list.

3.  Select **Choose File**, and select your configuration file \(xml file extension\).

4.  Select **Upload**.

    You should see the **Codesigning configuration** update set in the **Retrieved Update Sets** list.

5.  Select and open the **Codesigning configuration** update set.

6.  Select **Preview Update Set Batch**.

    If any conflicts occur during the preview, resolve them by selecting **Accept remote update** or **Resolve known CS conflicts**.

7.  After resolving any conflicts, select **Commit Update Set Batch**.


**Parent Topic:**[Configuring Code Signing](../concept/config-code-signing.md)

