---
title: Customer Service Problem Management AI agents
description: The following agents are available for Customer Service Problem Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/cspm-ai-agents-overview.html
release: australia
topic_type: concept
last_updated: "2026-10-28"
reading_time_minutes: 3
breadcrumb: [Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Customer Service Problem Management AI agents

The following agents are available for Customer Service Problem Management.

-   **[Billing account information collector AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/tmt-billing-account-information-collector-ai-agent.md)**  
The agent retrieves the details of a billing inquiry case and uses the account number on the case to look up the matching billing account. It returns the billing account number, master plan instance number, and master plan instance description. Other AI agents use this agent to obtain billing account information.
-   **[Billing invoice data collector AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/tmt-billing-invoice-data-collector-ai-agent.md)**  
The agent retrieves the latest and previous invoices for a billing account, collects the line items on the latest invoice, and validates the pending amount. It compares the two invoice amounts and, when the latest invoice is higher, identifies the line item and the sold product behind the increase.
-   **[Customer interaction context gatherer AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/tmt-customer-interaction-context-gatherer-ai-agent.md)**  
The agent retrieves the details of a customer interaction and identifies the sold product that the interaction refers to. It gives customer service representatives the account, contact, category, status, and sold product context that they need when they troubleshoot voice quality issues.
-   **[Customer payment status AI Agent V2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/tmt-customer-payment-status-ai-agent-v2-ai-agent.md)**  
The agent checks whether a customer has outstanding payments on their account. It runs without user interaction, collecting the payment status in the background and passing the result to the orchestrator. It does not troubleshoot payments or call other agents.
-   **[Network correlation monitor AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/tmt-network-correlation-monitor-ai-agent.md)**  
The agent identifies the network services, customer accounts, and products that a network incident affects. It checks for service problem cases created recently and, with the user's approval, creates a major service problem case, links the incident and related cases to it, and creates child cases for the affected accounts.
-   **[Network remediation generation AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/tmt-network-remediation-generation-ai-agent.md)**  
The agent reads the resolution steps from the work notes of a network incident and maps each step to a task type: incident task, work order, or change request. It then creates the mapped tasks and displays a link to each one.
-   **[Network ticket actionable steps generation AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/tmt-network-ticket-actionable-steps-generation-ai-agent.md)**  
The agent generates actionable resolution steps for a network incident from similar past incidents, and falls back to generic steps when no similar incidents exist. The user can change the steps before the agent adds them to the work notes of the incident.
-   **[Network ticket resolution AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/tmt-network-ticket-resolution-ai-agent.md)**  
The agent collects the details of a network incident, analyzes the associated alert to produce a summary, and finds knowledge articles relevant to the incident. The user chooses whether to add the alert summary and the articles to the work notes of the incident.
-   **[On demand service tester AI Agent V2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/tmt-on-demand-service-tester-ai-agent-v2-ai-agent.md)**  
The agent analyzes a task by running the test groups that apply to it. It creates a diagnostic task, runs the test groups, and collects the final test run result. It returns the diagnostic task and the result to the orchestrator without displaying them to the user.
-   **[Preliminary troubleshooter AI Agent V2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/tmt-preliminary-troubleshooter-ai-agent-v2-ai-agent.md)**  
The agent triages a task by retrieving relevant knowledge articles and similar historical tasks, and consolidates them into a resolution plan with recommended next steps. It writes the plan, along with any customer payment information, to the work notes of the task.
-   **[Service repair AI agent V2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/tmt-service-repair-ai-agent-v2-ai-agent.md)**  
The agent reviews the results of a service test and creates a repair task when the test fails. It summarizes the diagnostic task, the overall test result, and any repair tasks created, and writes that summary to the work notes of the task.
-   **[Task information collector AI Agent V2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/tmt-task-information-collector-ai-agent-v2-ai-agent.md)**  
The agent gathers the details of a task and verifies that the task qualifies for further troubleshooting. It runs without user interaction, and returns the task details, the verification status, and the verification response to the orchestrator.
-   **[Telecom customer support AI voice agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/tmt-telecom-customer-support-ai-voice-agent.md)**  
The AI voice agent helps a consumer troubleshoot a broadband service issue over the phone. It validates the caller, finds their active services, and walks them through the troubleshooting steps from a knowledge article one step at a time. It can also check the contract termination status.
-   **[Ticket creation AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/tmt-ticket-creation-ai-agent.md)**  
The agent creates a service problem case for a connectivity issue. It checks that the sold product, short description, and experience profile are available, creates the case, and displays the case number with a link to the new record.
-   **[Ticket readiness AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/tmt-ticket-readiness-ai-agent.md)**  
The agent predicts the category, subcategory, assignment group, short description, and description for a network incident from similar historical incidents. It also estimates the resolution duration and retrieves the SLA duration, then updates the incident or its work notes with the recommendations the user accepts.

**Parent Topic:**[Telecommunications, Media and Technology AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/tmt-ai-agents-overview.md)

