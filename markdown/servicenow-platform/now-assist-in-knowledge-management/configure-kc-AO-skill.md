---
title: Configuring Article Optimization skill and prompts
description: Create custom prompts for the default Article Optimization \(AO\) skill in the Knowledge Center application and prompts using standalone custom skills.
locale: en-US
release: yokohama
product: Now Assist in Knowledge Management
classification: now-assist-in-knowledge-management
topic_type: task
last_updated: "2025-12-04"
reading_time_minutes: 2
breadcrumb: [Configure Now Assist in Knowledge Management, Now Assist in Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configuring Article Optimization skill and prompts

Create custom prompts for the default Article Optimization \(AO\) skill in the Knowledge Center application and prompts using standalone custom skills.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select **Create Skill** and complete the configuration form.

3.  Select **Next**.

    1.  Set **Role restriction** field to **Nobody**.

    2.  Select **Choose from library** to import an existing prompt for reference, otherwise, select**Write from scratch**.

        **Note:** Using existing custom skills to modify prompts may result in unreliable article optimization scans. The easier option is to choose an existing prompt, then clone and modify to suit your specifications.

    3.  Enter at least one value in the **Skill input** field.

        **Note:** The default value for **Datatype** is **Record** and that of **Table** is **Knowledge** **\(kb\_knowledge\)**.

4.  Select **Go to summary** and then **Finish**.

5.  Modify the existing prompt or select the **Plus** icon at the top of the prompt list to create a new prompt from scratch.

6.  Navigate to the **Deployment settings** page for the skill.

7.  Select **Publish** after ensuring that all the prompts and skill settings meet your specifications.

8.  Navigate to the **sys\_generative\_ai\_config** table and filter your prompt\(s\).

    1.  Add the location where the skill should be located on the **Now Assist Admin** page \(AO is located under **Platform Knowledge**.

    2.  Enter the **Feature name**, which should be the name of this skill.

9.  Open the record\(s\), scroll down to the **Generative AI Prompt Configs** related list and select **New**.

10. Add the following filter properties:

    -   Name: **optimization\_prompt**
    -   Value: prompt name from the **Output format** section of prompt.

## Result

Article optimization skill is now configured.

## What to do next

After successfully configuring the skill, proceed to activate the article optimization skill. For more information, see [Activate Article Optimization skill](activate-kc-AO-skill.md).

-   **[Activate Article Optimization skill](activate-kc-AO-skill.md)**  
Activate the Knowledge Center Article Optimization skill to enable use of article optimization features for generating knowledge articles in the Knowledge Center.

**Parent Topic:**[Configuring Now Assist in Knowledge Management](../../knowledge-management/concept/configuring-now-assist-km.md)

**Related topics**  


[Configure custom AI-based Article Optimization scans](configure-custom-ai-based-AO-scans.md)

