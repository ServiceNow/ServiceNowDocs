---
title: Opt out of data sharing
description: Stop your instance from contributing data that ServiceNow uses to improve its AI models and products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/aict-configure-opt-out-data-sharing.html
release: australia
topic_type: task
last_updated: "2026-11-02"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring data controls, Configuring ServiceNow AI settings, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Opt out of data sharing

Stop your instance from contributing data that ServiceNow uses to improve its AI models and products.

## Before you begin

**Important:** You can't opt back in from the instance. To reactivate data sharing after you opt out, you must work with your account executive or Customer Service and Support.

Role required: sn\_ai\_governance.ai\_steward or admin

## About this task

Opting out doesn't affect your instance's access to AI features. Your instance stops contributing the inputs, outputs, and related data that ServiceNow uses to improve its AI products.

The setting applies to one instance. If multi-instance management is configured, opt out on the production instance, because the setting is read-only on sub-prod instances. Otherwise, repeat this task on each instance that uses AI features.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **ServiceNow AI**.

2.  Select the **Data controls** tab.

3.  On the **Data Sharing** card, select **Opt out**.

    To review how ServiceNow uses shared data before you decide, select **FAQs** on the card.

4.  In the confirmation dialog box, select **Opt out**.


## Result

The **Data Sharing** card shows a status of **Inactive**, and the **Opt out** button no longer appears.

**Parent Topic:**[Configuring data controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-data-controls.md)

