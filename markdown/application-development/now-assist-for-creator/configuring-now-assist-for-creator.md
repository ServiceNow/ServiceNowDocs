---
title: Configuring ServiceNow Otto for Creator
description: To get started using ServiceNow Otto for Creator, install ServiceNow Otto for Creator. Then turn on the skills, AI agents, or agentic workflows that you want to use.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/now-assist-for-creator/configuring-now-assist-for-creator.html
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-07-28"
reading_time_minutes: 2
keywords: [Configure ServiceNow Otto for Creator, ServiceNow Otto for Creator, Now Assist, Now Assist for Creator, create with Now Assist, Configure Now Assist for Creator, Install Now Assist for Creator, Creator Workflow, Creator Pro Plus, Build Agent, Flow generation, App generation]
breadcrumb: [ServiceNow Otto for Creator, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Configuring ServiceNow Otto for Creator

To get started using ServiceNow Otto for Creator, install ServiceNow Otto for Creator. Then turn on the skills, AI agents, or agentic workflows that you want to use.

## Installing ServiceNow Otto for Creator

Check your company's entitlements to verify that you have access to ServiceNow Otto for Creator. To start using ServiceNow Otto for Creator, you must request it from the ServiceNow® Store. Once approval has been granted, you can install it on your instance. See [Install ServiceNow Otto for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/install-now-assist-for-creator.md) for more information.

## Activating AI capabilities

After installing ServiceNow Otto for Creator, you must turn on the AI capabilities that you want to use. Some AI capabilities are turned on by default, such as the ServiceNow Otto for Code skills, including code assist summarization, code assist edit, and code assist generation, and code assist autocomplete. Capabilities that aren't on by default must be turned on or activated in order to use them.

You can turn on ServiceNow Otto for Creator skills in the AI Admin Hub. When you turn on a skill, you might have to complete additional configuration steps, such as assigning roles and restrictions for who can access the skill. See the product documentation for the skill that you want to activate for additional configuration steps.

AI agents and agentic workflows are activated in AI Agent Studio. When you activate an AI agent or agentic workflow, you might have to complete additional configuration steps, such as selecting a large language model \(LLM\) for the AI agent or agentic workflow and assigning roles and restrictions. See the product documentation for the AI agent or agentic workflow that you want to activate for additional configuration steps.

## Required roles

To use ServiceNow Otto for Creator, you might need specific roles. Some roles are specific to the tool that the capability is embedded in, such as catalog\_builder\_editor to use the catalog item generation skill in Catalog Builder, or flow\_designer to use the flow generation skill.

Other roles might be required for ServiceNow Otto® experiences, such as the now\_assist\_panel\_user role for creating applications in ServiceNow Studio with the app generation skill.

ServiceNow Otto for Creator has its own role, now.assist.creator, which might be required for using some ServiceNow Otto for Creator capabilities. See [ServiceNow Otto for Creator \[now.assist.creator\] role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/creator-roles-1.md) for more information.

To learn what roles are required for the ServiceNow Otto for Creator AI capability you want to use, see the product documentation for the capability.

