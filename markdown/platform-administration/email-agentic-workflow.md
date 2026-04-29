---
title: Email Intent to Action Agentic Workflow
description: Email agentic workflow automates inbound emails by intelligently interpreting requests, extracting information, performing necessary actions, and drafting responses.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use agentic workflows in emails, Now Assist in Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Email Intent to Action Agentic Workflow

Email agentic workflow automates inbound emails by intelligently interpreting requests, extracting information, performing necessary actions, and drafting responses.

## Email request types

The Email agentic workflow is designed for intelligently processing and responding to various inbound email requests. It categorizes these requests into two types for appropriate automated handling:

-   Workflow executions: These emails contain requests where the system identifies a specific intent that triggers a predefined, automated workflow. This enables for the execution of custom processes based on the email's content.
-   Information queries: For these requests, the system acts as an intelligent assistant, answering questions by leveraging default AI search profile that can be mapped to existing information sources.

## Intent to action driven email processing

The foundation of an intelligent email automation system lies in its ability to accurately interpret the purpose of an incoming email and execute the appropriate action. This process is driven by Intent to Action mapping.

-   Intent: The underlying purpose or request expressed in an incoming email. It's what the sender wants to achieve \(for example "approve my leave," "answer my question"\). Admins define these intents. The system's framework attempts to match incoming emails to these predefined intents.
-   Action: The specific task or process that the system executes in response to a successfully identified intent.

An Intent represents the underlying purpose or request conveyed in an inbound email. These intents are predefined and configured by administrators, enabling the system to recognize specific types of requests, such as a "leave approval" or a "query about a specific topic." The system uses a framework to match incoming emails to these configured intents.

Once an intent is identified, a corresponding Action is triggered. An action is the specific task or process that the system performs to fulfill the email's request. Actions can take various forms:

-   Subflows: These are predefined workflows that execute a series of steps relevant to the matched intent. For example, a "leave approval" intent might trigger a subflow to initiate an approval process.
-   Reply Emails: In some cases, the action involves sending an automated email response back to the sender. For example, an acknowledgment or a direct answer containing extracted information.

**Note:** A crucial aspect of this system is handling emails that don’t match any preconfigured intents. For such cases, a Default Intent Action \(also referred to as a no intent action\) is executed. This default action can be configured by administrators. This fallback process is designed so that every email gets a response, whether it's a generic one like making a note for later manual review or sending a standard confirmation or an acknowledgment

Basically, the system's framework continuously analyzes incoming emails, identifies their intent, and performs the associated action, providing a structured and automated approach to managing diverse email requests.

## Email Agents

Email agents help automate triaging of tasks that are created via inbound emails by identifying intent, executing actions, and drafting appropriate email responses.

The email agentic workflow is powered by specialized AI agents, each responsible for intelligently processing and responding to inbound emails. These agents work together to understand and manage requests, execute actions, and generate appropriate communications.

1.  **Intent Identification Agent**

    This agent acts as the initial brain of the workflow and identifies the intent of inbound email requests using LLM \(LLMs\). It uses these advanced LLM \(LLMs\) to analyze the content of an inbound email, deciphering its underlying intent. Once identified, this intent is then mapped to a preconfigured and customized intent within the system.

    The Intent Identification Agent functions include:

    -   Intelligent Intent Recognition: Using LLMs to understand natural language and identify the user goal.
    -   Custom Intent Mapping: Linking recognized intents to specific, user-defined categories or actions. This enables flexibility and tailors it to the unique business needs.
    -   Action Association: Identifying intents with a variety of subsequent actions.
2.  **Intent Executor Agent**

    Once the Intent Identification Agent has determined the email's purpose, the Intent Executor Agent takes over. Its role is to carry out the instructions associated with the identified intent, this involves extracting any crucial data points from the email \(for example order numbers, customer IDs, specific requests\) and then executing the corresponding actions or workflows.

    The Intent Executor Agent functions include:

    -   Input Extraction: Identifying and extracting critical information from the email content needed for subsequent actions.
    -   Action Execution: Triggering and managing the execution of the predefined workflows or actions linked to the identified intent.
    -   Default Action Handling: Providing a fallback mechanism by executing a default action if an email's intent can’t be matched to any specific custom intent, confirming no request goes unaddressed.
    **Note:** Once the intent is finalized, this information will be used to retrieve any relevant actions.

3.  **Email Generator Agent**

    The Email Generator Agent is responsible for crafting clear, concise, and relevant email responses. It takes inputs from the inbound email, including the identified intent, and extracted information to formulate a suitable reply. The context, tone and goals for drafting emails can be configured by administrators.

    The Email Generator Agent functions include:

    -   Contextual Response Generation: Using all available information and context to create highly relevant and personalized email responses.
    -   Draft Creation \(Supervised\): Generating email drafts that can be reviewed and approved by a human agent before sending, enabling oversight and quality control.
    -   Automated Sending \(Unsupervised\): For routine or low-risk requests, the agent can be configured to automatically send emails without human intervention, significantly boosting efficiency.

