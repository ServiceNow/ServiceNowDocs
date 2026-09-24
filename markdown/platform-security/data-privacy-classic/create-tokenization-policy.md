---
title: Create a tokenization policy
description: Create a new tokenization policy to define which sensitive data should be anonymized through reversible tokenization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-privacy-classic/create-tokenization-policy.html
release: brazil
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
breadcrumb: [Tokenization, Data privacy, Data Privacy, Platform Privacy]
---

# Create a tokenization policy

Create a new tokenization policy to define which sensitive data should be anonymized through reversible tokenization.

## Before you begin

Before you begin, ensure you have:

-   Access to the Data Privacy module
-   Permissions to create tokenization policies
-   Identified the sensitive data entities and patterns you want to tokenize
-   Knowledge of which roles should have detokenization permissions

Role required: data\_privacy\_admin and admin

## Procedure

1.  Navigate to **System Security** &gt; **Data Privacy** &gt; **Tokenization**.

2.  Click **Create tokenization policy**.

    The policy creation form opens, presenting the policy details section.

3.  Enter a descriptive name for the tokenization policy.

    Use a name that clearly identifies what data is being tokenized, such as "Customer SSN Tokenization" or "Medical Record Numbers".

4.  Define the policy scope by selecting the table\(s\) and column name\(s\) that should be tokenized.

    You can select one or multiple tables and columns. Tokenization will apply only to those specified.

5.  Specify which roles are allowed to access de-tokenized \(original\) values.

    Only users with these roles can see the original sensitive data. Others see only the tokenized values.

6.  Select **Continue** to open the **Select child tables** page.

7.  If your deployment includes child tables with related sensitive data, configure child table tokenization settings.

    You can choose to tokenize child table data independently, with the same policy, or not at all.

8.  Select **Continue** to open the **Data patterns** page.

9.  Define the data patterns to be tokenized.

    1.  Select one or more data patterns that match the sensitive data in your selected fields \(e.g., Credit Card, Social Security Number, Email Address\).

    2.  Configure pattern-specific settings if available \(e.g., pattern matching options, special character handling\).

    Data patterns define what constitutes sensitive data within the fields you selected. You can use built-in patterns or create custom patterns.

10. Click **Save** to save the policy as a draft.

    The policy is created but not yet active. It appears in the policy list with a "Draft" status.

11. When ready, click **Publish** to activate the tokenization policy.

    Once published, the policy begins tokenizing data according to its configuration.


