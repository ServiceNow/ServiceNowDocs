---
title: Navigation Assistant AI voice agent
description: The Navigation Assistant AI voice agent provides employees with verbal, step-by-step guidance for HR self-service tasks.
locale: en-US
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [HR AI voice agents, Use agentic workflows, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Navigation Assistant AI voice agent

The Navigation Assistant AI voice agent provides employees with verbal, step-by-step guidance for HR self-service tasks.

The Navigation Assistant is an AI-powered voice agent designed to provide real-time, verbal guidance to employees to help them navigate HR self-service tasks within the Employee Center. The agent delivers step-by-step instructions for processes, such as requesting employment verification for a loan application.

The agent is highly responsive to user input. Employees can request the agent to repeat a step, to start the process over entirely, or to seek clarification if they are unable to perform a specific step.

Interaction features:

-   **Live Agent Transfer:** In alignment with all AI Voice agents, the employee can request to be transferred to a live agent at any point during the interaction for additional support.
-   **Automated Email Follow-up:** The Navigation Assistant automatically sends the Knowledge Base instructions via email to the employee for offline reference.
-   **Session Management:** To optimize system resources, each call is subject to an automatic timeout and will end after ten minutes of activity.

## Knowledge sourcing

To maintain accuracy, the Navigation Assistant utilizes Knowledge Base articles within the ServiceNow® instance as the sole source of truth. The agent does not synthesize or summarize information. It verbalizes the steps exactly as they are written in the Knowledge Base article.

## Knowledge Base article requirements

For the Navigation Assistant to perform at an optimal level, content creators should follow these standards when drafting or updating HR Knowledge Base articles:

-   **Explicit Step Sequencing:** All procedural content must be presented in a numbered list format. Bulleted lists are not supported for step-by-step guidance, as the agent relies on numerical sequencing to maintain the flow of the verbal interaction.
-   **Descriptive Titling:** Article titles must be highly descriptive and keyword-rich. This ensures the agent can accurately identify and retrieve the most relevant article in response to a specific employee query.
-   **Plain Text:** Articles must avoid the use of special characters, including currency symbols \(e.g., use "USD" or "dollars" instead of "$"\). Special characters can lead to unpredictable verbalization by the AI voice engine.
-   **Verbatim Verbalization:** The agent provides a direct verbal read-out of the text. It will not perform summarization. Content creators must ensure that articles are concise and free of redundant or repetitive information, as the agent will verbalize every word as written.

