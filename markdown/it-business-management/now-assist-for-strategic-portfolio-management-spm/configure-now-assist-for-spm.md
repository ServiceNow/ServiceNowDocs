---
title: Configure Now Assist for Strategic Portfolio Management \(SPM\)
description: If you have the admin role, you can configure the Now Assist for Strategic Portfolio Management \(SPM\) application to enable generative AI skills in Strategic Planning, Project Workspace, or Enterprise Agile Planning.
locale: en-US
release: xanadu
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
keywords: [Now Assist for SPM configuration, Now Assist for SPM features and skills, Choose inputs, Activate and configure the skills, Project Gen AI Docs, Multi feedback summarization, Conversational experiences for demand creation]
breadcrumb: [Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Configure Now Assist for Strategic Portfolio Management \(SPM\)

If you have the admin role, you can configure the Now Assist for Strategic Portfolio Management \(SPM\) application to enable generative AI skills in Strategic Planning, Project Workspace, or Enterprise Agile Planning.

## Before you begin

To enable the Agile story generation skill for Enterprise Agile Planning, complete the following tasks:

-   [Turn on the Now Assist panel](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   Ensure AI Search is activated and ready to use by navigating to **All** &gt; **AI Search** &gt; **AI Search Status**

Role required: admin

## About this task

Use the Now Assist Admin console to configure Now Assist for SPM. This console contains everything that you need to activate the plugins and configure the generative AI skills. For additional information, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

The following table lists the features and skills that you can access from the Now Assist Admin console.

<table id="table_u5z_gfb_fbc"><thead><tr><th>

SPM feature

</th><th>

Skill

</th></tr></thead><tbody><tr><td>

Feedback

</td><td>

-   Feedback summarization
-   Multi feedback summarization

</td></tr><tr><td>

Demand

</td><td>

Conversational experiences for demand creation

</td></tr><tr><td>

Docs

</td><td>

-   Project doc summarization \(Project Workspace\)
-   Planning item doc summarization \(Strategic Planning\)
-   EAP doc summarization \(Enterprise Agile Planning\)

</td></tr><tr><td>

Project

</td><td>

Email project summary

</td></tr><tr><td>

Stories

</td><td>

Agile story generationThe Agile story generation skill is supported starting with the Yokohama patch 3 release and Strategic Planning v4.7.0. If you are on earlier versions of the Yokohama release, you can activate the Story generation skill, which inlcudes generating stories from Epics only.

</td></tr><tr><td>

Product idea, Demand, Epic, Project, Capability, Feature, or Story

</td><td>

Write Planning item

</td></tr></tbody>
</table>**Note:** Now LLM Service is the default provider for this Now Assist application's skills.

The Now Assist for SPM application and conversational experiences for demand creation system requirements are as follows:

-   Now Assist for Platform
-   Strategic Planning
-   Project Workspace
-   SPM Pro Plus license

## Procedure

1.  Install the Now Assist for Strategic Portfolio Management \(SPM\) plugin \(sn\_spm\_gen\_ai\).

    -   For information about the application dependencies, see [Supporting information for Now Assist for Strategic Portfolio Management \(SPM\)](../concept/supporting-info-now-assist-spm.md).
    -   For information about the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
2.  Navigate to **All** &gt; **Now Assist Skills**

    If you’re already in the Now Assist Admin console, you can select the **Now Assist Skills** tab on the screen.

3.  Select the **Technology** category and then select SPM.

4.  From the Now assist skill card, select **Activate skill** to activate the required skill.

    ![Now Assist skills for Technology.](../images/now-assist-admin-page.png)

5.  Review the inputs and display parameters for the selected skill.

    1.  **Choose inputs**:
        -   Review the data source, such as the tables and fields. The inputs for most skills are selected by default and can't be modified. For information about the inputs for each skill, see [Skill inputs for Now Assist for Strategic Portfolio Management \(SPM\)](../reference/skill-inputs-for-now-assist-for-spm.md).

            ![Choose inputs for the multi feedback summarization skill in the Choose Input data screen.](../images/inputs-feedback.png "Choose the Inputs screen for the skill")

        -   Select **Save and continue**.
    2.  **Select display**: Review where the skill appears.
        -   **In-product desktop**: Enabling this option shows the skill within the Strategic Planning workspace.
        -   **Now Assist panel**: Enabling this option shows the skill within the Now Assist panel when launched from the Strategic Planning workspace.

            **Note:** The display options are available based on the skill.

        -   Select **Save and continue**.
    3.  **Review and activate**: Review the summary of your choices activate the skill by selecting **Activate**.
    For more information on the skill inputs, see [Skill inputs for Now Assist for Strategic Portfolio Management \(SPM\)](../reference/skill-inputs-for-now-assist-for-spm.md).

6.  Repeat the process to activate any other available skills for SPM.


## Result

The skill is configured and activated.

**Related topics**  


[Using Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-now-assist-for-spm.md)

[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

[Configuring Now Assist settings and features](https://www.servicenow.com/docs/access?context=configuring-na-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

