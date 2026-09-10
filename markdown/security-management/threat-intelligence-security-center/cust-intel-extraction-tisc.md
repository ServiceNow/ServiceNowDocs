---
title: Customize the threat intelligence extraction use cases
description: Edit the prompts in the threat intelligence extraction use cases to change how AI extracts threat entities from the documents that your analysts upload.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/cust-intel-extraction-tisc.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-08-14"
reading_time_minutes: 1
keywords: [Now Assist TISC, AI extraction, Threat Intelligence Security Center]
breadcrumb: [Administer, Threat Intelligence Security Center, Security Operations]
---

# Customize the threat intelligence extraction use cases

Edit the prompts in the threat intelligence extraction use cases to change how AI extracts threat entities from the documents that your analysts upload.

## Before you begin

**Important:** Some generative AI skills, AI agents, and agentic workflows are turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

Role required: admin

## About this task

ServiceNow Otto for Threat Intelligence Security Center \(TISC\) provides the threat intelligence extraction use cases for the platform document extraction skill. Each use case corresponds to an extraction type that analysts select in Import Intelligence. The use cases carry the prompt that instructs the model which entities to extract, in which output format, and with which fields.

## Procedure

1.  Navigate to **Admin** &gt; **AI Admin Hub** &gt; **AI Skills**.

2.  Select **Platform** &gt; **Other**.

3.  Select **Extract information from documents**.

    Use the search bar to search for the skill.

4.  In the use cases, locate the threat intelligence extraction use case to customize.

    The following use cases are shipped with ServiceNow Otto for Threat Intelligence Security Center \(TISC\):

    |Use case|Extraction type in Import Intelligence|
    |--------|--------------------------------------|
    |Threat Intel Extraction - Simple|**Extract entities only**: Returns the type and the value of each extracted entity.|
    |Threat Intel Extraction with attributes|**Extract entities with rationale**: Returns the type and the value of each extracted entity, and adds the Analysis Score and Analysis Reasoning values.|

    **Important:**

    Import Intelligence uses only these two use cases. Document extraction use cases that you create aren't available to the AI extraction flow in Import Intelligence.

5.  Open the use case and edit the prompt.

    The prompt holds the instructions sent to the model, including which entities to extract, the output format, and the fields to return.

    **Note:**

    Changes to the prompt affect every import that runs the use case. Test the prompt against a representative document before you make it available to your analysts.

6.  Select **Save**.


**Related topics**  


[Customize the ServiceNow Otto for Threat Intelligence Security Center \(TISC\) skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/cust-now-assist-tisc-skill.md)

