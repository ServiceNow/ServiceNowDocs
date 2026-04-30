---
title: Configuring the ServiceNow AI Platform to optimize performance
description: Configure browser settings, transaction and application quotas, and operational toggles options to optimize performance. Optimizing ServiceNow AI Platform performance supports a smooth a responsive user experience.
locale: en-US
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Platform performance, Maintain and monitor, Administer]
---

# Configuring the ServiceNow AI Platform to optimize performance

Configure browser settings, transaction and application quotas, and operational toggles options to optimize performance. Optimizing ServiceNow AI Platform performance supports a smooth a responsive user experience.

## Configuration overview

Most configuration for platform performance optimization is completed by instance administrators in each instance of the ServiceNow AI Platform. Any user can verify browser configuration to optimize performance.

-   [Set transaction quotas](c_TransactionQuotas.md)

    Instance administrators set transaction quotas to help prevent poorly performing queries and scripts from consuming system resources. After determining normal parameters for transactions, you can create a transaction quota rule that defines when a long-running transaction should be canceled.

-   [Set application quotas](c_ApplicationQuotas.md)

    Instance administrators can set application quotas in addition to global transaction quotas. Application quota rules limit the number of events or jobs that can run within an application's scope during a specified amount of time, helping optimize bandwidth use.

-   [Set operational toggles](operational-toggles.md)

    Instance administrators can control how much bandwidth an application uses in the instance by mapping system run levels to operational toggles.

-   [Verify browser settings for performance optimization](c_Compression.md)

    Verify that your browser supports data compression to support optimal performance. Any user can verify that their browser's settings.


