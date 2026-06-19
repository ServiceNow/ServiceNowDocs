---
title: Configure Data Discovery patterns
description: Configure a Data Discovery pattern and review current patterns. A Data Discovery pattern defines the regular expression used to match data against a target table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-discovery/configure-data-discovery-patterns.html
release: australia
product: Data Discovery
classification: data-discovery
topic_type: task
last_updated: "2026-05-04"
reading_time_minutes: 3
breadcrumb: [Data Discovery jobs, Exploring Data Discovery \(Classic\), Data Discovery, Platform Privacy]
---

# Configure Data Discovery patterns

Configure a Data Discovery pattern and review current patterns. A Data Discovery pattern defines the regular expression used to match data against a target table.

## Before you begin

Role required: data\_discovery\_admin

## About this task

Custom Data Discovery patterns can be used with Now Assist anonymization in addition to the base system patterns provided with the platform. A pattern applies to Now Assist prompts when it is associated with the **Generative AI** data channel. Base system patterns that don't include "\(Generative AI\)" in their name can also apply to Now Assist, provided they are associated with the **Generative AI** data channel. Configured patterns apply consistently across Now Assist skills, Now Assist Virtual Agent, AI Agents, and custom skills built with the Now Assist Skill Kit.

**Note:** Data Privacy for Now Assist is available in Yokohama and later releases. On Xanadu instances, use the Sensitive Data Handler to mask sensitive data for generative AI.

**Important:** Now Assist anonymization uses two-way masking. When a Now Assist skill such as incident summarization processes a record, sensitive data matching an active pattern is replaced with placeholder tokens in the prompt sent to the large language model \(LLM\). The original values are then restored in the response returned to the end user. End users therefore see unmasked data in Now Assist responses; this is by design. The purpose of masking is to prevent sensitive data from being transmitted to the LLM, not to hide it from the end user in the final response.

## Procedure

1.  Navigate to **System Security** &gt; **Data Discovery** &gt; **All Data Patterns**.

2.  In the Data Discovery Pattern list, select **New**.

3.  In the Data Discovery job fields form, fill in the fields.

<table id="table_tgp_2pb_grb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Internal Scope

</td><td>

Scope of the pattern.

</td></tr><tr><td>

Description

</td><td>

Description of the job.

</td></tr><tr><td>

Name

</td><td>

Name of the data pattern.

</td></tr><tr><td>

Application

</td><td>

Application scope of pattern.

</td></tr><tr><td>

Expression

</td><td>

Regular expression used to discover the data pattern. **Note:** Expression length must be less than 1000 characters.

</td></tr><tr><td>

Keyword\(Optional\)

</td><td>

A specific word\(or words separated by comma\) to be searched for around a expression. Must be used with **Keyword Proximity****Note:** A keyword can be used to search for additional context for a pattern. For example, using keyword can help differentiate between a date of birth or a date of hire given they have the same MM/DD/YY formatting.

</td></tr><tr><td>

Keyword Proximity\(Optional\)

</td><td>

How far from the expression to search for keywords. Must be used with **Keyword****Note:** Default is 30, upper bound of 64

</td></tr><tr><td>

Privacy technique configuration

</td><td>

The masking technique applied to matched data before it is sent to the LLM. Common techniques include: -   **Synthetic replacement**

Replaces the matched value with a realistic but fictitious substitute \(for example, substituting a different email address\). Use when the LLM needs plausible values to maintain response quality.

-   **Static replacement**

Replaces the matched value with a fixed non-inferable placeholder \(for example, replacing any SSN with "999-99-9999"\).

-   **Selective replacement with x**

Obscures part or all of the value using wildcard characters \(for example, masking most digits of a card number while retaining the last four\). Use when partial visibility is acceptable and helps the LLM understand context.

-   **Remove**

Deletes the matched value from the prompt entirely.

</td></tr><tr><td>

Synthetic Value

</td><td>

List of values substituted for the patterns

</td></tr><tr><td>

Type

</td><td>

Type of pattern-   **Local**: The pattern is regex-based
-   **Model**: Uses AI/ML service


</td></tr></tbody>
</table>4.  Select **Submit**.

    -   The **Test** button enables you to test your regular expression before submitting the data pattern list.
5.  The data pattern must be set as active to be used with scheduled jobs.
6.  Navigate to **System Security** &gt; **Data Discovery** &gt; **Active Data Patterns**.

7.  In the Data Discovery Active Pattern list, select **Edit**.

8.  Select the pattern list from **Available Lists** and move it to **Selected Lists**.


