---
title: Using the ACL explainer AI agent
description: Ask the ACL Explainer AI agent about an access control list \(ACL\), a table, a field, or another resource in everyday language. Sample prompts and examples show how to phrase questions and the responses to expect.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/access-control/acl-explainer-ai-agent-using.html
release: australia
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2026-10-16"
reading_time_minutes: 4
breadcrumb: [Explore Access Control Lists, Access Control Lists \(ACLs\), Access Management]
---

# Using the ACL explainer AI agent

Ask the ACL Explainer AI agent about an access control list \(ACL\), a table, a field, or another resource in everyday language. Sample prompts and examples show how to phrase questions and the responses to expect.

Your wording doesn't have to match the sample prompts. The agent uses the names that you provide, such as an ACL name, table, field, or resource name. Explanations include rules inherited from parent tables, which can help you troubleshoot access. The agent also flags ACLs that exist but are inactive.

Remember that the agent is read-only. It can't update or delete an ACL or change ACL evaluation logic. For more information on how the agent is configured, see .

## Prerequisites

Activate the agent in AI Agent Studio.

To run the agent, you must have the admin or access\_analyzer\_admin role.

## Sample prompts for a single ACL

The following table lists sample prompts and results for a specific ACL.

<table><thead><tr><th>

Prompt

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Explain this ACL

</td><td>

Explains the ACL that you have open in ServiceNow.

</td></tr><tr><td>

Explain acl 8cdd4d2053753210d90aef0910e5e658

</td><td>

Explains the ACL with that sys\_id.

</td></tr><tr><td>

Explain the write ACL for incident.state

</td><td>

Interprets incident.state as the resource and write as the operation.

</td></tr><tr><td>

What does the \*.name ACL do?

</td><td>

Explains the rule for every field named "name" on every table.

</td></tr><tr><td>

Walk me through the script in this ACL

</td><td>

Provides a step-by-step walkthrough of the script, with notes on its complexity and performance.

</td></tr></tbody>
</table>## Decode an unfamiliar ACL script

You open an ACL that you didn't write and enter `Explain this ACL`. The agent explains what the rule controls, for whom, and why.

The ACL includes a script that you want to understand. You enter `Walk me through the script in this ACL`. The agent returns a step-by-step explanation in plain English, with notes on the script's complexity and performance. To ask about one part of the ACL only, enter a follow-up prompt such as `What roles does this ACL need?`.

## Sample prompts for ACLs on a table

The following table lists sample prompts and results for the ACLs on a table.

<table><thead><tr><th>

Prompt

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Explain ACLs of incident table

</td><td>

Includes rules inherited from the task table and prompts you to choose an operation to explain.

</td></tr><tr><td>

Explain read ACLs of incident table

</td><td>

Describes the evaluation order, then the combined roles, conditions, and scripts.

</td></tr><tr><td>

Explain the deny unless read ACLs on incident

</td><td>

Filters the results to Deny-Unless ACLs. Filters for Allow-If, wildcard, and inherited ACLs work the same way.

</td></tr></tbody>
</table>## Explore the ACLs on a table

You want to know what controls access to incident records.

In the ServiceNow Otto panel, you enter `Explain ACLs of incident table`. The agent lists each operation with its number of ACLs, including rules inherited from the task table, and prompts you to choose an operation.

You choose the read operation. The agent describes the evaluation order for the read ACLs, then the combined roles, conditions, and scripts.

You then enter `Can an admin bypass it?`. Because the agent retains the table and operation, it answers only that part of your question and doesn't repeat the full explanation.

## Sample prompts for ACLs on a field

The following table lists sample prompts and results for ACLs on a field.

<table><thead><tr><th>

Prompt

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Explain field ACLs of incident table

</td><td>

Lists the field operations with the number of ACLs for each, then explains the operation that you choose.

</td></tr><tr><td>

Give the query\_range ACLs applied to sys\_user\_group.name

</td><td>

Explains the query\_range ACLs that are evaluated for the name field on the sys\_user\_group table.

</td></tr><tr><td>

What does task.\* ACL mean and where is it applicable?

</td><td>

Explains the task.\* ACL and the tables and fields that it applies to.

</td></tr></tbody>
</table>## Find the rule in force for a field

You enter `How is writing controlled on the priority field of incident?`. The agent follows the field hierarchy to find the rule that applies.

If no incident.priority ACL exists, the agent explains the task.priority ACL instead, because the incident table inherits it from the task table. The agent links to the ACL record so that you can verify the rule. If a more specific rule exists but is inactive, the agent flags it.

## Check who can search on a field

You enter `Who can search on the short_description field of change_request?`. The agent explains the query\_range ACLs on the field, which control who can filter and search on it.

## Sample prompts for ACLs on non-table resources

Some resources, such as GraphQL schemas, web services, and flows, don't have an ACL with their own name. The ACL that is referenced in the resource definition protects them. Enter the name of the resource, and the agent finds and explains that ACL. The agent also covers UI pages and processors.

The following table lists sample prompts and results for ACLs on resources that aren't tables.

<table><thead><tr><th>

Prompt

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Show me ACL for Agent Chat Dynamic Translation

</td><td>

Explains the ACL configured in a GraphQL schema definition.

</td></tr><tr><td>

Show me ACL for ACE Contents

</td><td>

Explains the ACL configured in a web service definition.

</td></tr><tr><td>

Show me ACL for Get topics data for user

</td><td>

Explains the ACL configured for a flow or action.

</td></tr><tr><td>

Explain acl for Record Summarization

</td><td>

Explains the ACL on a REST endpoint.

</td></tr></tbody>
</table>