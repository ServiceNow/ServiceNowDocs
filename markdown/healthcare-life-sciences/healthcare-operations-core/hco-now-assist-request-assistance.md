---
title: Request care team assistance agentic workflow
description: Initiate a structured case intake process. Collect all necessary information to create and log a support case for proper tracking and resolution by using the Request care team assistance agentic workflow inthe Care Team Operations AI Chat Assistant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/healthcare-operations-core/hco-now-assist-request-assistance.html
release: brazil
product: Healthcare Operations Core
classification: healthcare-operations-core
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Create requests with ServiceNow Otto, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Request care team assistance agentic workflow

Initiate a structured case intake process. Collect all necessary information to create and log a support case for proper tracking and resolution by using the **Request care team assistance** agentic workflow inthe Care Team Operations AI Chat Assistant.

## Before you begin

Role required: sn\_hco.care\_team\_member or sn\_hco.care\_team\_manager

## About this task

When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

This agentic workflow creates support requests of varying case types that are then sent to support departments for fulfillment.

The following Care Team Operations plugins contain the case types for this agentic workflow:

-   Care Team Operations for Biomed
-   Care Team Operations for Environmental Services
-   Care Team Operations for Facilities
-   Care Team Operations for Healthcare IT

## Procedure

1.  Open the **Care Team Operations AI Chat Assistant**: in Care Team Portal, open the ServiceNow Otto panel; in Care Team Mobile, select the assistant's tab in the navigation bar.

2.  Select **Request care team assistance**.

3.  Describe one or more support requests in detail.

4.  Respond to any questions asked by the Care team operations case intake AI agent to provide more context as needed.

5.  Reply to the AI agent.

    -   If the AI agent displays correct information for all support cases, reply **Yes**.
    -   If information displayed isn’t correct, respond **No** and provide additional information until the correct request information is captured.

## Result

After confirming all request details are correct, the Care team operations case creation AI agent creates one or more cases for supporting service departments as needed. Case information will display in card form and you can select the case number to navigate directly to the case within Care Team Portal.

Cases created are fulfilled by users with the Support Agent role in the Healthcare Operations Workspace.

**Note:** Upon conclusion of conversation,the Care Team Operations AI Chat Assistant creates an interaction record, which can be viewed within your instance at any time.

