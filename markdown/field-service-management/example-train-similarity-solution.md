---
title: Example: Suggest similar part requirements for work order tasks
description: This example provides a use case of a medical equipment maintenance manager updating and training a similarity definition solution in the Field Service Management application to suggest the similar part requirements for a work order task.Update and train the Similar Part Requirements similarity definition solution to suggest the required parts for a work order task.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Configuring Predictive Intelligence for Field Service Management, Setting up FSM reports and analytics, Configuring Field Service Management, Field Service Management]
---

# Example: Suggest similar part requirements for work order tasks

This example provides a use case of a medical equipment maintenance manager updating and training a similarity definition solution in the Field Service Management application to suggest the similar part requirements for a work order task.

## Problem Scenario

Joy, a medical equipment maintenance manager, expressed dissatisfaction with the relatively low initial success rates of servicing medical equipment. This issue emerged primarily because technicians didn’t have access to the necessary parts during their first-time visits. To address this problem, the manager must add the part requirements into the work order task based on the previous service history. However, this process is time-consuming and requires a thorough assessment of the tasks.

## Solution: Use Predictive Intelligence similarity solution

Joy decides to implement Predictive Intelligence for Field Service Management to improve the task closure rating by automatically suggesting the similar part requirements for work order tasks. This is achieved by training the machine-learning solution to leverage the past service history of the work order tasks.

Now, Joy collaborates with the administrator to train the machine-learning solution provided in Predictive Intelligence for Field Service Management. This solution is designed to collect and compare existing records with new ones. Leveraging the predictive intelligence feature, the administrator trains the Similar Part Requirements similarity solution to automate the process of suggesting the similar necessary part requirements for work order tasks. This is achieved by comparing the part requirement record with the work order task record and providing relevant results.

To train the solution, Joy enters the following values in the Similarity Definition form based on the instructions described for training the similarity solution. For more information, see [Train similarity solution to suggest similar parts for a work order task](example-train-similarity-solution.md#).

|Field|Value|
|-----|-----|
|Label|Similar Parts Requirements|
|Name|ml\_sn\_sn\_fsm\_ml\_global\_similar\_part\_requirements|
|Table|Part Requirement \[sm\_part\_requirement\]|
|Fields|Short description, Description, Skills, and Asset Display|
|Test Table|Work Order Task \[wm\_task\]|
|Test Fields|Description, Short description, skills, and Asset fields|
|Filter|\[Work order task\_Asset\] \[is\] \[not empty\]|
|Processing Language|English|
|Stopwords|Default English Stopwords|
|Training Frequency|Every 30 days|
|Update Frequency|Every 1 day|

## Train similarity solution to suggest similar parts for a work order task

Update and train the Similar Part Requirements similarity definition solution to suggest the required parts for a work order task.

### Before you begin

Role required: wm\_admin

### About this task

The Similar Part Requirements similarity solution collects and compares your existing records with new similar records. It helps to suggest the necessary parts for work order tasks that have been frequently used in the past. This solution utilizes the predefined parts requirement record stored in the Parts Requirement table to provide accurate recommendations.

To customize part suggestion based on specific work order task fields, you must modify this similarity solution. For a similarity solution to work correctly, the Part Requirements \[sm\_part\_requirement\] table in the Work Order Task \[wm\_task\] database must have at least the required number of records set in the configuration of your ServiceNow instance. The default minimum number required is 10,000.

### Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solution Definitions**.

2.  In the Similarity Definitions list, search for and select the Similar Part Requirements solution definition \(ml\_sn\_sn\_fsm\_ml\_global\_similar\_part\_requirements\).

3.  On the Similarity Definition form, verify the default field values for part requirements.

    **Note:** If the application scope isn't set to Predictive Intelligence for Field Service Management application, you can’t edit the form and a warning message appears. To make the form editable, click the word **here** at the end of the message.

<table id="table_bxj_sbx_4jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique name for your similarity solution.

</td></tr><tr><td>

Name

</td><td>

As you enter your solution Label value, this field automatically populates with a system-assigned name that's similar to your label value.

</td></tr><tr><td>

Table

</td><td>

Table that contains the part requirements record that you want to compare to other similar records and train against. After you assign a table value, a link appears in the form that shows the number of records that match your filter conditions.

</td></tr><tr><td>

Fields

</td><td>

Field types that contain the text of the part requirements records whose work order tasks you're trying to identify. You can select the columns from the Part Requirement \[sm\_part\_requirement\] table for similarity comparison with the work order task short description and other fields.

</td></tr><tr><td>

Test Table

</td><td>

Table that contains the work order task records that you want to compare with the part requirements records.

</td></tr><tr><td>

Test Fields

</td><td>

Fields from the work order task that are likely to contain text that is similar or relevant to the part requirements fields. These fields are used for similarity match with the part requirement fields.

</td></tr><tr><td>

Filter

</td><td>

Filter conditions applied on the field records to filter work order task records for part requirement recommendations.

</td></tr><tr><td>

Processing Language

</td><td id="processing">

Dominant language of the dataset you're training on the solution definition. If the dataset language is English, choose **English**.**Note:** The term processing indicates some of the language-specific steps used as part of training a solution. These steps might include tokenizing words, removing stop words, and stemming.

</td></tr><tr><td>

Stopwords

</td><td id="stopwords">

Common terms in the processing language that are excluded from the search, for example, prepositions.When you select your processing language, the system automatically adds a Stopwords list that uses the same language. For example, if your processing language is Italian, the **Default Italian Stopwords** list appears.

</td></tr><tr><td>

Training Frequency

</td><td>

The frequency with which the model for the similarity solution definition must be retrained.

</td></tr><tr><td>

Update Frequency

</td><td>

Frequency of how often to include new records in the model to retrieve the similarity results.

</td></tr></tbody>
</table>    For more information, see [Create and train a similarity solution](https://www.servicenow.com/docs/access?context=create-similarity-solution&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

4.  In the Training Request Schedule related list, update the schedule for training the Similar Part Requirements solution definition.

    By default, the training request schedule is **Periodically** and runs after every 30 days.

5.  Click **Update &amp; Retrain**.

6.  Open the Similar Part Requirements solution definition \(ml\_sn\_sn\_fsm\_ml\_global\_similar\_part\_requirements\) and in the ML Solutions related list, view the training solution progress in the **Progress** column.

    When **Progress** is 100%, in the ML Solutions related list, you can include more useful content in the part requirements suggestions by reviewing the similarity examples based on the similarity score and updating the similarity score threshold value.

7.  Update the similarity score threshold.

    1.  In the **Active** column, click the link for the solution.

    2.  Review the similarity examples by clicking the **Similarity Examples** related link on the ML Solution form.

        For more information, see [Review solution similarity examples](https://www.servicenow.com/docs/access?context=review-similarity-examples&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

    3.  In the Solution Statistics related list on the ML Solution form, enter the required value in the **Similarity Score Threshold** field, right-click the ML Solution form, and then click **Save**.

        For more information, see [Update your similarity score threshold](https://www.servicenow.com/docs/access?context=update-similarity-threshold&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).


### Result

When the solution is complete, the required part similar to the fields selected for a work order task are sent as part requirement recommendations.

