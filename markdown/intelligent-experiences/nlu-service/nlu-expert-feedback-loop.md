---
title: NLU Expert Feedback Loop
description: Provide feedback on Virtual Agent chat log utterances to help the system continuously learn and to better predict user input.
locale: en-US
release: xanadu
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 14
breadcrumb: [NLU Workbench - Advanced Features, Natural Language Understanding, Enable AI experiences]
---

# NLU Expert Feedback Loop

Provide feedback on Virtual Agent chat log utterances to help the system continuously learn and to better predict user input.

Embedded video: NLU Expert Feedback Loop, presented by the ServiceNow Virtual Agent Academy

## Summary usage

The Expert Feedback Loop takes data from your instance and provides it to you for feedback. This data comes from your users' Virtual Agent \(VA\) chat logs and includes utterances from those logs. Using the nlu\_admin role, navigate to **All** &gt; **NLU Workbench** &gt; **Expert Feedback Loop** and mark each utterance in a model by confirming whether the utterance is correct \(match\) or incorrect \(mismatch\) to an intent. This feedback helps the model to continuously improve the model performance.

## Installation

Expert Feedback Loop is part of the NLU Workbench - Advanced Features app available on the ServiceNow® Store.

To use Expert Feedback Loop, ensure that the NLU Workbench - Advanced Features \(sn\_nlu\_workbench\) plugin is active on your instance. For more information, see [Install NLU Workbench - Advanced Features](../task/install-nlu-workbench-adv-features.md) and [Activate the NLU Workbench](../task/activate-nlu-workbench.md).

