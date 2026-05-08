---
title: Bring in skills through Skills import
description: Import the skills specific to your organization into your Skills Foundation application through the Skills Workspace.
locale: en-US
release: australia
product: Talent Development Core
classification: talent-development-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Skills Workspace, Exploring Skills Foundation, Skills Foundation, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Bring in skills through Skills import

Import the skills specific to your organization into your Skills Foundation application through the Skills Workspace.

## Before you begin

Role required: sn\_skills\_int.admin

Skills import 

## Procedure

1.  Navigate to **All** &gt; **Skills Workspace**.

2.  Select the Lists icon \(![Lists icon](../../ohs-incident-management/image/list-icon-hs.png)\).

3.  Select **Import history** &gt; **Skill imports**.

    The Skill imports display all the imports at various stages. You can have an import in Draft, In-progress, Completed, or Canceled state. You can only have a single import in draft/ in-progress state at any given point. The current import must be canceled or completed to start another import.

4.  Select **Import**.

5.  In the Create a new skill import window, Get started section, enter a description for the import in the Import description field.

6.  Select **Next**.

7.  In the Select a source section, choose how you want to import the skills.

<table id="choicetable_nlp_zwn_4dc"><thead><tr><th align="left" id="d339255e143">

Option

</th><th align="left" id="d339255e146">

Process

</th></tr></thead><tbody><tr><td id="d339255e152">

**File upload**

</td><td>

Access the predefined skills import template so you can import your skills data in the required format. For more information, see [Import skills through file upload](file-upload-skills-import.md).

</td></tr><tr><td id="d339255e171">

**Integration**

</td><td>

Select an integration source to import skills data from the external systems.-   Workday integration

For more information, see [Workday spoke integration in Skills Foundation](../concept/workday-spoke-with-skills-intelligence.md).

-   SAP SuccessFactors integration

For more information, see [SAP SuccessFactors integration Skills Foundation](../concept/sap-successfactors-with-skills-foundation.md).

</td></tr><tr><td id="d339255e226">

**Custom import**

</td><td>

Skills from Credly \(OOTB source\) that are in the Queue \(Dynamic skills table\) are imported automatically. Shows the number of new skills being imported.

 **Note:** You can select specific skills and import them directly from the Queue list. For more information, see [Dynamic skill import for harmonization](dynamic-skill-import.md).

</td></tr></tbody>
</table>8.  Select **Next**.

9.  In the Existing matches section, skills that are identical to the existing skills in the library \(cmn\_skills table\) are identified by AI Search and are not processed again, but are only listed as existing skills.

    You have the following tabs to review the skills:

    -   Summary - Overview of skill matches.
    -   Existing matches - Skills that have been mapped to the existing skills in the cmn\_skills table.
    -   Previously mapped - Skills that have been mapped in the previous import.
    -   Previously discarded - Skills that have been discarded in the previous import.
10. Select **Continue upload**.

11. In the Review upload section, review the uploaded skills displayed in various categories.

    -   Summary - Overview of the uploaded skills.
    -   Errors - Skills with errors. For example, missing description, missing Level type and so on.
    -   Incomplete - Skills that don’t have data in the required fields.
    -   Duplicate in source - Skills that exist more than once in the source file.
    -   Ignored from upload
    -   All - All the uploaded skills.
    You can edit the incomplete skills, duplicate skills, or skills with errors at this stage and correct them before the actual upload.

12. Select **Upload skills**.

    **Note:** The skills with errors are not uploaded.

    The upload process takes some time to complete depending on the number of skills imported. For example, uploading a thousand skills takes around five minutes.

13. In the Review skills section, review the uploaded skills.

    The uploaded skills are analyzed by AI Search and are displayed in the following tabs.

<table id="table_hbm_j13_1cc"><thead><tr><th>

Review skills categories

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Summary

</td><td>

Summary of the skills processed.

</td></tr><tr><td>

Needs review

</td><td>

Review the skills manually for normalization and identifying possible duplication. The AI Search calculates match strength by looking at how closely imported skill names align with existing skill. Evaluate the possible matches to mark new skills by selecting **Create as new**, **Accept possible matches** or **Discard**. You can select multiple skills or all skills at a time and perform these action.You can select multiple skills or all skills at a time and perform these actions. If you select a single skill, a pop-up opens where you can select the possible match for duplication.

</td></tr><tr><td>

All

</td><td>

All imported skills are displayed.

</td></tr></tbody>
</table>    **Note:** You can go back to the previous section using the **Back** button or restart the entire import with the Restart Playbook option in the menu. This option is available from the third step in the import only after the actual import happened.

    You can cancel the import at any stage by selecting the **Cancel import** button.

14. After all the skills are reviewed in the Needs review list, select **Mark as complete** to complete the import process successfully.

    **Note:** New skills are added to the skills library \(cmn\_skills table\) only after selecting **Mark as complete** for the import.


## Result

In the **Skills in this import** tab, you can check all the imported skills. All the skills will be read only after marking the import as complete.

