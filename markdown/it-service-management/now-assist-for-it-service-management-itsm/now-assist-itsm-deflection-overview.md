---
title: In-form deflection in Now Assist for IT Service Management \(ITSM\)
description: In-form deflection enables users to resolve issues directly within the create incident form. When users describe an issue, Now Assist for IT Service Management \(ITSM\) searches the knowledge base and returns solutions based on the user's hardware, location, and the tone of their description.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-deflection-overview.html
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-06-24"
reading_time_minutes: 1
keywords: [deflection, Now Assist for ITSM, user context, sentiment analysis]
breadcrumb: [Use generative AI skills, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# In-form deflection in Now Assist for IT Service Management \(ITSM\)

In-form deflection enables users to resolve issues directly within the create incident form. When users describe an issue, Now Assist for IT Service Management \(ITSM\) searches the knowledge base and returns solutions based on the user's hardware, location, and the tone of their description.

In-form deflection enables end users to find resolutions without creating an incident. When a user describes an issue in the **Short description** field, Now Assist for IT Service Management \(ITSM\) searches the knowledge base and returns relevant solutions tailored to that specific user's context.

## In-form deflection process

When you enter an issue description, the system performs the following enhancements to the search process:

-   User context embedding: The system fetches your location and hardware information from the knowledge graph and rephrases your query to include this context. For example, `my laptop is not working` is set to `MacBook Pro is not working` if your hardware is a MacBook Pro.
-   Sentiment analysis: The system detects the tone of your description. If the description indicates frustration, the response reflects that tone and prioritizes solutions accordingly.

## In-form deflection benefits

Using in-form deflection reduces incident volume and enables users to resolve issues quickly:

-   Get personalized solutions specific to your hardware and location.
-   Resolve issues immediately without waiting for incident assignment.
-   Receive responses that reflect the tone of your description and prioritize relevant solutions.
-   Skip incident creation when a self-service solution is available.

## User context application

User context is applied based on your issue type. When your issue relates to hardware or location, the system rephrases your query to include this information. When your issue is generic, such as "what is Outlook," the system returns generic results without modifying the query, because the context is not relevant to the question.

