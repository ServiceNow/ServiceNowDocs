---
title: Customizing a Now Assist for CSM skill
description: Learn how to access, activate, and customize a Now Assist for CSM skill using the Now Assist Admin console and Now Assist Skill Kit.
locale: en-US
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2025-11-18"
reading_time_minutes: 3
keywords: [Generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Configure, Now Assist for CSM, Customer Service Management]
---

# Customizing a Now Assist for CSM skill

Learn how to access, activate, and customize a Now Assist for CSM skill using the Now Assist Admin console and Now Assist Skill Kit.

Role required: admin

Now Assist for CSM provides base system skills that can be tailored to meet specific business requirements. Customization ensures that skills align with your organization's workflows, data sources, and user roles. There are two main ways to customize:

-   Using Now Assist Admin console: Modify base system skills, input configurations, and display settings.
-   Using Now Assist Skill Kit: Build and publish custom skills for advanced use cases by customizing inputs and prompts, and then publish it. You can also use the Now Assist Skill Kit to clone base system skills, as long as they are the latest versions created after the release of the Now Assist Skill Kit.

![Flowchart showing process steps in Now Assist Admin console and Now Assist Skill Kit](../image/cloning-in-now-assist-for-csm.png)

## Access and activate a skill in Now Assist Admin console

1.  Navigate to **All** &gt; **Now Assist Admin console** &gt; **Skills**.
2.  Select the Now Assist Skills tab.
3.  Select **Customer** &gt; **CSM**
4.  Choose the skill you want to configure.
5.  Select **Activate Skill**.
6.  Go through the guided set up steps and activate the skill.
7.  To customize the base system skills:
    1.  Make a copy of the skill as you cannot directly modify the base system skill.
    2.  Edit the copied skill's name so it is more descriptive for the LLM.
    3.  Adjust input configurations by adding fields or creating a new data source.
    4.  Test the skill with a sample record.

        **Tip:**

        -   ISelect **Edit prompt in Now Assist Skill Kit** to edit the prompt in Now Assist Skill Kit.
        -   You need the sn\_skill\_builder.admin role to edit the prompt in the Now Assist Skill Kit \(NASK\).
        -   To edit a prompt, locate the prompt for the specified provider, clone it, apply the necessary changes, add pre or post processors and conditions as needed, finalize and publish the updated prompt, and then return to test changes on Now Assist Admin console.
    5.  Customize how and when the skill capability will exist and be available.
    6.  Choose how the skill will be triggered.
    7.  Define who has access to this skill. Roles selected here will be available in the **Select display** step.
    8.  Select where to display the skill- **In-product**, or in Now Assist panel.
    9.  Under each display type, open the chevron and specify user roles by entering role names in the User roles field.
    10. Review your choices and select **Activate** to complete the skill customization.

        **Note:** For more information, see [Customize a case summarization skill in Now Assist for Customer Service Management \(CSM\)](customize-a-now-assist-for-csm-skill.md).


## Access and clone base system skills with the Now Assist Skill Kit

1.  Navigate to **All** &gt; **Now Assist Skill KIt**.
2.  Under the **ServiceNow skills** tab, select the prompt you want to edit in [Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=using-now-assist-skill-kit&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

    **Note:** You need the sn\_skill\_builder.admin role to activate and customize the prompt in the Now Assist Skill Kit \(NASK\).

3.  Create a [clone](https://www.servicenow.com/docs/access?context=clone-and-edit-servicenow-skill&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for the selected skill by selecting the overflow icon ![More options](../image/OverflowIcon.png)
4.  Enter a name, description and provider to clone the skill.
5.  In the **Skill contents** pane, select the**Inputs** edit icon and add any inputs that you like to add to the prompt.
6.  In the **Prompt** screen, select the edit icon and add the desired inputs to the prompt or [Create](https://www.servicenow.com/docs/access?context=create-prompt-template&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) a new prompt.
7.  [Test](https://www.servicenow.com/docs/access?context=test-prompt-template&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) the prompt.
8.  [Evaluate](https://www.servicenow.com/docs/access?context=evaluate-prompt&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) the prompt.
9.  [Finalize and publish](https://www.servicenow.com/docs/access?context=publish-skill&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) the skill from the Now Assist Skill Kit.

    **Warning:** Once finalized, you won't be able to edit this version of the prompt. You can always update and create a new version, or clone and create a new prompt.

10. Test the changes on associated records.
11. [Activate](https://www.servicenow.com/docs/access?context=activate-skill&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) it in the Now Assist Admin console and set display options.

    **Note:** This is not required for all skills.


