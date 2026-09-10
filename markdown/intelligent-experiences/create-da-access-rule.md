---
title: Create a desktop action access rule
description: Configure rules to enforce security boundaries for AI agents in your organization. Resource access rules define which files, folders, websites, and applications AI Desktop Actions can access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-da-access-rule.html
release: australia
topic_type: task
last_updated: "2026-08-21"
reading_time_minutes: 3
breadcrumb: [Control resource access, Adaptive desktop actions for desktop and web, Configure, AI Desktop Actions, Enable AI experiences]
---

# Create a desktop action access rule

Configure rules to enforce security boundaries for AI agents in your organization. Resource access rules define which files, folders, websites, and applications AI Desktop Actions can access.

## Before you begin

This task must be performed in the ServiceNow instance.

Role required: sn\_aia.admin

## About this task

The Desktop action resource access rule form includes fields for configuring the rule and a Policy related list for linking the rule to policies.

\[Omitted image "da-resource-rule-form.png"\] Alt text: Desktop action resource access rule with form fields and policy related list.

For more information about the default resource access rules available with the installation of the application, see [Default policy and rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/security_policy_governance_concept.md).

## Procedure

1.  Navigate to **All** &gt; **AI Desktop Actions** &gt; **Desktop Action Access Rules**.

    Access rules can also be created from the related list of a policy record, which links the rule to that policy.

2.  Select **New**.

3.  On the Desktop action resource access rule form, fill in the fields.

<table id="table_y1z_b2w_hkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rule name

</td><td>

A descriptive name for the rule. Keep names specific to the resource or restriction so rules are easy to identify when linked to multiple policies.Example: Restrict Payroll Folder, Allow GitHub, Block Excel Files

</td></tr><tr><td>

Active

</td><td>

Option to enable or disable the rule. Only active rules are evaluated during policy checks.

</td></tr><tr><td>

Resource type

</td><td>

The type of resource this rule applies to:-   File
-   Folder
-   Website
-   Application
This determines which match type and permission options are available.

</td></tr><tr><td>

Resource access

</td><td>

Whether the rule permits or blocks access: -   **Allow**: AI agent can access the resource.
-   **Deny**: AI agent can't access the resource.
Deny rules take precedence over Allow rules. If any rule explicitly denies access to a resource, the agent can't access it, regardless of any other Allow rules.

If no rule matches a resource \(neither Allow nor Deny\), the AI agent prompts the user for the access during execution. To enforce strict security, create explicit Allow rules for only the resources AI agents should access.

 Example: If you have an Allow rule for `*.xlsx` \(allow Excel files\) and a Deny rule for `/payroll/**` \(deny payroll folder\), the AI agent can access `/documents/report.xlsx` but can't access `/payroll/report.xlsx`.

</td></tr><tr><td>

Value

</td><td>

The resource identifier \(path, URL, or app name\) to match against. The format depends on match type and resource type.Example: /payroll/\*, \*.github.com, chrome, \*/Documents/\*.pdf

</td></tr><tr><td>

Match type

</td><td>

Match types determine how the Value field is compared against actual resources on the user's system:-   **Exact**: The value must match exactly \(case-sensitive\). Use for precise, single-item restrictions.

Example:

Value: `/payroll/salaries.xlsx` matches only that exact file, not `/payroll/salaries.pdf` or `/payroll`. Value: `github.com` matches only that exact domain.

-   **Wildcard**: The value must match with patterns using wildcards. Use `*` to match any characters at the current level \(single directory or domain part\). Use `**` to match any characters recursively across multiple directory levels. Works for file paths, folders, application names, and website domains.

Example:

Value: `**/*.log` matches `/tmp/app.log`, `/var/logs/app.log`, and any .log file anywhere. Value: `*.github.com` matches `api.github.com`, `user.github.com`, but not `github.io`.

**Note:** This field does not apply to the Application resource type.

</td></tr><tr><td>

Permissions

</td><td>

The specific operations allowed:-   **Read**: The AI agent has read-only access to the resource.
-   **Create**: The AI agent can read and create the resource.
-   **Update**: The AI agent can read, create, and update the resource.
-   **Delete**: The AI agent can read, create, update and delete the resource.
**Note:** This field does not apply to the Application and Website resource type.

</td></tr><tr><td>

Description

</td><td>

Description explaining what the rule controls, why it's necessary, and what resources are affected.Example: Denies automated access to payroll folder \(/payroll/\*\). Agents can't read, write, or execute files in this location. Finance team must manually handle payroll documents.

</td></tr></tbody>
</table>4.  From the form header, select **Save**.

5.  Link the rule to the policies.

    1.  In the Policy related list, select **Edit**.

    2.  From the Collection column, select the policies to add, then move them to the Policy List column.

    3.  Select **Save**.

6.  Select **Submit**.


## What to do next

Execute adaptive desktop actions on your desktop. For more information, see [Execute adaptive desktop actions for desktop and web](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/use_ai_desktop_actions_adaptive.md).

Take manual control of automation during execution. For more information, see [Take control of AI Desktop Actions execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/control_ai_desktop_actions_execution_adaptive.md).

**Parent Topic:**[Controlling what AI Desktop Actions can access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/security_policy_governance_concept.md)

