---
title: Configuring Now Assist for Sourcing and Procurement Operations \(SPO\)
description: If you have the admin role, you can configure the Now Assist for Sourcing and Procurement Operations \(SPO\) application so that your requesters, procurement specialists, and sourcing managers can use the generative AI skills in Source-to-Pay Workspace Workspace and Core UI.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
keywords: [configuring generative AI for financial services operations, configuring generative AI for FSO]
breadcrumb: [Now Assist for Sourcing and Procurement Operations \(SPO\), Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configuring Now Assist for Sourcing and Procurement Operations \(SPO\)

If you have the admin role, you can configure the Now Assist for Sourcing and Procurement Operations \(SPO\) application so that your requesters, procurement specialists, and sourcing managers can use the generative AI skills in Source-to-Pay Workspace Workspace and Core UI.

## Before you begin

Role required: admin

## About this task

Use the Now Assist Admin console to configure Now Assist for SPO. This console contains everything that you need to install the plugins and configure the generative AI skills. For additional information, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

The following table lists the features and skills that you can access from the Now Assist Admin console.

<table id="table_akf_42k_mbc"><thead><tr><th>

Now Assist for SPO features

</th><th>

Skills

</th></tr></thead><tbody><tr><td>

Summarization for fulfillers

</td><td>

-   Sourcing request summarization
-   Purchase requisition summarization
-   Procurement case summarization

</td></tr><tr><td>

Conversational intake

</td><td>

-   Now Assist Genius Results
-   Now Assist Multi-turn Catalog Ordering
-   Now Assist Topics

</td></tr></tbody>
</table>![Now Assist skills for SPO section, showing the Summarization for fulfillers and Conversational intake feature cards.](../image/now-assist-for-spo.png "Now Assist skills for SPO")

## Procedure

1.  Install the Now Assist for Sourcing and Procurement Operations \(SPO\) plugin \(sn\_spend\_gen\_ai\).

    -   For information about the plugin dependencies and plugin activation order, see [Supporting information for Now Assist for Sourcing and Procurement Operations \(SPO\)](../concept/now-assist-spo-supporting-info.md).
    -   For information about the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features** to access the **Now Assist Features** tab of the Now Assist Admin console.

3.  Expand the **Finance and Supply Chain** workflow group and select **SPO**.

    The SPO features are grouped under the Finance and Supply Chain workflow group. Each feature has its associated skills.

4.  Activate and configure the skills for Now Assist for Sourcing and Procurement Operations \(SPO\).

<table id="table_bcq_z34_tcc"><thead><tr><th>

Skills

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Conversational intake

</td><td>

On the Conversation intake skill card, verify that your AI conversational intake skills are active for SPO.

**Note:** The Platform AI conversational experience skills are active by default.

 For more information, see [Configuring Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

</td></tr><tr><td>

Summarization for fulfillers

</td><td>

1.  On the Summarization for fulfillers skill card, select **View details**.
2.  In the All available Summarization for fulfillers skills section, select **Activate skill** for any the following skills that you would like to activate:
    -   Sourcing request summarization
    -   Purchase requisition summarization
    -   Procurement case summarization


</td></tr></tbody>
</table>5.  Select **General Details** and review the details about the skill and select **Save and continue** to go to the next step in the Guided Setup.

6.  Follow the steps to configure and activate a skill using the Guided Setup.

7.  Select **Choose input** and review the base input table and input fields, and then select **Save and continue** to go to the next step in the Guided Setup.

8.  Select **Customize and test prompt** to test the prompt on a record.

9.  Select **Save and continue** to go to the next step in the Guided Setup.

10. Select **Define Availability** and choose one of the following options.

<table id="choicetable_e25_bvj_1cc"><thead><tr><th align="left" id="d140653e427">

Option

</th><th align="left" id="d140653e430">

Description

</th></tr></thead><tbody><tr><td id="d140653e436">

**Skill is always available**

</td><td>

Skill is always available to users.

</td></tr><tr><td id="d140653e445">

**Customize skill availability**

</td><td>

The skill is available only when the certain conditions are met \(Default\).Use the condition builder to set your conditions.

</td></tr></tbody>
</table>11. Select **Save and continue** to go to the next step in the Guided Setup.

12. Choose **Select display** to determine where you'd like to display the skill.

<table id="choicetable_x1c_5b2_1cc"><thead><tr><th align="left" id="d140653e481">

Option

</th><th align="left" id="d140653e484">

Description

</th></tr></thead><tbody><tr><td id="d140653e490">

**In-product**

</td><td>

Now Assist skills are displayed on forms and workspaces.

</td></tr><tr><td id="d140653e501">

**Now Assist panel**

</td><td>

Now Assist skills are available in the Now Assist panel. **Note:** If you don't see this option, you must activate the Now Assist panel. For more information, see [Turn on the Now Assist panel](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

</td></tr></tbody>
</table>13. Select **Save and continue** to go to the next step.

14. Review your choices and select **Activate** to complete the configuration for the skill.

15. Select **Return to Summarization for fulfillers**.

    The skill is displayed in the Active skills section.


