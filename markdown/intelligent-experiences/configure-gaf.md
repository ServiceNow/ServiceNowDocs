---
title: Configure Group Action Framework
description: Set up Group Action Framework \(GAF\) to improve the response quality, recall speed, and consistency of AI agents.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure, Now Assist AI agents, Enable AI experiences]
---

# Configure Group Action Framework

Set up Group Action Framework \(GAF\) to improve the response quality, recall speed, and consistency of AI agents.

## Before you begin

There must be a ml\_platform read ACL for GAF to be configured. If there is no read ACL present, you must create it and grant the appropriate role access, such as admin, ml\_admin, or sn\_aia.admin. This is required for GAF to access Machine Learning tables and services. If your ACL is not configured correctly, you may see the error "Failed to initialize pipeline: Failed to load message\_content dataset. No columns to parse from file."

To access GAF's optimized prediction feature, you can enable Now Assist in AI Search. For more information, see [Setup AI Search for Group Action Framework](setup-ai-search-gaf.md).

Role required: sn\_aia.admin

## About this task

You can activate GAF to have AI agents use indexed clusters that perform LLM executions on representative records rather than all records. GAF is used by some AI agents and agentic workflows to work optimally. For more information about GAF and how it works, see [Group Action Framework](../concept/group-action-framework.md).

You can have different GAF configurations for different agentic workflows and Now Assist applications. You must configure each agentic workflow or application separately.

**Important:** Setting up GAF can take some time, between 10 minutes up to an hour, depending on the number of records in the grouping. The script runs in the background.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scripts - Background**.

2.  Paste the following code into the text area.

    Do not run the script until the groupSkillID and the actionSkillID variables have values. The values are acquired in the following steps.

    ```
    var groupSkillId = ""; 
    var actionSkillId = ""; 
    var topicSkillId = "43bce9e477e012103f075cea5b5a998f"; 
    new sn_gaf.GAFUtils().activate(groupSkillId, topicSkillId, actionSkillId, "run_once");
    ```

    The topicSkillId is the same for all GAF setups.

3.  In a new browser tab, navigate to the Now Assist Skill Config \[sn\_nowassist\_skill\_config\] table by entering `sn_nowassist_skill_config.list` in the filter navigator.

4.  In the **Name** field, enter `*grouping` and search to see the grouping records that are associated with your agentic workflows and Now Assist applications.

    ![Now Assist Skill Config table filtered by *grouping in the Name field](../image/gaf-grouping-search.png)

5.  Open the grouping record for the agentic workflow or application that you want to configure.

6.  In the Now Assist Config Var Set related list, open the Grouping inputs record.

7.  Confirm that the filters for the grouping include all the records you want to index.

    If you want to add filters to change what records are included in the GAF setup, do so here. The more records that you include means that you have a longer setup time, but they can help increase the quality of your results. You should have at least 2000 records for successful clustering.

    **Note:** Your current scope should be Group-Action Framework to make changes.

    ![Now Assist Skill Config Var Set record with Variables set to Incident table, short description field, and filter State is closed](../image/gaf-grouping-inputs.png)

8.  Return to the Now Assist Skill Config Grouping record and copy the sys\_id.

    You use this sys\_id and two other sys\_ids in the background script function call.

9.  In the browser tab with the background script, paste the sys\_id in the script between the quotation marks for the groupSkillId variable.

    Your `groupSkillId` variable should be in the same format as the `topicSkillId` variable.

10. In the tab with the Now Assist Skill Config record, return to the Now Assist Skill Config table and search for `*action strategy` to find the action strategy skill config for the application.

    Make sure that the record is for the same application. If you pasted the sys\_id of the GAF ITSM grouping, you must open the GAF ITSM action strategy.

11. Open the action strategy record for the application that you’re configuring.

12. Copy the sys\_id of the action strategy record.

13. In the browser tab with the background script, paste the sys\_id in the script between the quotation marks for the actionSkillId variable.

    Your `actionSkillId` variable should be in the same format as the `groupSkillId` and `topickillId` variables.

    ![Completed GAF script with all three values populated](../image/gaf-script.png)

14. Run the background script by selecting **Run script**.

    Running this background script creates a scheduled job called GAF - Run Offline Flow. You can view the scheduled job on the Scheduled Script Executions \[sysauto\_script\] table.


## Result

GAF is configured on your instance for that Now Assist application and can be used by AI agents to find related records.

## What to do next

To verify that grouping and action outputs have been generated, go to the ML Solution \[ml\_solution\] table to check if the clustering solution is running or completed. If it is complete, check the following tables to see records for groups, clustered records, and down-sampled records per group are present.

-   GAF record group \[sn\_gaf\_record\_group\]
-   GAF record group detail \[sn\_gaf\_record\_group\_detail\]
-   GAF action strategy result \[sn\_gaf\_action\_strategy\_result\]

You can repeat this procedure for additional agentic workflows and Now Assist applications.

You may see the error "Failed to initialize pipeline: Failed to load message\_content dataset. No columns to parse from file." when trying to configure GAF. This could be because your instance lacks data on the table or filters you configured excluded records from the table. You can reach out to Now Support for additional assistance if you cannot resolve this error.

