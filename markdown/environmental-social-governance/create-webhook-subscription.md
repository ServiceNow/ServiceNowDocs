---
title: Create a webhook subscription
description: Webhooks are used to simplify communication between two applications. Create a webhook subscription to connect to Concur through webhook.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a SAP Concur webhook registry, Integrating Operational Sustainability Management \(formerly ESG\) with SAP Concur, Integrating Operational Sustainability Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Create a webhook subscription

Webhooks are used to simplify communication between two applications. Create a webhook subscription to connect to Concur through webhook.

## Before you begin

Role required: sys\_admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **Actions**.

3.  Using the **Search** field, search for Create webhook subscription.

4.  Select**Create webhook subscription**.

5.  Select **Test**.

6.  In the Test Action dialog box fill in the fields.

    1.  In the **Name** field provide a name for the test.

        Ensure that the name has no spaces and special characters.

    2.  In the **Endpoint** field, paste the URL that you generated when you created the SAP webhook registry.

    3.  In the **Topic** field, select **Public.concur.travel.itinerary**.

    4.  Select **Run Test**.


**Parent Topic:**[Create a SAP Concur webhook registry](create-concur-webhook-registry.md)

