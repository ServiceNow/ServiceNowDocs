---
title: Resolve issues using in-form deflection ServiceNow Otto for IT Service Management \(ITSM\)
description: Use the create incident form with ServiceNow Otto for IT Service Management \(ITSM\) to find a solution and deflect the issue without creating an incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-deflection-workflow.html
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-07-29"
reading_time_minutes: 2
keywords: [deflection, Now Assist for ITSM, self-service resolution]
breadcrumb: [In-form deflection, Use generative AI skills, ServiceNow Otto for IT Service Management \(ITSM\), IT Service Management]
---

# Resolve issues using in-form deflection ServiceNow Otto for IT Service Management \(ITSM\)

Use the create incident form with ServiceNow Otto for IT Service Management \(ITSM\) to find a solution and deflect the issue without creating an incident.

## Before you begin

To get personalized results, the user context based on hardware and location context must be configured.

Role required: none

## About this task

**Note:** ServiceNow Otto for IT Service Management \(ITSM\) classifies your description as an incident or a request. An incident description reports a problem, such as `my laptop is not working`. A request description asks for something new, such as `I need a new laptop`. This task describes the flow for an incident classification. For the request classification flow, see [Resolve requests using in-form deflection ServiceNow Otto for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-request-deflection.md).

## Procedure

1.  Access the **Create New** incident form.

    1.  Navigate to the employee portal.

    2.  Search for `Create incident with ServiceNow Otto for IT Service Management \(ITSM\)`.

2.  In the **Short description** field, enter a brief summary of your issue.

3.  In the **Please describe your issue below** field, enter a specific description of your issue.

    Specific descriptions return more relevant results. Enter a specific description, such as `my laptop is not working` rather than `computer broken`. ServiceNow Otto for IT Service Management \(ITSM\) classifies your description as an incident or a request and personalizes the results based on your hardware and location context. For resolving requests, see [Resolve requests using in-form deflection ServiceNow Otto for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-request-deflection.md).

4.  Review the search results in the **Incident search results** widget.

    ServiceNow Otto for IT Service Management \(ITSM\) displays relevant solutions from the knowledge base. The results are personalized based on your hardware such as your assigned device and location.

    \[Omitted image "now-assist-deflection-solution.png"\] Alt text: Personalized solution results for a laptop issue, showing troubleshooting steps based on the user's assigned device and location.

5.  If one of the solutions resolves your issue, select **Solution found**.

    Selecting **Solution found** closes the form and marks the issue as resolved through deflection. No incident is created. The issue is recorded as deflected.

6.  If no solution in the search results resolves your issue, provide additional details in the **Please describe your issue below** field and select **Proceed with incident creation**.

    Select **Proceed with incident creation** to create an incident record that will be assigned to an incident management team. Use this path when deflection is not applicable or when you need formal tracking and assignment.


