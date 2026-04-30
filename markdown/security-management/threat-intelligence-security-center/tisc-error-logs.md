---
title: View webhook error logs
description: Use this error logs section to view all the audit entries which are marked as error in the status for a particular webhook.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure webhooks, Working with Webhooks, Administer Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# View webhook error logs

Use this error logs section to view all the audit entries which are marked as error in the status for a particular webhook.

## Before you begin

Role required: sn\_sec\_tisc.admin

## About this task

The audit logs enables the users to further investigate, debug the execution, and identify the root cause of the execution failure.

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

    **Note:** Each error log is associated to a batch and using the batch ID \(from the Batch column\) you can view the associated batch record. Click on any of the batch ID and this will open in a separate tab. Each batch ID contains the webhook batch number, error message, response status code, retry count, actual payload data, and the list of events which will be sent to the webhook.

8.  Click **Retry batch** to retry the failed batches.

    When you click on this button, this sends a request payload \(of that particular batch information\) to the configured webhook endpoint.

    **Note:** This action is available only for the batch records which has the execution errors or completed successfully and the records those are in retry state will be automatically retried.


**Parent Topic:**[Configure webhooks](setup-webhooks.md)

