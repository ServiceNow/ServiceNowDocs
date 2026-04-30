---
title: Data retrieval limitations
description: By default, there are no restrictions on how data is retrieved from Qualys. Many records can be related to low severity vulnerabilities that a customer is not willing to remediate using their vulnerability response process. Updating the corresponding REST message/method parameters can modify this behavior.
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Resolve integration issues, Qualys, Integrate, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Data retrieval limitations

By default, there are no restrictions on how data is retrieved from Qualys. Many records can be related to low severity vulnerabilities that a customer is not willing to remediate using their vulnerability response process. Updating the corresponding REST message/method parameters can modify this behavior.

The REST message/method responsible for this update is **Qualys Host Detection – Standard/post**. To update the values, add a new HTTP Query Parameter to the post method with the following values:

-   Name: severities
-   Value: 3-5 \(or whatever appropriate severities are desired\)

