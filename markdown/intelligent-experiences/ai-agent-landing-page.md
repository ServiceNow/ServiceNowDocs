---
title: Available AI agents on the ServiceNow AI Platform
description: All ServiceNow AI agents are listed. Depending on your license, not all AI agents may appear in your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-agent-landing-page.html
release: australia
topic_type: concept
last_updated: "2026-05-29"
reading_time_minutes: 1
breadcrumb: [AI assets, Enable AI experiences]
---

# Available AI agents on the ServiceNow AI Platform

All ServiceNow® AI agents are listed. Depending on your license, not all AI agents may appear in your instance.

## Prerequisites and setup

To access an AI agent, you must have either the appropriate ServiceNow Otto plugins installed or have access to the appropriate pricing tier. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

## Role masking

AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with your applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aia.md).

In the data access settings, you must also add the necessary roles to enable reading of the tables for the records you want to evaluate for readiness. For example, you can add the itil role to the AI agent's list of approved roles so that it can access Incident records.

## AI agents as users

When a Virtual Agent conversation is triggered, any updates or comments in the record's work notes display as the AI agent rather than the user who initiated the conversation.

## Accessing an AI agent

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Go to the **AI Agents** tab.
3.  Select the name of an agent.

