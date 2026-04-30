---
title: Configure the Troubleshooting steps identification AI agent to use the Search retrieval tool
description: Configure the Troubleshooting steps identification AI agent to use the Search retrieval tool to fetch relevant cases and knowledge articles, including their attachments, to help solve your issue.
locale: en-US
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [AI Agents, Agentic AI]
breadcrumb: [Set up the Troubleshooting steps identification AI agent, Configure, Now Assist for CSM, Customer Service Management]
---

# Configure the Troubleshooting steps identification AI agent to use the Search retrieval tool

Configure the Troubleshooting steps identification AI agent to use the Search retrieval tool to fetch relevant cases and knowledge articles, including their attachments, to help solve your issue.

## Before you begin

Role required: admin

## About this task

The Search retrieval tool is configured to use the \[CSM AIS\] Configurable Workspace Search Config AI search profile. By default, this profile is linked to the Case and Knowledge search sources, which are defined in the \[CSM AIS\] Case and Knowledge Table indexed sources. For more information, see [Indexed sources in AI Search](https://www.servicenow.com/docs/access?context=indexed-sources-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Indexed Sources** &gt; **New**.

2.  On the form, fill in the **Name**, **Source**, and **Retention Policy** fields and select **Submit**.

    For a description of the field values, see [Indexed Source form](https://www.servicenow.com/docs/access?context=indexed-source-form-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

3.  In the Semantic Index Configuration related list, select **New** and fill in the details as needed.

    For a description of the field values, see [Semantic Index Configuration form](https://www.servicenow.com/docs/access?context=semantic-index-configuration-form&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

4.  In the Semantic Index Fields related list, select **New** and add the fields of the table that you want included in your search.

    For a description of the field values, see [Semantic Index Field form](https://www.servicenow.com/docs/access?context=semantic-index-field-form&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

5.  Navigate to **All** &gt; **AI Search Sources** &gt; **New**.

6.  On the form, fill in the **Name**, **Indexed Source**, and **Conditions** fields.

    For a description of the field values, see [Search Source form](https://www.servicenow.com/docs/access?context=search-source-form-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

7.  Navigate to **All** &gt; **AI Search** &gt; **Search Profile** &gt; **\[CSM AIS\] Configurable Workspace Search Config**.

8.  In the Search Sources related list, select **Link Existing** and then link the previously created search source.

9.  Activate the \[CSM AIS\] Configurable Workspace Search Config AI search profile by selecting **Publish**.

10. Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview** &gt; **Explore All**.

11. On the **AI agents** tab, navigate to **Troubleshooting steps identification AI agent** &gt; **Add tools and information** &gt; **Search retrievals** and select **Get Similar cases and Relevant knowledge articles**.

12. In the Edit search retrieval window, add the previously created indexed source into **Search sources** and then specify what to search for in the **Fields returned** and **Semantic index fields**.

    For a description of the field values, see [Add a search retrieval to an AI agent](https://www.servicenow.com/docs/access?context=add-retriever-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

13. Select **Save**.


## Result

The Troubleshooting steps identification AI agent can now use the Search retrieval tool to fetch the relevant information from additional sources.

