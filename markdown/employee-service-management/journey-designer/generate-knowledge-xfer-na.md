---
title: Generate offboarding knowledge transfer plans using ServiceNow Otto
description: Managers working for organizations using the offboarding knowledge transfer plan generation agentic workflow can use to initiate a knowledge transfer request for departing employees. Once the manager confirms the request, an AI agent automatically discovers and categorizes the employee's documents into a structured knowledge transfer summary.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/journey-designer/generate-knowledge-xfer-na.html
release: zurich
product: Journey Designer
classification: journey-designer
topic_type: task
last_updated: "2026-03-02"
reading_time_minutes: 3
breadcrumb: [Offboarding knowledge transfer plan generation agentic workflow, AI in Journey designer, Use, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Generate offboarding knowledge transfer plans using ServiceNow Otto

Managers working for organizations using the offboarding knowledge transfer plan generation agentic workflow can use to initiate a knowledge transfer request for departing employees. Once the manager confirms the request, an AI agent automatically discovers and categorizes the employee's documents into a structured knowledge transfer summary.

## Before you begin

The following plugins must be installed and configured:

-   AI Agents for HR Service Delivery \(sn\_hr\_ai\_agents\)
-   ServiceNow Otto for HRSD \(sn\_hr\_gen\_ai\)
-   Journey designer \(sn\_jny\)
-   AI Search \(glide.ais\)
-   External Content Connectors \(sn\_ext\_conn\)
-   External Content Connectors SharePoint Online \(sn\_ext\_conn\_spo\)

**Tip:** For more information about configuring External Content Connectors for Microsoft SharePoint Online or another external content repository, see [Configuring External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/configuring-ext-cont-connectors.md).

In the journey configuration for which you want to enable agentic offboarding, the following fields must be configured:

-   The **Journey accelerator plan type** field must be set to **Agentic AI Offboarding Plan Type**.
-   The **LE activity sets can be personalized** check box must be selected.

The configuration tasks in the following topics must be completed:

-   [Add Employee Center to the ServiceNow Otto display experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-hrsd/enable-na-va-ec.md)
-   [Configure the AI agent triggers for offboarding to use Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/journey-designer/config-offboarding-trigger-ec.md)
-   [Activate the Offboarding knowledge transfer trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/journey-designer/activate-trigger-offboarding-kt.md)
-   [Activate the Knowledge transfer record created trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/journey-designer/activate-trigger-kt-record-created.md)
-   [Activate the AI skill for offboarding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/journey-designer/activate-na-skills-offboarding.md)

Role required: manager

## About this task

When an offboarding journey is created with the **Journey accelerator plan type** field set to **Agentic AI Offboarding Plan Type**, a manager receives a notification from ServiceNow Otto after they access the Employee Center. The manager is prompted to initiate a knowledge transfer for a departing employee whose offboarding journey has begun.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

    A notification from ServiceNow Otto appears.

2.  Select the Otto icon.

    ServiceNow Otto provides a message with the following information:

    -   Name of the departing employee
    -   Their departure date
    -   A prompt asking whether a knowledge transfer is needed
3.  Enter `Yes` to confirm that a knowledge transfer is needed for the departing employee.

    ServiceNow Otto prompts you to specify the time range for retrieving documents authored by the departing employee.

4.  Specify the time range in months that the AI agent should use for document retrieval.

    **Tip:** The AI agent retrieves a maximum of 25 documents by default. You can change this limit using the **sn\_jny.offboarding\_kt\_ai\_search\_max\_documents** system property.

    ServiceNow Otto generates a knowledge transfer stage that contains a work summary for the specified time range in the departing employee's offboarding journey. You’re then prompted to specify whether you want to publish the tasks associated with the knowledge transfer stage.

5.  Enter `Yes` to publish the tasks in the knowledge transfer stage generated by the AI agent.

    ServiceNow Otto outputs a message that includes the following information:

    -   A link to the offboarding journey with the published knowledge transfer stage
    -   Confirmation that the departing employee will be notified to review the knowledge transfer
    -   Confirmation that the manager will be notified when the departing employee approves and shares the knowledge transfer

## Result

The knowledge transfer request is completed. The AI agent discovers and categorizes documents authored by the departing employee within the specified time range. A knowledge transfer summary is created and the departing employee is notified to review the content.

## What to do next

The departing employee must review and approve the knowledge transfer summary before it’s shared with the manager. For more information about this process, see [Review offboarding knowledge transfer summaries using Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/journey-designer/review-knowledge-xfer-na.md).

**Parent Topic:**[Offboarding knowledge transfer plan generation agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/journey-designer/offboarding-knowledge-x-agentic-wf.md)

