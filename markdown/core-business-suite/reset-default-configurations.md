---
title: Reapply the default configurations
description: If the default configurations aren’t applied for Core Business Suite or its business units, reapply the default configurations by running a script.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-05"
reading_time_minutes: 1
breadcrumb: [Configure, Core Business Suite]
---

# Reapply the default configurations

If the default configurations aren’t applied for Core Business Suite or its business units, reapply the default configurations by running a script.

## Before you begin

**Note:** When the default configurations aren’t applied, the following message appears:

Installation succeeded, but some default configurations couldn't be applied. Review and complete the remaining steps in configuration.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script - Background**.

    The run script page opens.

2.  Copy this script and paste it into the script editor.

    ```
    var driverScript = new sn_cbs.CBSDriver();
    var result = driverScript.onBUTrigger("placeholder");
    gs.info(JSON.stringify(result, null, 2));
    ```

3.  Replace `placeholder` with the appropriate business unit name.

    **Note:** Use only the supported business unit names when replacing the text placeholder. Using an incorrect name can cause the script to fail.

    Business unit names are: CBS, WSD, LEGAL, HR, S2P, HEALTH, FCM.

4.  Select **Run Script**.

    After the script completes, the script-completed page displays the execution logs followed by a success message.


**Parent Topic:**[Configure Core Business Suite Foundation](../concept/configure-cbs.md)

