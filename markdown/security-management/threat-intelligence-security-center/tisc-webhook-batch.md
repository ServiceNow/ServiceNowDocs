---
title: View webhook batches
description: A webhook batch record is created for each webhook execution.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure webhooks, Working with Webhooks, Administer, Threat Intelligence Security Center, Security Operations]
---

# View webhook batches

A webhook batch record is created for each webhook execution.

## Before you begin

Role required: admin

## About this task

In order to reduce the number of API calls sent to the webhook endpoints, batching of events is implemented in webhooks. For each webhook, if there are multiple events triggered almost during the same time, then all these events are sent as part of the same request to the webhook endpoint.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Select **Webhooks Configurations** &gt; **Webhooks**.

    The Webhooks page displays.

3.  Select the webhook.

4.  Go to **Error Logs**.

5.  View the error logs.

    The list view shows all the error logs from one particular webhook.

6.  Go to **Batch** column.

7.  Click on any **Batch ID**.

    The Webhook Batch page is displayed.

    **Note:** All the batches are stored in the table `sn_sec_tisc_webhook_batch`.

    Below is the sample payload format that the webhook end point receives:

    ```
    {
        "batch_id": "06eeb3693b6bca10f6f82a60c5e45a7b",
        "events": [
            {
                "record": "Observable",
                "record_fields": {
                    "is_false_positive": "false",
                    "reputation": "malicious",
                    "sys_updated_on": "2024-07-22T14:31:26.000Z",
                    "type": "url",
                    "sys_updated_by": "admin",
                    "sys_created_on": "2024-07-04T06:45:20.000Z",
                    "id": "url--1e77adb7eb8b06107750fa86cad0cd70",
                    "is_defanged": "false",
                    "sys_created_by": "SecCommon.System",
                    "tags": "Enriched",
                    "taxonomies": "T1: V1",
                    "domain": "urlhaus.abuse.ch",
                    "status": "active",
                    "source_count": "1",
                    "threat_score": "20",
                    "sys_id": "da77adb7eb8b06107750fa86cad0cd70",
                    "value": "https://urlhaus.abuse.ch/url/2578255/",
                    "confidence": "89",
                    "expiration_time": "2025-10-07T07:13:18.000Z",
                    "tlp": "CLEAR"
                },
                "trigger": {
                    "name": "Observable Update",
                    "type": "UPDATE",
                    "trigger_time": "2024-07-22T14:31:26.000Z",
                    "trigger_fields": [
                        {
                            "field_name": "reputation",
                            "previous_value": null,
                            "current_value": "malicious"
                        }
                    ]
                }
            },
            {
                "record": "Observable",
                "record_fields": {
                    "is_false_positive": "false",
                    "reputation": "malicious",
                    "sys_updated_on": "2024-07-22T14:31:19.000Z",
                    "type": "url",
                    "sys_updated_by": "admin",
                    "sys_created_on": "2024-07-04T06:45:20.000Z",
                    "id": "url--9a77adb7eb8b06107750fa86cad0cd6f",
                    "is_defanged": "false",
                    "sys_created_by": "SecCommon.System",
                    "tags": "Enriched",
                    "taxonomies": "T1: V1",
                    "domain": "urlhaus.abuse.ch",
                    "status": "active",
                    "source_count": "1",
                    "threat_score": "20",
                    "sys_id": "5a77adb7eb8b06107750fa86cad0cd6f",
                    "value": "https://urlhaus.abuse.ch/url/2578264/",
                    "confidence": "89",
                    "expiration_time": "2025-10-07T07:13:18.000Z",
                    "tlp": "CLEAR"
                },
                "trigger": {
                    "name": "Observable Update",
                    "type": "UPDATE",
                    "trigger_time": "2024-07-22T14:31:19.000Z",
                    "trigger_fields": [
                        {
                            "field_name": "reputation",
                            "previous_value": null,
                            "current_value": "malicious"
                        }
                    ]
                }
            }
        ]
    }
    ```

    Following table lists the batch payload structure and its attributes which will be sent to the users as webhook payload:

<table id="table_gkw_kjl_2cc"><thead><tr><th>

Parameters in Batch Payload

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

batch\_id

</td><td>

String

</td><td>

Specifies unique identifier for a batch.

</td></tr><tr><td>

events

</td><td>

Array of Objects

</td><td>

Contains an array of events which are triggered as part of that webhook. Each event will contain the snapshot of the field values at the time of event generation and also contains the trigger information.**Note:** For more information on viewing the parameters in the event object, see [Webhook Triggers](../concept/tisc-triggers.md).

</td></tr></tbody>
</table>    **Note:**

8.  Click **Retry batch** button to retry the failed batch.

    **Note:** You can also trigger the retry batch for the completed batches.


**Parent Topic:**[Configure webhooks](../concept/setup-webhooks.md)

