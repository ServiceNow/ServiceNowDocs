---
title: Automatic Security Task generation
description: Learn about how and when your instance generates Security Tasks.
locale: en-US
release: australia
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Security Tasks, Security Center, Platform Security]
---

# Automatic Security Task generation

Learn about how and when your instance generates Security Tasks.

## Automatically generated Security Tasks

Security Tasks can be automatically generated. Automatic Security Task generation is triggered by an associated event that occurred on the platform. For example:

-   **Metrics threshold breached**

    A Security Task is generated for a metric when it's threshold is breached. There’s only one open task for a metric, even if the same metric has multiple breaches. If a Security Task for a breached metric is closed, a new task is generated is the threshold is breached again.

-   **Event notification**

    A Security Task is generated when a security event notification triggers \(meets conditions of it's policy\). As with metrics, there’s only one open task for a policy, with a new task being generated if the previous one is closed, and the notification triggers again. For details on security event notifications, see [Security Event Notifications](security-policies.md).

-   **Hardening score deviation**

    When the hardening score degrades below the configured threshold value \(default 3\), a Security Task is generated. For example, if the hardening score is 97, and is 94 the next day, a Security Task is created just after the score of 94 is calculated. Only a single open task is created. The platform will not generate another task if the score lowers again the next day from 94 to 91. For details on your hardening score, see [Hardening compliance score trend](score-trend.md).

-   **Customer Action**

    A Security Task is generated whenever a Customer Action is installed. For details on Customer Actions, see [Customer Actions](critical-updates.md).

-   **Banner announcement**

    A Security Task is generated for each new banner announcement. For details on banner announcements, see [Security banner announcements](scc-banner.md).


## Automatically generated security settings

Configuration options for automatically generated Security Tasks are found in the security center properties page. Find these settings by navigating to **All** &gt; **Security Center** &gt; **Security Center Properties**.

-   **Enable/Disable automated Security Tasks**

    When the **Yes/No** field is selected, automated Security Tasks are enabled on your instance.

-   **Hardening score degradation threshold**

    The value in the field represents the amount by which the hardening score must degrade \(since the last daily score\) to generate a Security Task. This value must be a positive integer. The default value is 3.


**Parent Topic:**[Security Tasks](security-task-manager.md)

