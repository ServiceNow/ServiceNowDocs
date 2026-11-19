---
title: Resolve requests using in-form deflection ServiceNow Otto for IT Service Management \(ITSM\)
description: Use the create incident form with ServiceNow Otto for IT Service Management \(ITSM\) to receive a personalized catalog item recommendation when your description is classified as a request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-request-deflection.html
release: zurich
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-07-29"
reading_time_minutes: 2
keywords: [deflection, Now Assist for ITSM, request classification, catalog item]
breadcrumb: [In-form deflection, Use generative AI skills, ServiceNow Otto for IT Service Management \(ITSM\), IT Service Management]
---

# Resolve requests using in-form deflection ServiceNow Otto for IT Service Management \(ITSM\)

Use the create incident form with ServiceNow Otto for IT Service Management \(ITSM\) to receive a personalized catalog item recommendation when your description is classified as a request.

## Before you begin

To get personalized results, the user context based on hardware and location context must be configured.

Role required: none

## About this task

**Note:** ServiceNow Otto for IT Service Management \(ITSM\) classifies your description as a request when you ask for something new rather than report a problem, such as `I need a new laptop` or `I need new headphones`. For the incident classification flow, see [Resolve issues using in-form deflection ServiceNow Otto for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-deflection-workflow.md).

## Procedure

1.  Access the **Create New** incident form.

    1.  Navigate to the employee portal.

    2.  Search for `Create incident with ServiceNow Otto for IT Service Management \(ITSM\)`.

2.  In the **Short description** field, enter a brief summary of your issue.

3.  In the **Please describe your issue below** field, describe what you need.

    Describe what you need, such as `I need a new laptop` rather than `my laptop is not working`. ServiceNow Otto for IT Service Management \(ITSM\) classifies your description as a request and personalizes the recommendation based on your assigned hardware and location context.

4.  Review the recommended catalog item in the **Incident search results** widget.

    For a request classification, ServiceNow Otto for IT Service Management \(ITSM\) suggests a catalog item matched to your assigned hardware, such as a compatible replacement laptop.

    \[Omitted image "now-assist-deflection-request-result.png"\] Alt text: Personalized catalog item recommendation for a headphone request, based on the user's assigned hardware.

5.  Select the recommended catalog item link to open the request form.

    Complete and submit the request form to order the item.

6.  If the recommended catalog item resolves your need, select **Solution found**.

    Selecting **Solution found** closes the form and marks the issue as resolved through deflection. No incident is created. The issue is recorded as deflected.

7.  If the recommended catalog item doesn't meet your need, provide additional details in the **Please describe your issue below** field and select **Proceed with incident creation**.

    Select **Proceed with incident creation** to create an incident record that will be assigned to an incident management team. Use this path when deflection is not applicable or when you need formal tracking and assignment.


