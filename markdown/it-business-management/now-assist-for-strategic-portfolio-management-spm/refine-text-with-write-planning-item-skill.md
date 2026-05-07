---
title: Improve efficiency and quality using refine records skill with Now Assist Context Menu \(NACM\)
description: Improve record quality by enabling AI-assisted text refinement in the text fields of Product idea, Demands, Epic, Projects, Capability, Features, Stories, Project tasks, Risks, Strategic priorities, Goals, Targets, Initiatives, Feedback, Milestones, and Story forms.
locale: en-US
release: australia
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 4
breadcrumb: [Using Now Assist for Strategic Portfolio Management \(SPM\), Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Improve efficiency and quality using refine records skill with Now Assist Context Menu \(NACM\)

Improve record quality by enabling AI-assisted text refinement in the text fields of Product idea, Demands, Epic, Projects, Capability, Features, Stories, Project tasks, Risks, Strategic priorities, Goals, Targets, Initiatives, Feedback, Milestones, and Story forms.

## Before you begin

The Refine record skill is activated by default. For more information on how to activate the skill if it isn't automatically activated or if you want to change the skill configuration, see [Configure Now Assist Admin features](../concept/configuring-na-spm.md).

If you have users with custom roles that need access to this skill, you must update ACLs for those roles and also add those custom roles to the In product role.

Role required: You only need the roles required for the record type you want to refine.

## About this task

Use the refine records skill and Now Assist Context Menu \(NACM\) to simplify record creation and updates, reduce effort, and improve record quality. Within the rich or long text field of these records, you can use the now assist context menu to shorten or elaborate the text. For example, you can type a short sentence in the rich or long text field or select the existing text and then expand or shorten it. The skill considers other fields in the form to generate meaningful content that improves the record quality. You can also enter a long paragraph in the text field and shorten it without losing key information.

Enable portfolio, project, product, demand managers and agile team members to refine record content efficiently using the Elaborate and Shorten options and create records with sufficient information. The refine records skill helps in improving clarity and completeness of your records and reduces the rework due to missing or unclear information.

The refine records skill and Now Assist Context Menu \(NACM\) is available in Strategic Planning Workspace, Portfolio Planning Workspace, Demand Workbench, Agile Development 2.0 and Project Workspace.

This task is explained using Strategic Planning Workspace as the example.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace**.

2.  From Strategic Planning Workspace, open any record that you want to refine.

3.  Select the text to refine in the text field of your record.

    For example, you can select **Description** text for Feedback record text. You can refer to context menu configuration table to view the forms and text fields which includes NACM.

4.  Select the **Refine with Now assist** menu and then select **Shorten** or **Elaborate** based on your requirement.

    ![Use Now Assist refine menu to refine or improve text of SPM records.](../images/write-planning-items-skill-sp.png)

5.  Select **Replace** to replace the content in the text field.

    ![AI-generated text for a project record using the refine records skill.](../images/write-planning-item-skill-refined-text.png)

6.  From the Refined by Now Assist window, select **Refine** and then select **Shorten** or **Elaborate** to improve the generated text.

7.  When you're finished refining the content, you can replace the existing content with generated content, provide feedback, or copy it.

<table id="choicetable_nly_n5h_1dc"><thead><tr><th align="left" id="d142561e190">

Option

</th><th align="left" id="d142561e193">

Procedure

</th></tr></thead><tbody><tr><td id="d142561e199">

**Provide feedback for the generated text**

</td><td>

If you think that the generated text was helpful, select the helpful icon \(![Helpful icon.](../images/icon-helpful-feedback.png)\). If you think that the generated text wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../images/icon-nt-helpful.png)\).This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d142561e222">

**Copy the text**

</td><td>

Select the copy to clipboard icon \(![Copy to clipboard icon.](../images/icon-copy-spm.png)\) to use the generated text for another purpose, such as pasting it into an email.

</td></tr></tbody>
</table>    **Note:** The refine records skill and Now Assist context menu \(NACM\) is available in the text fields of Product idea, Demands, Epic, Projects, Capability, Features, Stories, Project tasks, Risks, Strategic priorities, Goals, Targets, Initiatives, Feedback, Milestones, and Story forms.

    You can configure the Now Assist context menu for these forms and long text fields.

    |Table name|Roles|
    |----------|-----|
    |dmn\_demand|demand\_user|
    |pm\_project|project\_manager|
    |pm\_project\_task|project\_manager|
    |rm\_story|scrum\_story\_editor|
    |sn\_align\_core\_project|sn\_align\_core.apw\_user|
    |sn\_gf\_strategy|sn\_gf.strategy\_planner|
    |sn\_gf\_goal|sn\_gf.goal\_user|
    |sn\_gf\_goal\_target|sn\_gf.goal\_user|
    |sn\_align\_core\_initiative|sn\_align\_core.apw\_user|
    |risk|project\_manager|
    |sn\_align\_core\_feedback|sn\_align\_core.pf\_user|
    |sn\_milestones\_milestone|sn\_align\_core.apw\_user|
    |sn\_align\_core\_product\_idea|sn\_align\_core.pf\_user|
    |sn\_align\_core\_capability|sn\_align\_core.apw\_user|
    |sn\_align\_core\_scrum\_epic|sn\_align\_core.apw\_user|
    |sn\_align\_core\_feature|sn\_align\_core.apw\_user|
    |sn\_align\_core\_demand|sn\_align\_core.apw\_user|


**Parent Topic:**[Using Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-now-assist-for-spm.md)

**Related topics**  


[Exploring Now Assist for Strategic Portfolio Management \(SPM\)](../concept/exploring-now-assist-for-spm.md)

[Skill inputs for Now Assist for Strategic Portfolio Management \(SPM\)](../reference/skill-inputs-for-now-assist-for-spm.md)

