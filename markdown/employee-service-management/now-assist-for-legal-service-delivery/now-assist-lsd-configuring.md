---
title: Configure Now Assist for Legal Service Delivery \(LSD\)
description: If you have the admin role, you can configure the Now Assist for Legal Service Delivery \(LSD\) application so that legal users or request fulfillers can use the generative AI skills from Legal Counsel Center and Core UI.
locale: en-US
release: yokohama
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Now Assist, generative AI]
breadcrumb: [Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Employee Service Management]
---

# Configure Now Assist for Legal Service Delivery \(LSD\)

If you have the admin role, you can configure the Now Assist for Legal Service Delivery \(LSD\) application so that legal users or request fulfillers can use the generative AI skills from Legal Counsel Center and Core UI.

Ensure you have installed Legal Counsel Center \(sn\_lg\_cf\_workspace\) - Version 1.5.1 or a later version.

**Important:** These Now Assist skills are now turned on by default. The skills will be automatically available to appropriate role users for the application. This change simply activates the skills and does not touch the roles that are needed to use them. The new default behavior works as follows:

-   **New customers**

    When you install a Now Assist product, designated skills are turned on automatically.

-   **Existing customers who are upgrading \(starting with Zurich Patch 4\)**

    Any previously unconfigured skill is turned on automatically \(the skill was never turned on, then off again\).

    There is no change to Now Assist skills that are currently enabled and customized.

    Previously configured skills that were turned on, then off, remain inactive.


The legal request summarization and legal matter summarization skills are available in the base system with the required configurations. To create a customized skill, you must create a copy of the skill that is in the base system before you modify the configuration. The parent skill is automatically deactivated when you activate your new customized skill. For more information, see [Customize a summarization skill in Now Assist for Legal Service Delivery \(LSD\)](../task/now-assist-lsd-customize-skill.md).

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

The following table lists the features and skills that you can access from the Now Assist Admin console.

<table id="table_ipf_bbd_wyb"><thead><tr><th>

LSD features

</th><th>

Skills

</th></tr></thead><tbody><tr><td>

Legal Request and Matter

</td><td>

-   Legal request summarization
-   Legal matter summarization

</td></tr></tbody>
</table>The data access permissions for the Now Assist for Legal Service Delivery \(LSD\) skills are available in the base system. To grant data access to additional roles, you must configure the data access permissions manually for those roles.

For more information, see [role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

-   **[Skill inputs for Now Assist for Legal Service Delivery \(LSD\)](now-assist-lsd-skill-inputs.md)**  
Get a quick overview of the skill inputs for Now Assist for Legal Service Delivery \(LSD\) so that you can configure how and when a skill is used.
-   **[Customize a summarization skill in Now Assist for Legal Service Delivery \(LSD\)](../task/now-assist-lsd-customize-skill.md)**  
If you have the admin role, you can customize a Now Assist for Legal Service Delivery \(LSD\) skill so that you can use the generative AI skills in Legal Counsel Center and in Core UI.
-   **[Configuring Q&amp;A Genius Results in Now Assist for Legal Service Delivery \(LSD\)](../task/now-assist-lsd-cofig-gen-results.md)**  
By using Q&amp;A Genius Results in the Now Assist for Legal Service Delivery \(LSD\) application, you can quickly find the most optimal information in Employee Center, Legal Counsel Center, and global search.

**Parent Topic:**[Now Assist for Legal Service Delivery \(LSD\)](now-assist-lsd-landing.md)

