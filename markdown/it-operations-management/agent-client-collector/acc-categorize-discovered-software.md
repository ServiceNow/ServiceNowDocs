---
title: Categorize discovered software
description: Group discovered installed software packages in your environment by business relevance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/acc-categorize-discovered-software.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 2
keywords: [software categorization, Agent Client Collector, signature, discovered software]
breadcrumb: [Software packages categorization, ACC deployment - endpoints, Agent Client Collector, IT Operations Management]
---

# Categorize discovered software

Group discovered installed software packages in your environment by business relevance.

## Before you begin

In the System Properties, verify that the software categorization system property is set to true: `sn_acc_vis_content.sw_categorization.enabled=true`.

Role required: discovery\_admin

## About this task

Software categorization classifies discovered software packages into categories, such as AI tools, security software, communication software, or a publisher-based category. Use this procedure to define a category and a signature that matches discovered software to that category.

## Procedure

1.  Create a category.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

    2.  Open the **Entity Categories** \(sn\_acc\_vis\_content\_entity\_category\) table.

    3.  Under related links, select **Show List**.

    4.  Select **New**.

    5.  On the form, fill in the fields.

<table id="table_utr_pxf_lkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The display name of the category. This field is required.For example: Adobe Acrobat, AI Tools, or Microsoft.

</td></tr><tr><td>

Description

</td><td>

Brief description of the category.

</td></tr><tr><td>

Active

</td><td>

When selected, activates the category. **Note:** You can also activate a saved category later from the **Entity Categories** table.

</td></tr></tbody>
</table>    6.  Select **Submit**.

    7.  View the saved categories in the **Entity Categories** table.

        **Note:** You can activate saved categories from this table by setting Active=true for the relevant categories.

2.  Create a signature.

    The signature is a rule that matches software to a category based on the software name or publisher.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

    2.  Open the **Installed Software Signature** \(sn\_acc\_vis\_content\_sw\_install\_signature\) table.

    3.  Under related links, select **Show List**.

    4.  Select **New**.

    5.  On the form, fill in the fields.

        Define the match condition using the software name, publisher, or both. Either the software name or the publisher is required.

<table id="table_d5c_byf_lkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The display name of the signature. This field is required.For example: ChatGPT.

</td></tr><tr><td>

Category

</td><td>

Category assigned to matching software.For example: AI Tools.

</td></tr><tr><td>

Software name condition

</td><td>

Matching condition for the software name. Options are: Exact match, Contains, Starts with, and Ends with.

</td></tr><tr><td>

Software name

</td><td>

Pattern to match against the software name. Defining either Software name or Publisher is required.For example: ChatGPT.

</td></tr><tr><td>

Publisher condition

</td><td>

Matching condition for the publisher.Options are: Exact match, Contains, Starts with, and Ends with.

</td></tr><tr><td>

Publisher

</td><td>

Pattern to match against the publisher. Defining either Publisher or Software name is required.

</td></tr><tr><td>

Version condition

</td><td>

Matching condition for the version. Options are: Any version, Exact match, Starts with, Ends with, Contains, Less than, Greater than, Not empty, and Empty.

</td></tr><tr><td>

Version

</td><td>

Pattern to match against the version.**Note:** If you don't specify a version, the signature matches any version.

</td></tr><tr><td>

Description

</td><td>

Brief description of the signature.

</td></tr><tr><td>

Active

</td><td>

When selected, activates the signature.

</td></tr></tbody>
</table>    6.  Select **Submit**.

    Submitting the signature triggers evaluation of the installed software against it and categorization of any matches.


## Result

The categorized software appears in the **Installed Software Catalogs** \(sn\_acc\_vis\_content\_sw\_install\_catalog\) table. Each entry in the table shows the software package, its assigned category, and the signature that matched. For each record, either the **Software package** or the **SAM discovery model** column is populated, depending on whether SAM is installed on the instance. Filter by category to see all the software in the group.

