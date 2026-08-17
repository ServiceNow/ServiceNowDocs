---
title: Configure custom skills and rules
description: Create and manage custom skills and rules, or instructions to control how Build Agent behaves during a session. Rules are preloaded into every session automatically. Skills are available on demand when you or the agent invokes them by name.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ba-configure-custom-skills-rules.html
release: australia
topic_type: task
last_updated: "2026-08-03"
reading_time_minutes: 4
keywords: [custom skills, custom rules, build agent, configure, instructions, Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Build Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Configure custom skills and rules

Create and manage custom skills and rules, or instructions to control how Build Agent behaves during a session. Rules are preloaded into every session automatically. Skills are available on demand when you or the agent invokes them by name.

## Before you begin

You must be on Australia Patch 5 or later to work with custom skills and rules.

Role required: admin

## About this task

Both skills and rules are stored as records in the Build Agent Instruction table. Each record has a type that determines how Build Agent loads the instruction during a session.

-   Use skills to provide task-specific guidance that Build Agent can use when needed. For example, internal guidelines for creating a specific type of record or handling a particular workflow pattern.
-   Use rules to enforce consistent behavior every time the agent runs. For example, naming conventions, required fields, or organizational standards.

Each skill or rule instruction has an **Applies To** setting that controls which Build Agent sessions can use it. The coverage levels from broadest to narrowest are as follows:

-   **Instance**

    Applies to all Build Agent sessions on the instance. Instance-level instructions take the highest precedence.

-   **Application**

    Applies only when Build Agent is working within a record's application scope. Use application-level instructions to provide guidance specific to one scoped application.

-   **User**

    Applies only to sessions for the user who created the instruction. User-level instructions are stored separately from instance and application instructions.


**Note:** Check your entitlements to determine whether you have access to custom skills and rules in Build Agent.

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow Studio** or **All** &gt; **App Development** &gt; **ServiceNow IDE**.

2.  Select the Settings icon \[Omitted image "ba-settings-icon.png"\] Alt text: in the Build Agent chat panel.

    \[Omitted image "ba-settings-panel-1.png"\] Alt text: Build Agent panel showing greeting message and the Settings button

3.  Select the tab for the type of instruction you're creating.

    -   Select the **Skills** tab to create a custom skill.
    -   Select the **Rules** tab to create a custom rule.
4.  On the form, fill in the fields.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the instruction. Maximum 100 characters.

</td></tr><tr><td>

Type

</td><td>

Defines the type of instruction.-   Select **Skill** for on-demand guidance
-   Select **Rule** to apply the instruction automatically to every session


</td></tr><tr><td>

Applies To

</td><td>

Controls which Build Agent sessions use the instruction.-   Select **Instance** to apply to all sessions on the instance
-   Select **Application** to apply only when the session is in the record's application scope
-   Select **Me** to apply the instruction only to you


</td></tr><tr><td>

Active

</td><td>

Availability of the instruction for use. Selected by default.

</td></tr><tr><td>

Description

</td><td>

Description of what the skill or rule does. Maximum 1,000 characters.

</td></tr><tr><td>

Instructions for Build Agent

</td><td>

Instruction text that Build Agent follows. Plain text only, maximum 65,000 characters. Writing instructions in clear, structured prose helps Build Agent interpret the guidance accurately.

</td></tr></tbody>
</table>    Some example instructions are:

    -   Rules:
        -   `reuse_before_create`

            `Check for existing artifacts before generating new ones. Before creating a table, field, business rule, script include, flow, or UI action, search the instance for something that already covers the requirement. Prefer extending an approved existing artifact over creating a near-duplicate. If a close match exists, tell me about it and wait before proceeding.`

        -   `naming_convention`

            `Use our application prefix. All tables and fields you create use our approved prefix followed by the application short name. Match existing naming in the app you're working in rather than introducing a new pattern.`

    -   Skill:

        `security_review`

        `Audit the app for access control and risky patterns. Review the current application and report on tables with missing or overly broad ACLs, client scripts using GlideRecord, scripts running with elevated privileges they don't need, and roles granted more broadly than the workflow requires. For each finding, give the artifact name, the risk in one sentence, and the change you recommend. don't make changes. Report only.`

    \[Omitted image "ba-new-custom-rule.png"\] Alt text: New rule editor form with Name, Type, Applies To, Active, Description, and Instructions for Build Agent fields, alongside the Rules settings panel listing existing custom rules with toggle switches.

5.  Select **Save**.

    The new skill or rule appears in the settings panel list. The panel updates automatically to reflect the change.

6.  Edit an existing instruction by selecting its Open rule record icon.

    Make changes to the instruction, then select **Save**.

    \[Omitted image "ba-instruction-edit.png"\] Alt text: Rules panel showing two rule cards with toggles and edit icons

7.  Enable or disable an instruction by selecting its toggle.

    \[Omitted image "ba-instruction-toggle.png"\] Alt text: Skills tab showing the toggle enabled for the add\_comments skill, highlighted with a purple box.


## What to do next

Active rules get dynamically loaded per turn in a Build Agent session, so they're available immediately. Active skills are available immediately on demand during a session.

**Parent Topic:**[Build Agent configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/configure-build-agent.md)

