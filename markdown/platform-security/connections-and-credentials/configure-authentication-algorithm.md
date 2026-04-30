---
title: Configure an authentication algorithm
description: Configure an authentication algorithm so that you can sign outbound HTTP requests.
locale: en-US
release: yokohama
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Authentication Algorithms, Connections and Credentials, Access Management]
---

# Configure an authentication algorithm

Configure an authentication algorithm so that you can sign outbound HTTP requests.

## Before you begin

You should have a script include configured before you configure an authentication algorithm.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Credentials &amp; Connections** &gt; **Authentication Algorithms**, and click **New**.

2.  On the form, fill in the fields.

    The database selection in the **Format** field determines which fields are available.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name of this algorithm.|
    |Algorithm|Outbound request type.|
    |Description|Description of what your algorithm does.|
    |Application|Scope that your application runs in.|
    |Instance Authentication Script|Script that you select from the Script Includes table.|
    |MID Authentication Script|Script that you select from the MID Server Script Includes \[Discovery view\] table.|

3.  Click **Submit**.


