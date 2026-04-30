---
title: Create a context input in Recommended Actions
description: As an admin or RA author, create a context input for a context and use it in rule condition builder, resource generator input and recommendation-action mappings.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-12"
reading_time_minutes: 1
breadcrumb: [Configuring the Recommended Actions application, Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Create a context input in Recommended Actions

As an admin or RA author, create a context input for a context and use it in rule condition builder, resource generator input and recommendation-action mappings.

## Before you begin

Role required: sn\_nb\_action.next\_best\_action\_author, or admin

## About this task

After creating context inputs, you must configure the RA UIB component to pass the context input values. For more information, see [Configuring Recommended Actions UIB component for context inputs](../concept/ra-csm-dynamic-context-inputs.md#section-config-ra-ci).

**Note:**

Creating context inputs is not mandatory. You can create context inputs for a context only when you want to include or map parameters other than the context table.

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Contexts**.

2.  Open a context that you want to edit.

3.  On the Context inputs related list, select **New**.

    **Note:** The Context inputs related list appears only when a parent context is not mapped to the context. For more information on the context input configuration limitations, see [Context Input configuration limitations](../concept/ra-csm-dynamic-context-inputs.md#section-ci-config-limits).

4.  In the form, fill in the fields.

<table id="table_fvt_kgp_yfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Field type of the input such as Choice, Reference, String, List, Integer, etc.Depending on the field type that you select, you might need to configure additional settings in the related tabs. For example, if you select Reference as the field type, you need to select a reference table.

</td></tr><tr><td>

Application

</td><td>

Scoped application name.The applicable name is populated by default.

</td></tr><tr><td>

Label

</td><td>

Name of the context input.The **Column name** field is auto-filled.

</td></tr><tr><td>

Active

</td><td>

Enabling the **Active** check box makes the context input available for use in the context.

</td></tr></tbody>
</table>5.  Provide the necessary details in the related tabs.

    The related tabs that display vary based on the field type selected in the **Type** field. For more information on the data types, see [Field types reference](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

6.  Select **Save**.


## Result

The context input appears in the appropriate fields of rules, recommendations, and resource generators.

-   **Default search term** pill picker in the Contextual AI Search Config section of Context form.
-   **Advanced Condition** drop-down field of the Rule form.
-   Pill pickers in the Action inputs section of the Recommendation form.
-   **Default search term** pill picker in the Contextual AI search configuration section of the Context form.
-   Pill pickers in the Generator inputs section of the Resource generator form.

## What to do next

Use the context inputs for creating the conditions in rules, and action inputs in recommendations and generator inputs in resources generators.

