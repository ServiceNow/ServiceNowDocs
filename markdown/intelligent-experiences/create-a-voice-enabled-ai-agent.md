---
title: Create an AI voice agent
description: Create an AI voice agent in the AI Agent Studio to resolve cases, incidents, or tasks through the phone channel.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Deploy AI voice agents, Now Assist AI agents, Enable AI experiences]
---

# Create an AI voice agent

Create an AI voice agent in the AI Agent Studio to resolve cases, incidents, or tasks through the phone channel.

## Before you begin

Role required: sn\_voice\_aia.admin

## Procedure

1.  Navigate to the New AI Agent page in the Assistant Designer or AI Agent Studio.

<table id="table_emg_jm5_w2c"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

Navigate in Assistant Designer

</td><td>

1.  Go to the **Asset Library** and select **Create asset**.

The Create asset window appears.

2.  Select **AI Agent**.

You are redirected to the New AI Agent workflow in the AI Agent Studio.

</td></tr><tr><td>

Navigate in AI Agent Studio

</td><td>

1.  Go to **All** &gt; **AI Agent Studio** &gt; **Create and manage** and select the **AI agents** tab.
2.  In the Add drop-down list, select **Voice** to create an AI voice agent.
 ![AI agents window showing the drop-down list used to create an AI voice agent.](../image/voice-agent-select-agent-type-voice.png)

</td></tr></tbody>
</table>2.  On the New AI Agent page, describe your AI agent and provide instructions on how you want your AI agent to perform its tasks.

    Select **Generate details** to generate a description and instructions with Now Assist. If you provide the description of what you want the agent to do, you can select **Generate** to write the name, description, AI agent role, and instructions fields for you. You can change those fields after the text has been generated or try again with new instructions.

    **Note:** The more details that you provide, the more accurately your AI agent can perform.

    1.  On the form, fill in the fields.

<table id="table_mp3_4nj_zcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI agent name

</td><td>

Name of the AI agent. Provide a name according to the outcome that you want your AI agent to achieve.

 For example: Incident manager.

</td></tr><tr><td>

AI agent description

</td><td>

Brief summary of what your AI agent can do autonomously. Outline all the activities that you want your AI agent to perform.

 Example for the Incident manager: The Incident manager AI agent assists users with existing incidents by gathering information over the phone, matching it to records in the system, and sharing relevant incident details. It can also make limited updates to the incident using preconfigured tools.

</td></tr></tbody>
</table>    2.  On the form, fill in the fields.

        **Note:** The AI agent uses this information as guidance to tailor its responses and actions.

<table id="table_uj3_msj_zcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI Agent role

</td><td>

Capabilities and responsibilities for your AI agent. Roles enable your AI agent to perform its required actions.

 Example for the Incident manager: You’re an AI agent with the purpose of communicating incident details and making changes to those incidents for users calling in as long as they match the caller for those incidents. You have access to tools that can retrieve a few fields for incidents, comments, and escalate the urgency. Only proceed with gathering information and tool execution if the user and caller listed on the incident match.

</td></tr><tr><td>

List of steps

</td><td>

Necessary steps to be followed by the AI agent while carrying out its role.

**Note:** The instructions are sent to the large language model \(LLM\).

 Example for the Incident manager: Incidents are records for tracking issues and their resolution updates through a set of journal entries. Your objective is to act as an incident manager. If the user provides an incident number, verify the caller identity before sharing permitted details. If no number is given, match incidents using the short description and confirm with the user. Allow updates only if the user matches the caller. Offer live agent transfer if the user is unsatisfied.

 To resolve an incident:

1.  Verify the caller number.
2.  Search for incident records associated with the user.
3.  Consider the context and relationship between different data points.
4.  If the user provides an incident number, verify their identity against the caller field before sharing permitted details. Proceed with updates or modifications only after the caller's identity is verified.
5.  If no incident number is given, search using the short description, list matching incidents with brief summaries, and confirm which one the users wants to explore further.
6.  Only share allowed fields \(for example, incident number, caller, dates, urgency, state, short description, comments\). Summarize comments if there are more than five, and notify the user if a field is empty or restricted.
7.  If the user is unsatisfied, offer to transfer to a live agent. End the conversation politely if they’re satisfied or after a transfer.


