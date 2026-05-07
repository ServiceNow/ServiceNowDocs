---
title: Automated quality assurance
description: Configure the Automated quality assurance skill to generate quality assurance scores and feedback for closed cases through automatic review based on defined scoring criteria.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-02-02"
reading_time_minutes: 4
keywords: [Generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Activate Now Assist Skills, Configure, Now Assist for CSM, Customer Service Management]
---

# Automated quality assurance

Configure the Automated quality assurance skill to generate quality assurance scores and feedback for closed cases through automatic review based on defined scoring criteria.

## Before you begin

Role required: admin

## About this task

Add, configure, review, and activate the Automated quality assurance skill, including parameters, display options, and availability checks.

**Note:** In the base system, administrators can modify the display settings, role assignments, and add the custom parameters in the skill. All other fields are read-only. To customize additional settings, administrators must clone the skill first.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  Select the **Customer** workflow, and **CSM** as the product.

3.  Activate skill for the **Automated quality assurance** skill.

    Each skill has a guided setup with multiple steps. A check symbol next to each step indicates whether its setup is complete, partially complete, or incomplete. After configuring a step, select **Save and continue** to move forward, or **Back** to return to a previous step.

4.  Select **General details** and review the skill name and description.

    **Note:** You can't modify the input data source in the base system.

5.  Select **Choose inputs** and review the input tables and fields to create prompts that determine where data is pulled from.

6.  Select **Define scoring parameters** to review the parameters and categories used to calculate the quality assurance score.

    **Note:** In the base system, you can only edit weights and disable parameters. An admin can add custom parameters to a skill directly, without cloning it.

    -   Viewing Parameter Details

        1.  Select any parameter to view its detailed scoring rubric. The rubric explains the evaluation criteria and scoring methodology for the parameter.
        2.  Review the rubric to understand how interactions are scored for this parameter. The total weight across all the categories and parameters should add up to 100%. For example, If there are 9 categories and 21 parameters, having just one parameter turned on with 100% weightage meets the requirement.
        |Category|Parameter|What it measures|
        |--------|---------|----------------|
        |Issue Understanding &amp; Diagnosis|Root cause analysis|Agent identifies and explains the underlying cause — not just surface symptoms. Good agents explain why the problem occurred; weak agents restate what the customer said.|
        |Resolution completeness &amp; actionability|Every part of the customer's question is addressed without gaps. Clear, step-by-step instructions the customer can follow immediately, matched to their technical level.|
        |Communication Quality &amp; Writing|Grammar &amp; mechanics|No spelling errors, typos, grammatical mistakes, or punctuation problems. Measures basic writing correctness — not tone or style.|
        |Clarity &amp; conciseness|Clear, direct language without jargon or redundancy. Good agents explain technical terms; weak agents ramble or write ambiguously.|
        |Tone &amp; professionalism|Helpful, respectful tone even with frustrated customers. Good agents acknowledge concerns; weak agents blame the customer or use overly casual language.|
        |Formatting &amp; readability|Response structured for easy scanning using numbered lists, bullets, and short paragraphs rather than walls of text.|
        |Customer Empathy|Issue acknowledgment|Agent explicitly acknowledges the customer's concern or frustration early in the response before jumping to a solution.|
        |Personalization|Response uses the customer's name and references specific case or account details rather than a generic reply.|
        |Active listening signals|Agent paraphrases or references specific details from the customer's message, showing they absorbed what was said.|
        |Knowledge Base Utilization|KB article sharing|Agent proactively shares relevant knowledge base articles or help docs with contextual explanations — not just generic links.|
        |Self-service enablement|Resources provided help the customer handle similar issues independently in the future.|
        |Proactive guidance|Agent anticipates related future issues and provides preventive information or best practices beyond what was explicitly asked.|
        |First-Contact Resolution Intent|Complete resolution|Issue fully resolved in the first interaction without requiring follow-up. Good agents exhaust options within their scope before escalating.|
        |Information gathering efficiency|All necessary diagnostic info gathered upfront rather than asking piecemeal across multiple exchanges.|
        |Appropriate escalation|When escalation is needed, agent clearly explains why and sets realistic expectations for next steps and timeline.|
        |Closing &amp; Next Steps|Resolution confirmation|Agent confirms what was resolved and what happens next, rather than ending ambiguously.|
        |Timeline &amp; expectations|Specific timelines provided for open or pending issues — not vague terms like "soon" or "as soon as possible."|
        |Professional sign-off|Polite, professional closing with a genuine offer to help with additional questions.|

    -   Enabling or Disabling Parameters

        1.  Locate the  **Active**  toggle or check box for the parameter you want to enable or disable.
        2.  Toggle the parameter status: Enable the toggle to activate the parameter in quality scoring and disable the toggle to exclude the parameter from quality scoring. When you disable a parameter, the system prompts you to redistribute its weight among remaining active parameters. Adjust the weights of other parameters to verify that the total equals 100%. Weight redistribution is required because all active parameter weights must sum to 100% for accurate scoring.
    -   Adjusting Parameter Weights

        1.  Select the weight field for any active parameter to edit it.
        2.  Enter the new weight value as a percentage.
        3.  Adjust weights for other parameters as needed to verify that the total equals 100%.

            **Note:** The system validates that active parameter weights sum to exactly 100% before permitting you to save changes.

7.  Select **Define Availability** to review when the skill capability is active and accessible.

8.  Select **Display** to activate the skill and make it visible in the In-product desktop for specific roles.

    **Note:** The skill appears on forms and workspaces. By default, the skill is available to customer service managers and customer service agents’ roles. Admins can deactivate the skill to hide it from managers and agents during testing the configuration accuracy.

9.  Assign roles that should have access to quality dashboards.

10. Select **Review and Activate** to check the default setup.

11. Select **Activate skill** to turn on the skill for agents and complete the configuration.

    Skill is activated for agents, and a success modal shows up with the option **Return to Now Assist skills.**


