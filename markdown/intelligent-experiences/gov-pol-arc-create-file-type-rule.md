---
title: Create a file type rule for an Arc policy
description: Keep sensitive file types out of reach of ServiceNow Arc by setting whether the agent can read, write, or not access files with specific extensions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-pol-arc-create-file-type-rule.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, file type rule, file extensions, file access, arc policies]
breadcrumb: [Working with Arc policy rules, Managing Arc policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Create a file type rule for an Arc policy

Keep sensitive file types out of reach of ServiceNow Arc by setting whether the agent can read, write, or not access files with specific extensions.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward and sn\_app\_arc.admin

## About this task

Arc checks file type rules before it reads or changes a file. Only the extensions you list are restricted.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Govern** &gt; **Policies** &gt; **Arc policies**.

2.  Select the policy you want to update.

3.  Select the **File types** tab.

4.  Select **Create file types**.

    If the policy already has file type rules, select **+ Add rule** instead.

5.  On the form, fill in the fields.

<table id="table_file_type_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Rule Name**

</td><td>

Name that describes what the rule does, for example, Block spreadsheets or Allow PDF documents.

</td></tr><tr><td>

**Priority**

</td><td>

Order in which rules are evaluated when more than one rule covers the same extension. A lower number is evaluated first. The default is 100. Give deny rules lower numbers than allow rules, so a deny isn't overridden by a broader allow.

</td></tr><tr><td>

**Active**

</td><td>

Option to enforce the rule. Selected by default. An inactive rule is left out of the policy for every policy that links it.

</td></tr><tr><td>

**File Extensions**

</td><td>

Extensions the rule covers, separated by commas and without the leading dot, for example, `xls,xlsx,xlsm` or `pdf,docx,doc`. Enter `*` to cover every extension.

</td></tr><tr><td>

**Access Mode**

</td><td>

What the agent can do with matching files.

 -   **__Allow Read Only__**

The agent can open and read the files but can't change them.

-   **__Allow Read &amp; Write__**

The agent can read, write, edit, and delete the files.

-   **__Deny — hard block all access__**

The agent can't read or change the files. This is the default.

</td></tr><tr><td>

**Description**

</td><td>

Compliance reason for the rule, kept for your audit trail, for example, Block spreadsheet access to prevent exposure of personal data.

</td></tr></tbody>
</table>6.  Select **Create**.


## Result

The rule appears on the policy's **File types** tab, and Arc applies it for the users the policy covers at their next policy sync.

## Example: Keep private keys and certificates out of reach

Developers sometimes keep private keys and certificate bundles in their project folders. To make sure Arc never reads or changes them, create a file type rule with the following values:

-   **Rule Name**: `Block keys and certificates`
-   **File Extensions**: `pem,key,p12,pfx`
-   **Access Mode**: **Deny — hard block all access**
-   **Description**: `Prevent agent access to private keys and certificate stores.`

Enter the extensions without the leading dot and separate them with commas. The agent can still work with every other file in the project.

