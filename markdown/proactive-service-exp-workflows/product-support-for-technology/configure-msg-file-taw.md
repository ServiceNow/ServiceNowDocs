---
title: Customize message files for Proactive Service Experience Workflows
description: Customize the messages that provide instructions to the network engineers that are working on network-initiated issues for different subcategories, levels of escalation, and personas in Proactive Service Experience Workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/proactive-service-exp-workflows/product-support-for-technology/configure-msg-file-taw.html
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Messages in escalation workflows, Use, Proactive Service Experience Workflows, Product Support for Technology]
---

# Customize message files for Proactive Service Experience Workflows

Customize the messages that provide instructions to the network engineers that are working on network-initiated issues for different subcategories, levels of escalation, and personas in Proactive Service Experience Workflows.

## Before you begin

Role required: admin

## About this task

Each subflow in Proactive Service Experience Workflows references a message file that provides instructions for agents to use to troubleshoot, escalate, and resolve network-initiated incidents. You can use the default message text, or customize the text for your internal troubleshooting processes.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Messages**.

2.  Search for key values that contain `sd_wan`.

3.  Select the record with the text that you want to customize.

4.  In the **Message** field, provide instructions for that subflow's subcategory, persona, and level of escalation.

5.  Select **Update**.


**Parent Topic:**[About messages used in escalation workflows in Proactive Service Experience Workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/product-support-for-technology/psew-about-msgs.md)

