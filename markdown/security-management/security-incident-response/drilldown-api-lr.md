---
title: Set up the REST API
description: You use the LogRhythm REST API key to gather additional event details for individual alarm fields. The API key provides details that are unavailable using the LogRhythm REST API.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [LogRhythm Overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up the REST API

You use the LogRhythm REST API key to gather additional event details for individual alarm fields. The API key provides details that are unavailable using the LogRhythm REST API.

## Before you begin

Role required: LogRhythm Client Console/Platform Manager Administrator

## About this task

This task is performed on the LogRhythm Client Console. Set up the LogRhythm REST API prior to installing the plugin from the ServiceNow Store.

## Procedure

1.  Navigate to the LogRhythm Client Console and select the **File** menu.

2.  Click **New** to create a new user.

    ![File menu expanded in the LogRhythm Console.](../image/lr-soap-5-cropped.png)

3.  In the **Is Person an Individual?** dialog that is displayed, click **Yes**.

    ![Is Person an Individual dialog.](../image/lr-soap-6.png)

4.  In the Person Properties dialog that is displayed, fill in the Name fields.

    Use a different name for the LogRhythm REST API than the one you used to create the REST API, for example, `REST API_2`.

    ![Person Properties dialog with name fields highlighted.](../image/lr-api-2-CDAPI.png)

5.  Click **OK**.

6.  Right-click the new listing in the Name column \(**API\_2\_REST**\) and, in the choice list, select **Create Case API Account**.

    ![Create Case API Account in LogRhythm Console.](../image/lr-api-3-CDAPI.png)

    **Note:** The Case API is not used, but the credentials for the Case API Account and the LogRhythm REST API are the same.

7.  In the Service Account Properties dialog, click **Generate**.

    ![API Token in Service Account Properties dialog.](../image/lr-api-4-CDAPI.png)

8.  Click **Copy**.

    ![Copy button on API Token API in Service Account Properties dialog.](../image/lr-api-5-CDAPI.png)

    You have now set up the LogRhythm REST API. You paste the string you copied in the previous step into your ServiceNow AI Platform instance in the LogRhythm REST API Token field during the configuration steps listed in [Install the plugin and configure LogRhythm](install-and-config-logrhythm.md).


## What to do next

You are now ready to [Install the plugin and configure LogRhythm](install-and-config-logrhythm.md).

**Parent Topic:**[LogRhythm Overview](../concept/ovrview-logrhythm.md)

**Previous topic:**[LogRhythm Overview](../concept/ovrview-logrhythm.md)

**Next topic:**[Install the plugin and configure LogRhythm](install-and-config-logrhythm.md)

