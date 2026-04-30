---
title: Guidelines for creating prompts
description: The guidelines help to write prompts for Out-of-Box \(OOB\) and custom knowledge article templates. Follow these instructions to create ideal prompts that optimize the use of AI models for generating knowledge articles.
locale: en-US
release: zurich
product: Now Assist in Knowledge Management
classification: now-assist-in-knowledge-management
topic_type: reference
last_updated: "2025-07-25"
reading_time_minutes: 5
breadcrumb: [Configure skills with custom prompts for knowledge article templates, Configure Now Assist in Knowledge Management, Now Assist in Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Guidelines for creating prompts

The guidelines help to write prompts for Out-of-Box \(OOB\) and custom knowledge article templates. Follow these instructions to create ideal prompts that optimize the use of AI models for generating knowledge articles.

## Create prompts for a how-to article template for a case

An ideal prompt maps to the following three fields in the template form:

-   Introduction: Includes the problem statement of the case along with the severity level.
-   Instruction: Includes the resolution steps for the issue described in the incident.
-   Short description: Includes the title of the issue described in the incident

|Section|Template field|
|-------|--------------|
|Problem|Introduction|
|Severity|Introduction|
|Instructions|Steps to resolve|
|Title|Short description|

## Structure of the prompt

Use the following prompt draft structure to create a prompt:

-   Initial header instructions \(the purpose of the prompt\)
-   Input source data
-   Guidelines for generating the article
-   Output structure along with mapping details, according to your requirements

    **Important:** When mapping, it’s important that the mapping key matches with the article template’s field key. The value must contain the sections that you intend to add.


## Sample prompt for generating a single KB how-to template article

```

As a professional customer support agent, your goal is to create a clear and comprehensive article based on a customer's case with only the following sections: 
Problem, Severity, Steps to resolve and Title. 
Follow the structure below to ensure the article is easy for other customers to read and solve the problem independently.

Customer Case Input:
<CUSTOMER CASE START>
{{short_description}}
{{description}}
{{activities}}
{{close_notes}}
<CUSTOMER CASE END>

**Guidelines for Article Generation:**
Do not use actual people's names, emails, phone numbers, or machine names from the case in the article.
Do not use your outside knowledge to write the article. Kindly use content from the case only.
In providing the content for each of the sections, if you are not confident, then return N/A for the specific section.

**Content Guidelines for Each Section:**
**Problem:**
Describe the issue comprehensively, in sentence format and include:
Observations of visible indications of the issue.
Relevant error messages or log details directly related to understanding the issue.
Steps to reproduce the problem with each step being a numbered list describing only a single action.
Add a new line character at the end of each step to display individual steps in separate lines in the final output.
**Severity:**
Calculate the severity of the problem after reading description from the case details and determine how critical it is to the users.
**Steps to Resolve:**
List each step required to resolve the issue, and ensure that each step is written in sentence format.
Attempted troubleshooting steps are included.
Steps should be in a numbered list with each step describing a single action.
Add a new line character at the end of each step to display individual steps in separate lines in the final output.
Derive information from comments, work notes, or resolution notes of the case, after verifying all relevant steps.
If no resolution is provided in the case, enter "N/A".
**Title:**
Provide a concise and formal title that accurately describes the issue. Derive the title from the short description of the incident
Use this structure to create a helpful and user-friendly article for other customers facing similar problems while adhering to the guidelines provided.

**Output Format:**
Before completing, verify that each list item is in a new line, in all cases of a numbered list. *Always generate a valid JSON object.
Generate a JSON response in the following format: 
{ 
"kb_introduction": { 
  "Problem": "string", 
  "Severity": "string 
}, 
"kb_instructions": { 
  "Steps To Resolve": "string" 
}, 
“short_description”: { 
  “Title”: “string” 
} 
}

```

## Sample prompt for generating a multi-KB how-to template article

```
Act like a professional customer service agent and understand the content of the child articles provided below. 
These child articles are used by customers to resolve issues encountered for different problems. 
Each child article starts with <CHILD_ARTICLE_START> and ends with <CHILD_ARTICLE_END>.

**CHILD ARTICLES:**

{{intermediateKBGenerator.output}}
{{intermediate_article_1}}

Your job then is to combine these child articles and write one parent article that captures all the important information present in the child articles. 
The parent article should show other customers how to resolve the problems on their own. Only use information present in the child articles.

The parent article must contain the following sections in the same order:
**Problem:**
Summarize problems from all child articles
**Severity:**
determine severity from all child articles
**Steps to Resolve:**
It should contain the detailed list of steps that customers can take to resolve the problem on their own. It should include all the steps and their details from the Steps to Resolve section of the child articles. Make sure to include all the relevant notes, code, scripts, references, additional information, URLs and any other entities that are needed for resolving the issue. For each separate problem, provide a title of the problem in a new line but do not include any generic words like "Issue", "Problem" or "Steps to Resolve" and do not add markdown format while generating the title for steps to resolve section and then the list of steps to resolve that problem. Make each step a numbered list item (starting with 1., 2., etc.). Then add a new line character at the end of each list item and 2 new line characters at the end of the last list item of each problem such that they appear in a new line in the final output with proper titles. Make sure to use full sentences for each step.
**Title:**
It should only contain a short description of the problem in formal language and only be a few words. It should be generic enough to capture the topics of the issues present in all the child articles.
For each section, if you are not absolutely sure, generate "Not enough information available for this section.".

Do not underline the section headers and titles. 
Do not apply bold styling to section headers and titles. 
Do not add special characters "*", "-" or "#" to the section headers and titles.

Generate a JSON response in the following format:
{ 
"kb_introduction": { 
  "Problem": "string", 
  "Severity": "string 
}, 
"kb_instructions": { 
  "Steps To Resolve": "string" 
}, 
“short_description”: { 
  “Title”: “string” 
} 
}

```

**Parent Topic:**[Configure skills with custom prompts for knowledge article templates](../task/Now-assist-configure-custom-prompts-for-templates.md)

