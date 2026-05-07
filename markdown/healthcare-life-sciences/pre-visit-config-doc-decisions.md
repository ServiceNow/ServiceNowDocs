---
title: Configuring the auto-generation of documents for procedure requests
description: You can define the conditions for auto-generating documents for a procedure request.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Pre-Visit Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configuring the auto-generation of documents for procedure requests

You can define the conditions for auto-generating documents for a procedure request.

**Important:**

Starting with the Yokohama release, Pre-Visit Management is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

By default, privacy consent and procedure consent documents are automatically generated for procedure requests with the Pre-Visit Management workflow. However, you can create pre-filled and reusable document templates based on your workflow requirements. For more information, see [Configure document templates for Healthcare and Life Sciences Service Management Core](hcls-config-doc-templates.md).

The privacy consent document is automatically triggered for the procedure request cases. The **Select privacy consent** decision rule generates the privacy consent document when the procedure request review task is set to **Complete** by a patient service representative in the playbook for Pre-Visit Management.

As a user with the admin rule, you can configure decision tables in the Healthcare and Life Sciences Service Management Core application by navigating to **All** &gt; **HCLS Service Management** &gt; **Administration** &gt; **Document decisions**. For more information, see [Configure the auto-generation of documents for healthcare cases](hcls-config-decision-tables.md).

The procedure consent document is sent to patients using the **Send procedure consent schedule** scheduled job. By default, the scheduler sends the procedure consent document to patients three days prior to procedure appointment booking date. As a user with the sn\_previsit.admin role, you can configure the **Send procedure consent schedule** scheduled job to change the schedule. For more information, see [Configure when to send the procedure consent form to a patient](../task/pre-visit-config-proc-consent-time.md).

