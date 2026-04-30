---
title: Define subflows for success plays
description: Before you create a success play, you must define a subflow and add it to the Definition Records table.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a success play, Basic setup, Customer success, Configure, Customer Success Management]
---

# Define subflows for success plays

Before you create a success play, you must define a subflow and add it to the Definition Records table.

For instructions on creating a subflow, see [Create a flow, subflow, or action in Workflow Studio](https://www.servicenow.com/docs/access?context=create-acl-flowdesigner&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US). After you have created the subflow, follow these steps to add it to the Definition Records table.

1.  Navigate to **All** and enter `sn_acct_lc_definition_record.list` in the Search filter.
2.  In the Definition Records page, click **New**.
3.  In the form, fill the fields.

<table id="table_w24_qff_1cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Flow

</td><td>

Select the subflow you have created.

</td></tr><tr><td>

Category

</td><td>

Select the category with which the subflow is to be associated.

</td></tr><tr><td>

State

</td><td>

The state of the definition record. This can be:-   Draft
-   Published
-   Closed
-   Cancelled


</td></tr><tr><td>

Title

</td><td>

Enter a title for this definition record.

</td></tr><tr><td>

Description

</td><td>

Enter a description for this definition record.

</td></tr></tbody>
</table>4.  Click **Submit**.

**Parent Topic:**[Create a success play](account-lifecycle-create-success-play.md)

