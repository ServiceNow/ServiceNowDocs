---
title: Link Subflow and Payload to External Queues
description: Link the subflow and the payload to your external queue to complete external routing.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Link Subflow and Payload to External Queues

Link the subflow and the payload to your external queue to complete external routing.

## Before you begin

Role required: admin

## Procedure

1.  On your ServiceNow instance, navigate to **All** &gt; **Advanced Work Assignment** &gt; **Queues** and select your Queue.

2.  On your Queue form, check the **External** field checkbox.

3.  In the External third-party provider section, select the provider you chose while creating the payload.

    For more information, see [Create a payload for external third-party providers](create-payload-extrnl-provider.md)

    If you need any additional information, add it in the `additionalParams` of the payload script, and select the added params from the **Document Fields to include** slush bucket.

4.  From the FDIH Dashboard, select **Test**.

    While you want to test your flow action, ensure that you select the HTTP\(s\) Connection you configured previously, the Resource Path URL for the third-party external provider, and provide the sample payload.

5.  In the script to run the FD, provide the necessary Work Item ID and the interaction sys\_id.

6.  Verify that you have the third-party external provider URL in the outbound HTTP logs after testing.

    Open the third-party external CCaaS provider and verify the transaction logs for the endpoint.


## What to do next

You can perform a quick setup test using the demo data by connecting to your external provider. For more information, see [Define external routing test implementation](../concept/define-extrnl-routng-plugin.md).

**Parent Topic:**[Configuring Advanced Work Assignment](installing-awa.md)

