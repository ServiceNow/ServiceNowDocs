---
title: Enroll in the Model Preview Program
description: Give your organization early access to AI models before they're generally available by accepting the Model Preview Program terms on an eligible instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/aict-configure-model-preview-program.html
release: australia
topic_type: task
last_updated: "2026-11-02"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring AI model providers, Configuring ServiceNow AI settings, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Enroll in the Model Preview Program

Give your organization early access to AI models before they're generally available by accepting the Model Preview Program terms on an eligible instance.

## Before you begin

**Important:** You can't turn off the Model Preview Program from the instance after you enroll and save.

Role required: sn\_ai\_governance.ai\_steward or admin

Your instance must be eligible for the program. On instances that aren't eligible, the program doesn't appear on the **AI model providers** tab. For eligibility, see [Configuring AI model providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-ai-model-providers.md).

## About this task

Enrollment is a global setting that data routing preferences don't affect. After you enroll, your allowed providers and fallback setting still apply to preview models.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **ServiceNow AI**.

2.  Select the **AI model providers** tab.

3.  Select **Edit**.

4.  In the **Model preview program** section, turn on the toggle.

    The **Model preview program - Terms of Service** dialog box opens. The toggle stays off until you accept the terms.

5.  To read the full terms, select the **Terms of Service** link.

6.  Select the **I have read and agree to the Terms of Service** check box.

7.  Select **Enable Model preview program**.

    The toggle turns on. Until you save, you can still turn it off.

8.  Select **Save**.

9.  In the **Save changes?** dialog box, select **Save**.


## Result

Your instance is enrolled in the Model Preview Program, and the toggle is locked on. Eligible preview models become available to AI applications on your instance, subject to your allowed providers and fallback setting.

**Parent Topic:**[Configuring AI model providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-ai-model-providers.md)

