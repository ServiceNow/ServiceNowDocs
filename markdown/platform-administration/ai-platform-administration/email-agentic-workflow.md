---
title: Email Intent to Action Agentic Workflow
description: The Email agentic workflow automates inbound email processing by intelligently interpreting requests, extracting required information, performing actions, and generating responses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-platform-administration/email-agentic-workflow.html
release: zurich
product: AI Platform Administration
classification: ai-platform-administration
topic_type: concept
last_updated: "2025-11-13"
reading_time_minutes: 5
breadcrumb: [Use agentic workflows in emails, Now Assist in Notifications, Configure core features, Administer]
---

# Email Intent to Action Agentic Workflow

The Email agentic workflow automates inbound email processing by intelligently interpreting requests, extracting required information, performing actions, and generating responses.

## Email request types

The Email agentic workflow intelligently processes and responds to inbound email requests, which are categorized into two types for appropriate automated handling:

-   Workflow executions: These emails contain requests where the system identifies one or more intents that trigger predefined automated workflows. This enables execution of custom processes based on the email content.
-   Information queries: For these requests, the system acts as an intelligent assistant, answering questions by using default AI search profile that can be mapped to existing information sources.

The workflow identifies and processes one or more intents from a single inbound email, evaluating each identified intent independently.

## Intent to action driven email processing

The foundation of an intelligent email automation lies in accurately interpreting the purpose of an incoming email and executing the appropriate actions. This process is driven by Intent to Action mapping.

-   Intent: The underlying purpose or request expressed in an incoming email. A single email can contain multiple intents, each representing a distinct request \(for example, "approve my leave" or "answer my question"\).
-   Action: The specific task or process that the system executes in response to a successfully identified intent.

Admins configure intents to enable the system to recognize and process different types of requests. The system identifies all relevant intents in an inbound email, matches them to preconfigured intents, and maps each intent to its corresponding actions.

Once an intent is identified, a corresponding action is triggered. Each intent can have one or more configured actions, such as executing workflows or sending reply emails. For inbound emails containing multiple intents, the system executes the configured actions for each identified intent independently. Actions include:

-   Subflows: These are predefined workflows that execute a series of steps relevant to the matched intent. For example, a "leave approval" intent might trigger a subflow to initiate an approval process.
-   Reply Emails: In some cases, the action involves sending an automated email response back to the sender. For example, an acknowledgment or a direct answer containing extracted information.

**Note:** A crucial aspect of this system is handling emails that don’t match any preconfigured intents. For such cases, a Default Intent Action \(also referred to as a no intent action\) is executed. This default action can be configured by administrators. This fallback process is designed so that every email gets a response, whether it's a generic one like making a note for later manual review or sending a standard confirmation or an acknowledgment.

The system's framework continuously analyzes incoming emails, identifies their intents, and performs the associated actions, providing a structured and automated approach to managing diverse email requests.

## Email Agents

Email agents automate the triage and processing of inbound email requests by identifying intents, executing actions, and generating appropriate email responses.

The email agentic workflow is powered by specialized AI agents, each responsible for intelligently processing and responding to inbound emails. These agents work together to understand and manage requests, execute actions, and generate communications.

1.  **Intent Identification Agent**

    This agent acts as the initial brain of the workflow and identifies one or more intents in the inbound email request using LLMs. It uses these advanced LLMs to analyze the content of an inbound email, deciphering its underlying intents. Once identified, these intents are then mapped to their corresponding preconfigured and customized intents within the system.

    The Intent Identification Agent functions include:

    -   Intelligent Intent Recognition: Using LLMs to understand natural language and identify one or more user requests.
    -   Custom Intent Mapping: Linking recognized intents to specific, user-defined categories or actions. This enables flexibility and tailors it to the unique business needs.
    -   Action Association: Identifying intents with a variety of subsequent actions.
2.  **Intent Executor Agent**

    Once the Intent Identification Agent has determined the email's purpose, the Intent Executor Agent takes over. Its role is to carry out the instructions associated with each identified intent. This involves extracting any crucial data points from the email \(for example order numbers, customer IDs, specific requests\) and then executing the corresponding actions or workflows.

    The Intent Executor Agent functions include:

    -   Input Extraction: Identifying and extracting critical information from the email content needed for subsequent actions.
    -   Action Execution: Triggering and managing the execution of the predefined workflows or actions configured for each identified intent.
    -   Default Action Handling: Providing a fallback mechanism by executing a default action if an email's intents can’t be matched to any specific custom intent, confirming no request goes unaddressed.
    When required inputs can't be extracted from an inbound email, the system handles missing inputs using configurable execution modes. The behavior is controlled by the system property **sn\_notif\_agents.missing\_inputs\_execution\_mode**.

    -   Type: Choice list
    -   Default: request\_missing\_inputs
    The following execution modes are supported for handling missing inputs:

    -   **request\_missing\_inputs**: Stops execution of all intent actions and sends a reply email to the sender requesting missing inputs.
    -   **skip\_intents\_with\_missing\_inputs**: Skips intent actions that are missing mandatory inputs and executes the remaining intent actions. If all identified intents are skipped, the system automatically falls back to the default behavior.
    -   **execute\_all\_intents**: Executes all intent actions regardless of missing inputs. Missing inputs are passed as empty strings, and downstream workflows determine how to handle them. No reply email is generated.
    **Note:** Once the intent is finalized, this information will be used to retrieve any relevant actions.

3.  **Email Generator Agent**

    The Email Generator Agent is responsible for generating clear, concise, and relevant email responses. It takes inputs from the inbound email, including the identified intents, and extracted information to generate a suitable reply. The context, tone, and goals for drafting emails can be configured by administrators. The responses generated by the Email Generator Agent are based on the reply email actions configured for one or more intents. As a result, one or more responses can be generated for a single email.

    The Email Generator Agent functions include:

    -   Contextual Response Generation: Using all available information and context to create highly relevant and personalized email responses.
    -   Draft Creation \(Supervised\): Generating email drafts that can be reviewed and approved by a human agent before sending, enabling oversight and quality control.
    -   Automated Sending \(Unsupervised\): For routine or low-risk requests, the agent can be configured to automatically send emails without human intervention, significantly boosting efficiency.

The Email Generator Agent supports a configurable **Email template** field that enables responses to be generated using predefined email templates. These templates help maintain consistency in branding, layout, and formatting of AI-generated emails.

-   **[General guidelines for creating and mapping an intent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/guidelines-creating-intent.md)**  
By following some general guidelines for creating email intents and mapping actions to intents, you can create clear and effective instructions that help maximize the efficiency and effectiveness.

**Parent Topic:**[Use email agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/use-agentic-ai-notifications.md)