Because Expert Feedback Loop relies on the data from VA chat logs, make sure that the Glide Virtual Agent \(com.glide.cs.chatbot\) plugin is also active. See [Activate Virtual Agent](https://www.servicenow.com/docs/access?context=activate-virtual-agent&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

## Importing expert feedback loop data between instances

Before you start an import, make sure you have access to the data in your instance and have enough data to proceed with your feedback.

If you're working in a sub-production instance, you must import the feedback data from the **open\_nlu\_predict\_intent\_feedback** table in your production instance to your sub-production instance. For guidance on how to import, see [Importing from another ServiceNow instance](https://www.servicenow.com/docs/access?context=c_ImportingFromAnotherSNInstance&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

Here are a few data scenarios regarding the system behavior for the NLU models that house the feedback loop utterances.

-   If you move a model to a different instance, the feedback data persists.
-   If you upgrade the instance, the feedback data persists.
-   If you clone an instance, the data does not persist, so you need to follow the procedure referenced above to import the data onto the cloned instance.

## Feedback context and access

The Expert Feedback Loop provides a mechanism for you to improve NLU models deployed to VA through feedback that you provide on a select subset of utterances. For each utterance, you are asked to confirm the predicted intent or to provide the correct intent that the utterance belongs to. After this feedback is complete, the data is used to tune the model performance, resulting in an improved model that can now be redeployed to gather more end user data. This is an iterative cycle that allows the system to continuously collect data, learn from the feedback you provide, and use that feedback to further improve your NLU models.

Once every 30 days, the system pulls up to 300 utterance samples from VA chat logs to the Expert Feedback Loop. The utterances are selected for feedback based on how well they represent all the utterances in the logs. Every utterance sampled from VA chat logs has a predicted intent picked by the system.

You can also set the number of utterances you want to be pulled from VA chat logs by adjusting the setting for the **glide.mlpredictor.option.nlu.activeLearning.label\_candidate\_table.max\_response\_size** system property.

Further information on the process of pulling utterances from VA chat logs can be found in the sections Procuring additional VA feedback data on demand and Using the Active Learning job, below.

As you review the utterances, decide whether each utterance belongs to its predicted intent or should be moved to a different intent. If you aren't sure about the correct intent, the utterance can be marked to revisit for further review. After you have marked at least 100 utterances with your feedback, the system uses all the marked utterances to tune and improve the model.

## Reviewing your VA chat log utterances

Now that you're in the loop, you can see in the following image a list of NLU utterances that support the intents in the VA models. Each page of the list shows approximately 20 utterances per page. Your goal is to review each utterance and mark its relationship status to a given VA intent. You mark each utterance with either the **NLU\_Match**, **Mismatch**, or **Unsure** value.

Marking an utterance as **NLU\_Match** means that you agree with the NLU prediction for that utterance. Marking an utterance as **Mismatch** means that the utterance belongs to a different intent, and if you select **Mismatch**, a dropdown of intents appears so you can select the correct intent. If you aren't sure which intent is correct, you can mark it as **Unsure**.

Utterances that are marked and saved with the **NLU\_Match** value or the **Mismatch** value are moved to the **Completed reviews** section. Utterances that are marked and saved with the **Unsure** value are moved to the **Needs further review** section.

Here's a scenario for the basic steps you use to complete your utterance reviews:

1.  At the top of the Export Feedback Loop screen, select a model you want to review in the **Expert Feedback Loop for** prompt. Within this feature, in some ways it doesn't matter which model you choose because these models serve mainly to house the utterances you are marking in your reviews. So in this example scenario, you decide to select the **IT Model** model, which has five intents and many utterances within each of those intents. The number of utterances you need to review are shown next to the name of the predicted intent, as shown in the following image. The intents in these models are listed in the **Predicted intents** column on your screen. Although you can review and mark utterances in any of the predicted intents, it's a better idea to complete the reviews consecutively in the order the intents first appear. For example, begin with the **ad\_password\_change** intent and then onward to other predicted intents.
2.  Click the **ad\_password\_change** intent so it loads its utterances into the **To do** section for your review.
3.  Review the 15 utterances in the intent. In this scenario, you've started by correctly marking the I want to change my AD password utterance as a match to the **ad\_password\_change** intent.
4.  Click **Save feedback**.

    Result: The system moves the utterance you marked over to the **Done** section of the screen. At the same time, the count of **To do** utterances drops from 15 to 14, while the count on the **Done** section rises from 0 to 1. If you had also marked another utterance with the **Unsure** value and saved that change, the count of utterances in the **Needs further review** section would also rise from 0 to 1.

    **Note:** If you don't know which intent best matches the utterance, mark it with the **Unsure** value. This action moves the utterance over to the **Needs further review** section, giving you time to mark other utterances in the **To do** section that may be easier to match or mismatch to an intent. You can always return to the **Needs further review** section to mark utterances that are more difficult to pin down to a specific intent.

5.  Repeat steps 1 through 4 as you move through the remaining intents in the **Predicted intents** column.

![Select a predicted intent so you can mark its utterances during review](../images/nlu-expert-feedback-loop1.png "Marking utterances as matched or mismatched to a VA intent")

The utterances in the **ad\_password\_change** intent are easy to mark as a match to its predicted intent because there's at least one utterance within the intent that has the word password in it.

When you have finished reviewing the utterances in the predicted intent and you click **Save feedback**, the screen refreshes to highlight the next predicted intent in the model.

If you want to see your utterances grouped by their value, click the **Showing** filter and select one of the options in its prompt. The values are **All**, **NLU\_Match**, and **Unsure**.

## Using the card view option to review your utterances

Your Expert Feedback Loop utterances appear on the **To do** section in a list view by default, as shown in many of the images you've seen so far above. However, you can also choose a different view that shows each utterance framed within a card. If you choose this option, each utterance appears on the page in groups of five. While still within the list view, click the **card** icon.

![How to activate the card view](../images/nlu-expert-feedback-loop4.png)

Result: The card view replaces the list view. Note the left and right arrows on either side of the page of utterance cards. When you click the right arrow, it turns the page to the next set of five cards. When you click the left arrow, it turns the page to the previous set of five cards. If you want to switch back to the list view instead of the card view, click the **list** icon as shown in the upper right hand corner of the image below.

![How to switch back to the list view](../images/nlu-expert-feedback-loop4a.png)

## Changing an utterance value

If you mark an utterance but then change your mind on the value you chose, you can resolve the issue by clicking on **MisMatch** and selecting another intent. Click **Save feedback** to save the change.

## Unsaved feedback

If you finish and log out of a session of marking your utterances, but forget to save your changes, select **Unsaved changes** from the **Showing** prompt. This action displays all the utterances you have given feedback for but haven't saved yet.

## Procuring additional VA feedback data on demand

To get more data from the VA chat logs to use in the Expert Feedback Loop, take the following steps.

1.  Use the nlu\_admin role and navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs** &gt; **Active Learning**.
2.  Click **Active Learning**.

    ![Opening the Active Learning job](../images/nlu-expert-feedback-loop5a.png)

3.  Click **Execute Now**.

    ![Click the 'Execute Now' button to start the Active Learning job](../images/nlu-expert-feedback-loop5b.png)

4.  Increase or set the values in the following four NLU system properties.

-   **glide.mlpredictor.option.nlu.activeLearning.va\_chat\_logs.max\_row\_limit - 3000**
-   **glide.mlpredictor.option.nlu.activeLearning.label\_candidate\_table.max\_data\_size - 10000**
-   **glide.mlpredictor.option.nlu.activeLearning.label\_table.max\_data\_size - 10000**
-   **glide.mlpredictor.option.nlu.activeLearning.label\_candidate\_table.max\_response\_size-300**

To see how these properties work within the context of other NLU properties, see [NLU Workbench properties](../reference/nlu-instance-properties.md).

## Reviewing uncategorized utterances

As part of the feed from VA chat logs to the Expert Feedback Loop, the system collects and displays in a list any utterances in your instance that aren't part of a VA intent. You access these utterances by selecting **Uncategorized** in the **Expert Feedback Loop for** prompt at the top of your screen.

When the screen refreshes, these utterances are shown in the **Utterance** column of the **Uncategorized utterances** section of your screen.

**Important:** It is extremely important to provide feedback on this set of utterances because the system is suggesting there is no associated intent for these utterances. By confirming this lack of association or by associating these utterances with an existing intent, you are helping the model to learn correctly.

Here are the steps you use to connect an uncategorized utterance to an intent:

1.  In the **Utterance** column, select an utterance from the list.
2.  In the **Corrected Intent** column, search and select an intent and its model from the prompt that you think is the best match for the utterance.

For example, a good pairing for this connection is the Can I trade my ESPP? utterance from the **Utterance** column and the 401kBenefitsInquiry intent from the **Corrected Intent** column, as shown in the image below.

**Note:** The **Corrected Intent** column enables you to search for and use all intents across all models in your instance.

![The number of uncategorized utterances depends on the Virtual Agent chat logs that are pulled into the daily feed to the Expert Feedback Loop](../images/nlu-expert-feedbacl-loop6.png "Pairing an uncategorized utterance with an intent and its model")

Regarding the image above, let's cover a few items that help describe how the uncategorized utterances page works, as follows. The **To do** section collects utterances that must be connected to an intent. On this particular day we see there are 120 such utterances. Note that the **Done** section on the screen has no utterances because you've not taken any action yet.

Note also that there's a vertical bar to the far right of the screen where you can scroll up and down to navigate the list of utterances. At the bottom of this scrolling screen, there are arrows that point left and right so you can to turn to the next or previous page of the full utterance list for the day.

Note also that when you do take action to make a connection, the **Save feedback** button, normally active by default, deactivates because the system recognizes your action and automatically saves your change.

## Expert Feedback Loop data in the Tune Model phase

The **Tune model** button in the Expert Feedback Loop is always enabled and supports the experience of moving utterances from the Expert Feedback Loop **Done** tab to the model and its test set. Use the nlu\_admin role to click this button any time you need to tune or retune your model.

![Tuning your model optimizes it prior to publishing it](../images/nlu-expert-feedback-loop7.png)

After reviewing utterances in the Expert Feedback Loop, you can push a portion of the feedback data to the default test set of your model. These utterances are then directly added to the **Test utterances** tab of your model. This helps you to continuously maintain and update your test set with real end user utterances. The system tracks the source of the test utterances for visibility into whether they came from the Expert Feedback Loop or from another source.

If you click the **Tune model** button before you have marked and saved at least 100 utterances, the screen refreshes to remind you that your model performance increases in quality when you have passed the 100 utterance feedback goal, as referenced in the text in the image below.

![Click the'Tune model anyway' button any time to improve your model but the tuning results are best if you first establish a goal that is at least 100 marked utterances](../images/nlu-expert-feedback-loop8.png)

As you keep marking and saving your feedback data, you can see the ratio of reviewed utterances \(in green\), and those that are still available for review \(in white\) on the progress bar image below.

![The progress bar shows you how many utterances have been reviewed, and those that are available for review.](../images/nlu-expert-feedback-loop8a.png)

On the **Tune your model** image below, you can see the default 60/40 percentage split for your model training set and your model test set. You can adjust these default values if needed by selecting your own chosen numbers in each of the two **\(%\)** boxes. Once you're satisfied with your percentage split, click the **Tune** button to tune your model based on the percentage values you chose.

**Note:** If you click the **View feedback** caret, it takes you to an Expert Feedback Loop screen where you can continue reviewing, marking, and saving your feedback utterances.

![Set your percentage split values before you click the Tune button](../images/nlu-expert-feedback-loop9.png)

## Using the Active Learning job

Scheduled jobs, also known as batch jobs or batch scheduling, are automated pieces of work that are performed at a specific time or on a recurring schedule. Many jobs run on schedules but we're focusing now on the Active Learning job as an example.

Here are three things you can do when using the Active Learning job.

-   Change the repeat frequency interval with which the Active Learning job will be set to run.
-   Check when the next scheduled run is set for the Active Learning job.
-   Execute the Active Learning job whenever you want \(on demand\).

Here are some steps to use to get started.

1.  Using the nlu\_admin role, navigate to the **All** field and type **sysauto\_script.list**, then press the **return** key on your keyboard. The screen refreshes to show the Schedule page, which lists all of the scheduled jobs.

    ![Schedule page.](../images/nlu-expert-feedback-loop10.png)

2.  On the Schedule page, click **Active Learning**. A record for the Active Learning job appears, as shown in the image below.

    ![Open the calendar](../images/nlu-expert-feedback-loop11.png)

3.  On the Active Learning record, configure the following fields.
    -   In the **Run** field, select one of the eight Repeat Interval options for the job. The options are: Daily, Weekly, Monthly, Periodically, One, On Demand, Business Calendar:Entry Start, and Business Calendar:Entry End.
    -   In the **Repeat Interval** field, enter the number of days you want between now and the next repeat interval for the Active Learning job.
    -   In the **Starting** field, click the Calendar icon and choose the day and time for the next Active Learning job interval.
    -   Click the **Update** button to save your configurations or click the **Execute Now** button to start the Active Learning job run.
    -   To verify when the next Active Learning job runs, navigate to the **All** field and type **sys\_trigger.list**, then press the **return** key on your keyboard. The Schedule page appears. Click **Active Learning**. The Schedule Item/Active Learning record appears and populates the **Next action** field with the date and time for the next Active Learning job run.

        ![The Active Learning record](../images/nlu-expert-feedback-loop12.png)


Detailed information about NLU's Active Learning job can be found in this KB article on the Support portal: [KB1633901](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1633901).

**Parent Topic:**[NLU Workbench - Advanced Features](nlu-workbench-advanced-features.md)

