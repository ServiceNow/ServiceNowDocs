---
title: Configure the Webhook on the Proofpoint DLP tenant for alert notifications to ServiceNow
description: Configure a webhook on Proofpoint using the REST API endpoint to start getting the alerts from the Proofpoint DLP tenant. Your ServiceNow instance creates DLP incidents from these alerts. The Proofpoint DLP integration provides a REST API endpoint for end users to configure the webhook.
locale: en-US
release: zurich
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Install and configure the Proofpoint integration for Data Loss Prevention, Data Loss Prevention Incident Response Integration with Proofpoint, Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Configure the Webhook on the Proofpoint DLP tenant for alert notifications to ServiceNow

Configure a webhook on Proofpoint using the REST API endpoint to start getting the alerts from the Proofpoint DLP tenant. Your ServiceNow instance creates DLP incidents from these alerts. The Proofpoint DLP integration provides a REST API endpoint for end users to configure the webhook.

## Before you begin

Role required: sn\_pp\_dlp.api\_integration\_user

## Procedure

1.  Log in to **Proofpoint**.

2.  Navigate to **Proofpoint Tenant** &gt; **Administration Application** &gt; **Integration** &gt; **Notification Policies**.

3.  Create a notification policy with an appropriate name.

4.  Click the **Notification policy** and manage the webhooks configured on the notification policy.

5.  Create a new webhook configuration by clicking **Add Webhooks**.

6.  Select the webhook type as **Generic**.

7.  In URL Input, enter a URL using the format: `https://<Instance_Name>.service-now.com/api/sn_pp_dlp/proofpointalertapi/getalerts`.

8.  Keep the method as **POST**.

9.  Add the following headers to the webhook:

    -   ```
Name: Authorization 
Value: Basic <Base64Encoded Username and Password of the ServiceNow instance user>
```

    -   ```
Name: Content-Type 
Value: application/json
```

10. D not change the other values.

11. Click **Save**.

12. Navigate to **Proofpoint Tenant** &gt; **Administration Application** &gt; **Policies** &gt; **Rules**.

13. In the Actions section, select the rules for which the webhook notification should be generated.

14. Add the newly created Notification policies that have a webhook configured.

15. Click **Save**.


**Parent Topic:**[Install and configure the Proofpoint integration for Data Loss Prevention](install-configure-proofpoint-integration-dlp.md)

