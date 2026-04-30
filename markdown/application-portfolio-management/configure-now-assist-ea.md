---
title: Configure Now Assist for Enterprise Architecture \(EA\)
description: If you have the admin role, you can configure the Now Assist for Enterprise Architecture \(EA\) to enable generative AI skills in Enterprise Architecture Workspace \(EA\).
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Now Assist for Enterprise Architecture \(EA\), Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Configure Now Assist for Enterprise Architecture \(EA\)

If you have the admin role, you can configure the Now Assist for Enterprise Architecture \(EA\) to enable generative AI skills in Enterprise Architecture Workspace \(EA\).

## Before you begin

Role required: admin

## About this task

Use the Now Assist Admin console to configure Now Assist for EA. This console contains everything that you need to activate the plugins and configure the generative AI skills. For additional information, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

The following table lists the features and skills that you can access from the Now Assist Admin console.

|EA feature|Skill|
|----------|-----|
|Architectural decision record|Architectural decision record doc summarization and actions \(Enterprise Architecture Workspace\)|

**Note:** Now LLM Service is the default provider for this Now Assist application's skills.

The Now Assist for Enterprise Architecture \(EA\) system requirements are as follows:

-   Now Assist for Platform \(v7.0.1\)
-   Enterprise Architecture Workspace \(v3.4.0\)

## Procedure

1.  Install the Now Assist for Enterprise Architecture \(EA\) plugin \(sn\_ea\_gen\_ai\).

    -   For information about the application dependencies, see [Supporting information for Now Assist for Enterprise Architecture \(EA\)](../concept/supporting-info-now-assist-ea.md).
    -   For information about the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

    If you’re already in the Now Assist Admin console, you can select the **Now Assist Skills** tab on the screen.

3.  Select the expand row icon \(![Expand Row icon](../../application-portfolio-management/image/ExpandIcon.png)\) next to **Technology**.

4.  Select **EA**.

5.  Activate and configure the skill for Now Assist for Enterprise Architecture \(EA\).

<table id="choicetable_wnn_hyf_b2c"><thead><tr><th align="left" id="d29759e255">

Skill

</th><th align="left" id="d29759e258">

Action

</th></tr></thead><tbody><tr><td id="d29759e264">

**ADR Doc Summarization and Actions**

</td><td>

1.  Select **Activate skill**.
2.  Go to step 6 and review the details.


</td></tr></tbody>
</table>6.  Review the following parameters for the selected skill.

    1.  Review the roles than can access the skill. If necessary, select the edit icon ![](../image/edit-icon.png) if you want to add access to more roles.

        You must verify that your application scope is set to Now Assist for Enterprise Architecture \(EA\). For information on how to change the application scope, see [Select an application from the application picker](https://www.servicenow.com/docs/access?context=t_SelectAnAppFromTheAppPicker&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

        **Note:** For the ADR Doc Summarization and Actions skill, the sn\_apm.apm\_user and sn\_apm.apm\_read roles are selected, by default.

        To learn more about security in Now Assist AI agents with access control lists \(ACLs\), see [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

    2.  **Select display**: Review where the skill appears.

        **Note:** When the **In-product desktop** option is selected, the skill is displayed in all EA products.

    3.  Select **Save and continue**.

    4.  **Review and activate**: Review the summary of your choices.
7.  Complete the configuration and activate the skill by selecting **Activate**.

    The skill is configured and activated.


