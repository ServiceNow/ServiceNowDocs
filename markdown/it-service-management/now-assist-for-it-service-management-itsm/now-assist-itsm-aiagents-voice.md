---
title: Agentic AI in the Voice application
description: Use the Voice AI agents to create and manage tickets for any IT service-related issues such as troubleshooting WiFi connections with voice calls.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Agentic AI in the Voice application

Use the Voice AI agents to create and manage tickets for any IT service-related issues such as troubleshooting WiFi connections with voice calls.

The Request catalog item with Voice AI agent video is an example that shows how to use a demo Voice AI agent.Demo Request catalog item with Voice AI agent 

## Managing IT-related issues using Voice AI agents

Using the Now Assist for ITSM Voice AI agents, you can do the following:

-   Create incidents and manage tickets using voice calls.
-   Use generic queries such as, "Is there an update to my ticket from yesterday?" or "What's the status of my VPN ticket?" and get responses in the context of your questions.
-   Escalate a ticket to a higher priority or add a comment to the ticket.

To modify the Voice AI agents, duplicate it, and adjust the settings according to your requirements.

**Important:**

-   When you modify an AI agent, or a tool, make sure that you update all instructions accordingly.
-   In the Define availability screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

**Note:** The Voice AI agents are installed with the IT Service Management AI voice agent collection application \(sn\_itsm\_voice\_aia\).

|Voice AI agent|Voice AI agent role|
|--------------|-------------------|
|Create incidents with voice AI agent|Creates an incident using voice.|
|Manage tickets with voice AI agent|Manages tickets using voice.|

**Note:** When you install the IT Service Management AI voice agent collection application \(sn\_itsm\_voice\_aia\) along with the demo data, you can activate the agents that are primers equipped with the essentials that you can expand on for your use cases.

<table id="table_idk_bcm_vgc"><thead><tr><th>

Voice AI agent primers

</th><th>

Voice AI agent role

</th></tr></thead><tbody><tr><td>

Request catalog item with voice AI agent

</td><td>

-   For software-related categories, the AI agent submits the requested item for the user.
-   For non-software categories, the AI agent emails a catalog item link to the user to submit the item.

</td></tr><tr><td>

Password reset with voice AI agent

</td><td>

Fetches the information to reset your password in one of the following ways:-   Provides the instructions from the knowledge article to reset the password in an email.
-   Provide the reset password link by SMS.
-   Reads out the URL for the reset password by voice.

</td></tr><tr><td>

Troubleshoot Outlook issue with voice AI agent

</td><td>

Searches the knowledge base to troubleshoot outlook issues. The AI agent can also email relevant links to troubleshooting articles and instructions to users.

</td></tr><tr><td>

Submit account unlock catalog with voice AI agent

</td><td>

Creates and submits a catalog item when a user requests their account to be unlocked.

</td></tr></tbody>
</table>## Creating Voice AI agents to search knowledge articles

You can use Voice AI agents to get answers to your questions or resolve issues using knowledge base articles.

For Voice AI agents to search knowledge base articles:

1.  Define the knowledge base articles.
2.  Define the search profile in AI search to search the knowledge base articles. For information on AI search, see Search profiles in AI Search
3.  Create the search retrieval tool to use the search profile in the Voice AI agent. For information on search retrieval, see Add a search retrieval to an AI agent

