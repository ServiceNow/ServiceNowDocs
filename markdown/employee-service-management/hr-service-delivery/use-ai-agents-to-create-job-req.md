---
title: Use AI agents to create job requisition
description: Use AI agents to automate the job requisition creation process from the Virtual Agent chat window and use the inputs from the hiring manager to create a refined job requisition.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [AI agents, Agentic AI]
breadcrumb: [Use, Hiring tab, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Use AI agents to create job requisition

Use AI agents to automate the job requisition creation process from the Virtual Agent chat window and use the inputs from the hiring manager to create a refined job requisition.

To be able to use the AI agents from the Virtual Agent chat window, you must configure them first. For information, see .

|AI Agent|Role|
|--------|----|
|Job requisition creation leader AI agent|Invokes the other agents in sequence, based on the user input.|
|Hiring requirement gathering AI agent|Fetches prefilled values configured in the catalog questions and collects job title and location from the hiring manager. It checks for a job requisition, with similar role and title, last opened by the hiring manager. If found, it asks the hiring manager if that can be used and fills in the values accordingly.|
|Hiring requirements refinement AI agent|Asks the hiring manager if they want to hire a candidate with similar skills to that of an existing candidate. If yes, it fetches the required skills, preferred skills, and maximum education of the existing candidate and prefills it. For any details that’s not available, it seeks information from the hiring manager to finalize the requirements.|
|Job description creation AI agent|Fetches job description, if available, from existing job requisition fetched by the Hiring requirement gathering AI agent. It also fetches the job description templates configured in the Template table. After fetching this information, it presents the available options to the user to choose from. They can choose to either reuse, modify, or create a job description. The job requisition is then created and its link is shared with the hiring manager.|

**Parent Topic:**[Using Hiring](use-hiring.md)

