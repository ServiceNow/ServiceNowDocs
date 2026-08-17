---
title: Service Exchange Knowledge Assistant agentic workflow
description: Use the Service Exchange Knowledge Assistant agentic workflow to get answers to Service Exchange questions directly in ServiceNow Otto.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-service-exchange-assistant-se.html
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2026-07-02"
reading_time_minutes: 1
breadcrumb: [Service Exchange, Use agentic workflows, ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\), Telecommunications, Media, and Technology \(TMT\)]
---

# Service Exchange Knowledge Assistant agentic workflow

Use the Service Exchange Knowledge Assistant agentic workflow to get answers to Service Exchange questions directly in ServiceNow Otto.

## Service Exchange Knowledge Assistant agentic workflow overview

The Service Exchange Knowledge Assistant agentic workflow helps users get answers to their Service Exchange related questions. Answers are grounded in documentation and knowledge articles that match the Service Exchange version installed on the instance. The workflow provides source links for every answer so users can verify the underlying documentation. To access this workflow, you must have the `sn_sb.admin` role.

To modify the Service Exchange Knowledge Assistant agentic workflow, you must duplicate the workflow and adjust the settings according to your requirements. For more information, see [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md).

You can initiate the workflow from the Now Assist panel by entering your question. For more information on the Now Assist panel, see [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md).

## Access the Service Exchange Knowledge Assistant agentic workflow

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select Service Exchange Knowledge Assistant.

To create an agentic workflow, see [Create an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-use-case-ai-agents.md).

## Test the Service Exchange Knowledge Assistant agentic workflow

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
2.  On the Overview page, select **Test AI reasoning**.
3.  Select the agentic workflow and version, and select **Start test**.

To test the use case, see [Manually test the execution of an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-use-case.md).

## AI agents and their role in the Service Exchange Knowledge Assistant agentic workflow

The following AI agents are used to execute the instructions for the Service Exchange Knowledge Assistant agentic workflow.

To create an AI agent, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-next-best-action-agent.md).

|AI agent|AI agent role|
|--------|-------------|
|Service Exchange Knowledge Assistant|This AI agent answers Service Exchange questions using documentation and knowledge articles curated for the Service Exchange version installed on the instance. It also cites the source documentation used to generate each answer.|

