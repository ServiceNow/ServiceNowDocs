---
title: Configuring the auto-generation of documents for enrollment requests
description: You can define the conditions for auto-generating documents for an enrollment request.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Patient Support Services, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configuring the auto-generation of documents for enrollment requests

You can define the conditions for auto-generating documents for an enrollment request.

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

By default, privacy consent document is automatically generated for enrollment requests with the Patient Support Services workflow. However, you can create pre-filled and reusable document templates based on your workflow requirements. For more information, see [Configure document templates for Healthcare and Life Sciences Service Management Core](hcls-config-doc-templates.md).

The privacy consent document is automatically triggered for the enrollment cases. The **Select privacy consent** decision rule generates the privacy consent document when the enrollment request review task is set to **Complete** by a care coordinator in the playbook for Patient Support Services.

As a user with the admin rule, you can configure decision tables for enrollment request documents in the Healthcare and Life Sciences Service Management Core application by navigating to **All** &gt; **HCLS Service Management** &gt; **Administration** &gt; **Document decisions**. For more information, see [Configure the auto-generation of documents for healthcare cases](hcls-config-decision-tables.md).

