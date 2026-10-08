---
title: Categorize domain usage
description: Group the domains that users visit in your environment by business relevance, such as AI tools, productivity applications, or security services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/agent-client-collector/acc-discover-ai-domain-usage.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Domain usage discovery and categorization, ACC deployment - endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Categorize domain usage

Group the domains that users visit in your environment by business relevance, such as AI tools, productivity applications, or security services.

## Before you begin

Verify the Agent Client Collector for Visibility \(ACC-VC\) VISC Get URL metrics policy is active to enable domain usage discovery to classify any domains. For more information, see [Agent Client Collector for Visibility Content default checks and policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-visibility-checks-policies.md).

Role required: discovery\_admin

## About this task

Domain usage discovery relies on how you categorize domains. To identify usage of a website or an application, create a domain signature and assign it to a category.

## Procedure

1.  Create a category.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

    2.  Open the **Entity Categories** \(`sn_acc_vis_content_entity_category`\) list and select **New**.

    3.  On the form, fill in the fields.

<table id="table_ofk_gnh_lkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The display name of the category. This field is required.For example: AI Tools, Productivity, or Microsoft.

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the category to help identify it.

</td></tr><tr><td>

Active

</td><td>

Option to activate the category.**Note:** You can also activate a saved category later from the **Entity Categories** list.

</td></tr></tbody>
</table>    4.  Select **Save**.

    5.  View the saved categories in the **Entity Categories** list.

        You can activate saved categories from this list by setting Active=true for the relevant categories.

2.  Create a signature.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

    2.  Open the **URL Domain Signature** \(`sn_acc_vis_content_url_domain_signature`\) table.

    3.  Under related links, select **Show List**.

    4.  Select **New**.

    5.  On the form, fill in the fields.

<table id="table_whr_m4h_lkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Domain type

</td><td>

The display name of the signature. The options are: External or Internal.

</td></tr><tr><td>

Category

</td><td>

The category to which the system assigns matching domains. For example, AI Tools. This field is required.

</td></tr><tr><td>

URL domain

</td><td>

The pattern to match against the URL domain. This field is required

</td></tr><tr><td>

Description

</td><td>

Option to add a brief description of the signature to help identify it.

</td></tr><tr><td>

Active

</td><td>

Option to activate the signature.

</td></tr></tbody>
</table>    6.  Select **Submit**.

    Saving the signature starts a job that evaluates the visited domains against the signature and categorizes any matches.


**Parent Topic:**[Domain usage discovery and categorization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-ai-domain-usage-discovery.md)

