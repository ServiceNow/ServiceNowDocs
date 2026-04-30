---
title: Tamper Detection
description: Use tamper detection to improve security by detecting unauthorized changes to your quorum control settings.
locale: en-US
release: xanadu
product: Cloud Encryption
classification: cloud-encryption
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Cloud Encryption with Key Management, Encryption]
---

# Tamper Detection

Use tamper detection to improve security by detecting unauthorized changes to your quorum control settings.

## Tamper detection process

When enabled, tamper detection validates your quorum control settings by checking for any unauthorized modifications \(tampering\). Tamper detection uses hash-based message authentication code \(HMAC\).

1.  When a setting is changed or created, your instance creates an HMAC. The HMAC is based on the value of the setting \(dare\_property\) record.
2.  Whenever your instance uses these settings, tamper detection validates it using the HMAC.
3.  If the setting validates successfully, it can be used by the platform, otherwise it cannot.

-   **Tamper detection runs daily on your instance**

    Tamper detection checks your settings for tampering using a daily scheduled job, and reports validation failures in your node and security logs. Tamper detection send a notification to Security and KMF admins for validation failures.

    ![flowchart displaying tamper detection job](../image/tamper-job-flow.png)

-   **Tamper detection runs before executing a key withdrawal**

    Tamper detection also validates your properties when you request a key withdrawal. If your settings do not pass validation, the key withdrawal does not execute. In this case, you must resolve any validation issues before key withdrawal can compete.

    ![flowchart displaying tamper detection during key withdrawal](../image/tamper-withdraw-flow.png)


## Identifying tampering

-   **Tamper detection updates your logs when validation fails.**

    If tamper detection fails to validate any of your quorum control settings, these failures appear in your node and security logs. The log entry includes the sys\_id of the settings \(dare\_property\) record that failed validation.

    ```
    2022-06-28 13:45:46 (582) Default-thread-5 B6FAC1F6C3D01110CF37169D7940DD6E txid=231c4d72c310 SEVERE HMAC_VALIDATION_FAILED:The dare_property record with sys_id: 776e3200c3210110900b169d7940dd76 failed HMAC validation
    
    2022-06-28 13:47:35 (264) Default-thread-8 B6FAC1F6C3D01110CF37169D7940DD6E txid=8e8cc972c310 SEVERE HMAC_VALIDATION_FAILED:The dare_property record with sys_id: 758b3200c3210110900b169d7940dd76 failed HMAC validation
    ```

    Logging displays information similar to these examples when validation fails. Successful validations do not appear in the logs.

-   **Tamper detection displays a warning message on your quorum control settings page**

    If a quorum control setting has failed validation, you can see a warning when you view the Quorum Control Policy settings page on your instance. The warning includes the sys\_id of the settings \(dare\_property\) record that failed validation.

    ![Example banner warning on quorum control page](../image/tamper-warning-banner.png)

-   **Tamper detection sends notifications to users with the __Security Admin__ and __KMF Admin__ roles**

    If tamper detection fails to validate any of your quorum control settings, your security admins and KMF admins receive a notification similar to this example.

    ![Example message for tamper detection](../image/tamper-sample.png)


## Resolving tampering issues with ServiceNow support

**Important:** Tamper detection validation failures can only be resolved with assistance of ServiceNow support.

![flowchart displaying tamper detection during key withdrawal](../image/tamper-resolve-flow.png)

If tamper detection fails to validate any of your quorum control settings, contact ServiceNow support for assistance in resolving the issue. After a support agent has resolved the validation failure, security and KMF admins receive a notification indicating that the issue has been resolved.

![Example message for tamper detection resolution](../image/tamper-resolve.png)

**Parent Topic:**[Cloud Encryption with Key Management](dare-overview.md)

