---
title: Offboarding knowledge transfer plan generation agentic workflow
description: The agentic workflow uses AI agents to identify, categorize, and transfer knowledge from departing employees to their managers and team.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/journey-designer/offboarding-knowledge-x-agentic-wf.html
release: australia
product: Journey Designer
classification: journey-designer
topic_type: concept
last_updated: "2026-02-04"
reading_time_minutes: 6
breadcrumb: [AI in Journey designer, Use, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Offboarding knowledge transfer plan generation agentic workflow

The agentic workflow uses AI agents to identify, categorize, and transfer knowledge from departing employees to their managers and team.

When employees leave an organization, they take valuable institutional knowledge with them. The offboarding knowledge transfer plan generation agentic workflow helps preserve this knowledge by performing the following actions:

-   Automatically discovering documents and resources the departing employee created
-   Organizing the retrieved documents and resources using AI-powered categorization
-   Creating tasks for managers to review and transfer critical information to remaining team members

The offboarding knowledge transfer plan generation agentic workflow integrates with Journey designer to create an AI-powered offboarding workflow. This agentic workflow operates in two phases: manager initiation and employee review. During manager initiation, an AI agent interacts with the departing employee's manager to determine whether knowledge transfer is needed and collect requirements. During employee review, a second AI agent presents the knowledge transfer content to the departing employee for review and approval before sharing with the manager.

## How offboarding knowledge transfer works

The knowledge transfer process is triggered when an employee's offboarding journey begins in Journey designer. The system triggers the first AI agent to engage with the manager through a conversational interface.

The manager-facing AI agent performs the following actions:

-   Retrieves employee and manager information from the offboarding journey record
-   Asks the manager whether knowledge transfer is needed for the departing employee
-   Collects the time range for knowledge retrieval based on manager input
-   Searches for documents that are authored by the departing employee within the specified time period
-   Creates a Knowledge Transfer record and generates Knowledge Transfer Resource records for each discovered document
-   Uses Now Assist AI to categorize the documents into meaningful groups based on content and context
-   Creates a Knowledge Transfer stage in the offboarding journey with assigned tasks
-   Provides a link to the employee journey for tracking and management

When the manager approves a knowledge transfer, the system triggers the second AI agent to engage with the departing employee. The employee-facing AI agent performs the following actions:

-   Retrieves AI-generated knowledge transfer content including work categories and resources
-   Presents the content to the employee in a structured format with resource links
-   Requests employee approval before sharing the knowledge transfer with the manager
-   Completes the knowledge transfer and notifies the manager upon employee approval

## AI agents

The offboarding knowledge transfer workflow uses two specialized AI agents that operate autonomously to complete specific tasks:

<table id="table_q3f_gsr_23c"><tbody><tr><td>

**AI agent**

</td><td>

**Description**

</td></tr><tr><td>

Offboarding knowledge transfer gather inputs AI agent

</td><td>

Interacts with managers to collect knowledge transfer requirements. Recognizes yes or no responses to proceed with the appropriate action, collects numeric values for time ranges, and tracks conversation progress to keep the interaction moving forward. Evaluates each decision point and takes appropriate actions based on manager responses.

</td></tr><tr><td>

Knowledge transfer reviewer

</td><td>

Interacts with departing employees to facilitate review and approval of AI-generated knowledge transfer content. Retrieves work summaries organized by category, displays structured information with resource links, and manages the employee consent process before sharing information with managers.

</td></tr></tbody>
</table>## Key capabilities

-   **Automated document discovery**

    The system searches across document sources to find relevant documents created by the departing employee within the specified time period.

-   **AI-powered categorization**

    Now Assist analyzes document content and automatically organizes resources into categories, making it easier for managers to understand the scope of knowledge to transfer.

-   **Journey integration**

    Knowledge transfer tasks are automatically added to the employee's offboarding journey in Journey designer, providing a structured workflow for managers.

-   **Conversational interfaces**

    Managers and employees interact with AI agents through natural conversational interfaces delivered through Now Assist in Virtual Agent.

-   **Employee consent and control**

    Employees review and approve AI-generated knowledge transfer content before sharing with managers, maintaining control over what information is shared during offboarding.

-   **Flexible sharing**

    Managers can designate specific team members to receive knowledge transfer information, ensuring the right people have access to critical expertise.

-   **State tracking**

    Knowledge transfers move through states from draft to completed, allowing administrators to monitor progress across all offboarding activities.


## Benefits

Organizations using the offboarding knowledge transfer plan generation agentic workflow gain several advantages:

-   Reduces knowledge loss when employees depart
-   Saves manager time by automating document discovery and initial categorization
-   Ensures consistent knowledge transfer processes across all offboarding activities
-   Provides visibility into knowledge transfer completion rates
-   Improves team continuity and reduces disruption from employee departures
-   Accelerates successor ramp-up with organized knowledge handoff resources

## Requirements

-   **Plugins**

    To use the offboarding knowledge transfer plan generation agentic workflow, you must install and configure the following plugins:

    -   AI Agents for HR Service Delivery \(sn\_hr\_ai\_agents\)
    -   ServiceNow Otto for HRSD \(sn\_hr\_gen\_ai\)
    -   Journey designer \(sn\_jny\)
    -   AI Search \(glide.ais\)
    -   External Content Connectors \(sn\_ext\_conn\)
    -   External Content Connectors SharePoint Online \(sn\_ext\_conn\_spo\)
-   **AI components**

    The following AI components must be activated to use this workflow:

    -   AI agents for the offboarding knowledge transfer plan generation agentic workflow
    -   Knowledge transfer document grouper skill in AI Admin Hub.
-   **Journey configuration**

    In the journey configuration for which you want to enable agentic offboarding, the following fields must be configured:

    -   The **Journey accelerator plan type** field must be set to **Agentic AI Offboarding Plan Type**.
    -   The **LE activity sets can be personalized** check box must be selected.

-   **[Add Employee Center to the ServiceNow Otto display experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-designer/enable-na-va-ec.md)**  
Enable ServiceNow Otto to appear in Employee Center to converse with AI agents in this agentic workflow.
-   **[Configure the AI agent triggers for offboarding to use Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-designer/config-offboarding-trigger-ec.md)**  
Add the Employee Center portal to the AI agent trigger configuration used in the offboarding knowledge transfer plan generation agentic workflow. This configuration change enables managers and employees to interact with AI agents through ServiceNow Otto.
-   **[Activate the Offboarding knowledge transfer trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-designer/activate-trigger-offboarding-kt.md)**  
Enable the offboarding knowledge transfer trigger to ensure that the workflow runs at the right time during the employee offboarding process. This trigger automates knowledge discovery and categorization, reduces manual effort for managers, and improves consistency in knowledge transfer processes.
-   **[Activate the Knowledge transfer record created trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-designer/activate-trigger-kt-record-created.md)**  
Enable the knowledge transfer record created trigger to ensure that the employee review workflow runs after a knowledge transfer record is generated. This trigger allows departing employees to review and approve auto-generated knowledge transfer content before sharing with their manager.
-   **[Activate the AI skill for offboarding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-designer/activate-na-skills-offboarding.md)**  
Enable the AI skill associated with the offboarding knowledge transfer plan generation agentic workflow. This skill supports automated knowledge discovery and categorization during the knowledge transfer process.
-   **[Generate offboarding knowledge transfer plans using ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-designer/generate-knowledge-xfer-na.md)**  
Managers working for organizations using the offboarding knowledge transfer plan generation agentic workflow can use to initiate a knowledge transfer request for departing employees. Once the manager confirms the request, an AI agent automatically discovers and categorizes the employee's documents into a structured knowledge transfer summary.
-   **[Review offboarding knowledge transfer summaries using Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-designer/review-knowledge-xfer-na.md)**  
Departing employees working for organizations using the offboarding knowledge transfer plan generation agentic workflow can use Now Assist in Virtual Agent to review and approve AI-generated knowledge transfer summaries. Once the employee approves the summary, it’s shared with the manager and designated team members.

**Parent Topic:**[AI in Journey designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/journey-designer/agentic-wf-jny-dsgnr-na-hrsd.md)

