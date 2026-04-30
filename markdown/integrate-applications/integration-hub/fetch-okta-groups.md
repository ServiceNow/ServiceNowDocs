---
title: Fetch Okta groups
description: Fetch Okta groups into your instance so that you can assign them to different users. You can fetch the groups on an as-needed or scheduled basis.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Okta Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Fetch Okta groups

Fetch Okta groups into your instance so that you can assign them to different users. You can fetch the groups on an as-needed or scheduled basis.

## Before you begin

Role required: okta.admin

## Procedure

1.  To fetch Okta groups on an as-needed basis.

    1.  Navigate to **Okta spoke** &gt; **Okta groups**.

    2.  Select **Fetch Okta groups**.

        The Get Groups subflow is triggered.

    3.  From the Okta groups list, you can review the following:

        |Column|Description|
        |------|-----------|
        |Name|Name of the Okta group.|
        |Description|Description of the Okta group.|
        |Group ID|Group ID of the Okta group.|
        |Type|Type of the Okta group.|
        |Group creation date|Date when Okta group was created.|
        |Group last updated date|Date when Okta group was last updated.|
        |Created|Date when Okta group was first synchronized with your ServiceNow instance.|
        |Updated|Date when Okta group was last synchronized with your ServiceNow instance.|

2.  Fetch Okta groups on a scheduled basis.

    1.  Navigate to **System Defintion** &gt; **Scheduled Jobs**.

    2.  Open the **Fetch Okta Groups** record.

    3.  Update the fields, as needed.

        **Note:**

        -   Make sure that the **Active** option is selected so that the scheduled job is activated for use.
        -   The Updated column on your ServiceNow instance displays the time when the Okta group details was updated.
    4.  Click **Update**.