</td></tr></tbody>
</table>        Follow these guidelines for writing effective Instructions:

        -   Define the AI agent's role:

            -   Clearly state the primary function of the AI agent in one or two sentences.
            -   Example: The AI agent acts as a customer service assistant.
        -   Outline specialties:

            -   Specify the key areas or tasks that the AI agent handles.
            -   Example: Specializes in handling inquiries and resolving customer issues.
        -   Identify the business problem:

            -   Articulate the specific business challenge for the AI agent to address.
            -   Example: Reducing customer wait times by 50%.
        -   Describe the workflow:

            -   Provide a brief scenario of how the AI agent is to be used.
            -   Example: Automating responses to common queries and escalating complex issues to human agents.
        -   Be concise and clear:

            -   Use simple and direct language.
            -   Avoid jargon and technical terms.
            -   Example: The AI agent helps customers find answers quickly.
        -   Provide actionable steps:

            -   Include specific instructions on how to set up and use the AI agent.
            -   Example: Step 1: Define the types of inquiries the AI agent handles. Step 2: Integrate the AI agent with the customer service platform.
        -   Include examples:

            -   Provide real-world examples to illustrate how the AI agent should function.
            -   Example: For example, the AI agent can automatically respond to questions about the order status.
        -   Focus on outcomes:

            -   Emphasize the benefits and outcomes of using the AI agent.
            -   Example: Using the AI agent leads to faster resolution times and higher customer satisfaction scores.
        By following these general guidelines, you can create clear and effective prompt instructions that enable you to use AI agents to their fullest potential. For more information and examples, see [General guidelines for creating AI agents](../concept/gg-creating-aia.md).

    3.  Determine if the AI agent can be accessed by third parties.

        Making your AI agent discoverable allows you to use your ServiceNow AI agent on other platforms. You can still use it on your ServiceNow instances as well.

    4.  Select **Save and continue** to move to the next step.

3.  In the **Add tools and information** tab, configure additional tools and data sources that provide capabilities necessary to your AI agent to accomplish its objectives.

    Select **Recommend Tools** for Now Assist to suggest the tools that are required for the AI agent to carry out the tasks that it's built for. Now Assist suggests tools based on the AI agent description and instructions given in the previous section.

    You can add the tools suggested by Now Assist or manually select the tools from the Add tool drop-down list. You must add at least one tool to continue setting up your AI agent, but you can also add more tools to your AI agent. The data input and output type for tools must be string for optimal voice experience.

    The following tools are available for AI voice agents:

    -   [File upload](../task/add-file-retrieval.md): Different file types such as PDF, DOCX, or TXT formats that you can add to your AI agent.
    -   [Flow action](../task/add-flow-action-ai-agent.md): Custom automated processes in your system that you can add to your AI agent. Example for the Incident manager agent: Fetch details of the incident.
    -   [Knowledge Graph](../task/add-knowledge-graph.md): Various Knowledge Graph items that you can add to you AI agent.
    -   [MCP server tool](../../model-context-protocol-client/task/add-mcp-server-tool.md): An MCP server tool that you can to your AI agent.
    -   [Record operation](../task/add-database-op-ai-agent.md): Different record operations that you can add to your AI agent.
    -   [Script](../task/add-script-ai-agent.md): Editable scripts and APIs that you can add to your AI agent.
    -   [Search retrieval](../task/add-retriever-ai-agent.md): Information retrieval processes in your system that you can add to your AI agent.

        **Note:** Create a dedicated search profile that includes only the KB articles for AI voice agents to reduce the search scope and minimize latency.

    -   [Sub flow](../task/add-sub-flow-ai-agent.md): Automated flows in your system that you can add to your AI agent.
4.  In the Define security controls tab, define who can access the AI agent and what data the AI agent has access to.

    1.  Define the users who can access this AI agent \(ACLs\).

        Choose from:

        -   **Any authenticated user**: A user who is logged in can access the AI agent.
        -   **Users with specific roles**: Users that are assigned specific roles can access the AI agent. Selecting this option enables you to select the roles in the Role drop-down list.
        -   **Public**: Anyone can access the AI agent, even without logging in.
    2.  Define the user identity of the AI agents to determine what data it has access to.

        The default selection is Dynamic user, in which the user passes their roles to the AI agent which allows the AI agent to run as the user that invokes it. The user's ACLs determine the data accessible to the AI agent.

5.  Define the availability of your AI voice agent.

    1.  Select **Allow** to enable users to use phone calls to invoke the AI agent.

    2.  In the Voice assistants field, select **Now Assist Voice Deployment** or if you configured a custom provider, select that.

    3.  Activate the AI agent by toggling the **Status**.

6.  Select **Done** to save the configuration.


