---
title: Configure Article Optimization skill and prompts
description: Create custom prompts for the default Article Optimization \(AO\) skill in the Knowledge Center application and prompts using standalone custom skills.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-in-knowledge-management/configure-kc-AO-skill.html
release: zurich
product: Now Assist in Knowledge Management
classification: now-assist-in-knowledge-management
topic_type: task
last_updated: "2026-07-20"
reading_time_minutes: 1
breadcrumb: [Configure ServiceNow Otto in Knowledge Management, ServiceNow Otto in Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure Article Optimization skill and prompts

Create custom prompts for the default Article Optimization \(AO\) skill in the Knowledge Center application and prompts using standalone custom skills.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **AI Skill Kit** &gt; **Home**.

2.  Select **Create Skill** and complete the configuration form.

3.  Select **Next**.

    1.  Set the **Role restriction** field to **Nobody**.

    2.  Select **Choose from library** to import an existing prompt for reference; otherwise, select **Write from scratch**.

        **Note:** Using existing custom skills to modify prompts may result in unreliable article optimization scans. Choose an existing prompt, then copy and modify it to suit your specifications.

    3.  Enter at least one value in the **Skill input** field.

        **Note:** The default value for **Datatype** is **Record** and that of **Table** is **Knowledge** **\(kb\_knowledge\)**.

4.  Select **Go to summary** and then **Finish**.

5.  Modify the existing prompt or select the **Plus** icon at the top of the prompt list to create a prompt from scratch.

6.  Navigate to the **Deployment settings** page for the skill.

7.  Select **Publish** after confirming that all prompts and skill settings meet your specifications.

8.  Navigate to the **sys\_generative\_ai\_config** table and filter your prompts.

    1.  Add the location where the skill should appear on the **AI Admin** page \(AO is located under **Platform Knowledge**\).

    2.  Enter the **Feature name**, which should be the name of this skill.

9.  Open the records, scroll down to the **Generative AI Prompt Configs** related list, and select **New**.

10. Add the following filter properties:

    -   Name: **optimization\_prompt**
    -   Value: prompt name from the **Output format** section of the prompt.

## Result

The article optimization skill is configured.

## What to do next

After configuring the skill, activate the article optimization skill. For more information, see [Activate the Article Optimization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-in-knowledge-management/activate-kc-AO-skill.md).

-   **[Activate the Article Optimization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-in-knowledge-management/activate-kc-AO-skill.md)**  
Activate the Knowledge Center Article Optimization skill to enable article optimization features for generating knowledge articles in the Knowledge Center.

**Parent Topic:**[Configuring ServiceNow Otto in Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-in-knowledge-management/configuring-now-assist-km.md)

**Related topics**  


[Configure custom AI-based Article Optimization scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-in-knowledge-management/configure-custom-ai-based-AO-scans.md)

