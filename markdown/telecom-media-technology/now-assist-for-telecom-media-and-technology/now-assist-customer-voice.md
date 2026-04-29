---
title: Now Assist for Telecommunications, Media and Technology \(TMT\) Customer voice quality issue resolution agentic workflow
description: Use this agentic workflow to resolve customer voice quality issues.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customer Service Problem Management, Use agentic workflows, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Now Assist for Telecommunications, Media and Technology \(TMT\) Customer voice quality issue resolution agentic workflow

Use this agentic workflow to resolve customer voice quality issues.

## Customer voice quality issue resolution agentic workflow overview

This agentic workflow gathers customer information, collects the subscriber experience profile from RADCOM, and creates a service problem case. By integrating RADCOM's AI agents with ServiceNow AI agents, wireless providers can link subscriber details with key service performance metrics. This integration enables swift resolution of service issues and reduces churn rates.

This agentic workflow is triggered when a new interaction is created in the CSM Interaction record under the following conditions:

-   Type: Phone or Chat
-   Category: Network

**Note:** The Customer voice quality issue resolution agentic workflow is available in read-only mode. Before using the workflow, you must make a copy and adjust the settings according to your requirements. See [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for details.

## Role masking

Required role: sn\_sprb\_mgmt.agent

Agentic workflows and their AI agents use [role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Application dependency

The Customer voice quality issue resolution agentic workflow has the following dependencies:

-   Customer Service \(sn\_customerservice\)
-   Customer Service Problem Management z\(sn\_sprb\_mgmt\)

## Configure the Customer voice quality issue resolution agentic workflow

This agentic workflow requires a third-party agent, the RADCOM ticket handling agent, to retrieve the customer experience profile. To use the third-party agent, you must create an external agent by following the steps listed in the  section.

## Test the agentic workflow

To access the use case testing page:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
2.  On the Overview page, select **Customer voice quality issue resolution**.

To test the use case, see [Manually test the execution of an agentic workflow](https://www.servicenow.com/docs/access?context=test-aia-use-case&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## AI agents used in the Customer voice quality issue resolution agentic workflow

The following AI agents are used to execute the instructions for the agentic workflow.

<table id="table_wxl_gns_fgc"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Customer interaction context gatherer AI agent

</td><td>

-   Retrieves and analyzes customer interaction data.
-   Provides detailed contextual information regarding customer communication patterns, product usage history, and relevant troubleshooting information.

</td></tr><tr><td>

RADCOM ticket handling AI agent \(external agent\)

</td><td>

Retrieves subscriber profile including network usage patterns, service quality metrics, and customer behavior insights.

</td></tr><tr><td>

Ticket creation AI agent

</td><td>

-   Identifies duplicate records, determines case type, and verifies documents.
-   Checks existing cases and creates a new case.

</td></tr></tbody>
</table>