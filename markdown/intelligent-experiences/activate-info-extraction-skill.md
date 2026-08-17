---
title: Activate the Extract Information from documents skill
description: Activate the Information Extraction skill, so AI agents can analyze and extract information from documents using generative AI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/activate-info-extraction-skill.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Information Extraction skill, Configure, Content Understanding, Enable AI experiences]
---

# Activate the Extract Information from documents skill

Activate the Information Extraction skill, so AI agents can analyze and extract information from documents using generative AI.

## Before you begin

Before activating the Information Extraction skill \(also known as Extract Information from documents skill\), make sure the Content Understanding application is installed.

Role required: DocIntel Admin \[sn\_docintel.admin\] or DocIntel Manager \[sn\_docintel.manager\]

## About this task

Content Understanding skills are enabled by default and are automatically available to users with the appropriate application roles. This default behavior functions as follows:

-   New users: When you install a ServiceNow Otto \(plugin\) product, it automatically enables the designated skills.
-   Existing users \(starting with Australia Patch 1\): There is no change to skills that are currently enabled or customized. A skill is turned on if the ServiceNow Otto plugin is installed, but the skill was never turned on, and an admin has never adjusted its roles. A skill is not turned on if it was previously turned on and then turned off, or if an admin has adjusted its roles.

If a skill was previously turned on and then turned off, or if an administrator adjusted its roles, perform this task to reactivate it.

**Note:** This task doesn't apply to the multimodal chat skill. The multimodal chat skill enables chat responses about the content of uploaded documents and images. It is used only on the server side by the Content insights AI agent and by the question answering capability in ServiceNow® Otto for Virtual Agent, and it doesn't require configuration in the AI Admin Hub.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills**.

2.  In the workflow list, select **Platform** &gt; **Other**.

3.  Search for the Extract information from documents skill.

4.  Select **Activate skill**.


## What to do next

[Set up a use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/set-up-use-case.md)

