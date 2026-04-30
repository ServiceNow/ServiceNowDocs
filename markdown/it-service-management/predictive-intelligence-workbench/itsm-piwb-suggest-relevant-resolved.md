---
title: Suggest relevant Resolved Incidents for an Incident
description: Use this template to recommend similar relevant resolved incidents to help expedite your incident investigation and resolution processes.
locale: en-US
release: yokohama
product: Predictive Intelligence Workbench
classification: predictive-intelligence-workbench
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [ITSM Predictive Intelligence Workbench implementation, ITSM Predictive Intelligence Workbench, IT Service Management]
---

# Suggest relevant Resolved Incidents for an Incident

Use this template to recommend similar relevant resolved incidents to help expedite your incident investigation and resolution processes.

## Before you begin

Role required: piwb\_manager or piwb\_viewer

## About this task

This use case template helps you improve your ITSM first-call resolution and reduce the time required to investigate resolution steps for incoming incidents. The template also provides a link to the Predictive Intelligence platform application and associated documentation.

The use case uses a similarity-based predictive model that compares an incoming incident with past resolved incidents for smarter resolution. Similar past active incidents are displayed in Agent assist and also in the Incident form via related search.

**Note:** You will need business users to validate the similar past active incident search results. Contact Customer Service and Support, if necessary, to configure sources for contextual search.

When the use case template shows the label **Pretrained**, you can go directly to the **Testing your models** implementation section. Otherwise, you will begin by creating a machine learning model.

## Procedure

1.  If you started this procedure directly from the Predictive Intelligence Workbench product **Create New from Template** module, and clicked on the product documentation link to get here, skip this step.

    Otherwise, navigate to **Predictive Intelligence Workbench** &gt; **Use Cases** &gt; **Create New from Template**.

2.  Select the **Suggest relevant Resolved Incidents for an Incident** template.

    The **Suggest relevant Resolved Incidents for an Incident** pop-up opens featuring a link to this procedure and a link to the platform Predictive Intelligence product and associated documentation.

3.  Create and train a machine learning predictive model.

    Creating a model involves the following: creating a word corpus, defining a similarity prediction rule, defining the initial training frequency, and defining the refresh frequency.

    1.  [Create a word corpus](https://www.servicenow.com/docs/access?context=create-word-corpus&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

        When creating a word corpus on the Word Corpus Content form, select an incidents-related table, such as Incident \[incidents\] in the **Table** field and define the time frame that best describes the current usage of words in the **Filter** field. For example, if your IT system experienced a major infrastructure change six months back, use data from the last six months only. In the **Field List** field, define only the fields that best capture the words: **Description**, **Short description**, and **Resolution notes**. Defining these alone is typically enough, since the prediction rule is expected to find incidents based on the short description.

        Creating the word corpus prepares you for the next step, creating the similarity prediction rule.

    2.  [Create and train a similarity solution](https://www.servicenow.com/docs/access?context=create-similarity-solution&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

    3.  For this initial model creation, provide the similarity solution definition label `Similar Resolved Incidents` in the **Label** field.

    4.  Set the **Training Frequency** field to **Run Once**.

        You can reset this configuration after you implement this use case into your business processes and have monitored its performance in the Predictive Intelligence Workbench dashboard.

    5.  Set the **Update Frequency** field to **Every 15 minutes**.

        This setting defines the frequency at which past incidents refresh in the search window. When possible, and if applicable, use an existing word corpus, created for another use case to reduce your overall word corpora and ease management of these records. In the **Table** field of the Similarity Definition form, select only those inputs for similarity that will be available at prediction time for incoming incidents. You can select more inputs in the **Test Table** field, if required, for comparison. It is best to start with similar fields for both the **Table** and **Test Table** fields.

        The **Filter** field conditions determine the search window for past resolved incidents. Configure the filter conditions to optimize for the best set of resolved incidents to search within. This includes many considerations, such as, time frame, location, category where incidents are relevant, and more.

    6.  Click **Submit &amp; Train** to create your similarity solution record and train it.

        Alternatively, you can click **Submit** to save your similarity solution record and return to train it later.

4.  [Evaluation and tune your model](https://www.servicenow.com/docs/access?context=review-similarity-examples&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

    If you have a similarity score above 60, but the two incidents do not look similar, you may want to create another model, word corpus, or both by changing inputs and filters. Keep in mind that modifying the solution definition will help you create a new solution, but it will invalidate the previous solution.

    If you want to revert back to the previous solution definition, you will have to reset the parameters and retrain the solution. Therefore, first try creating a new similarity model before creating a new word corpus.

    If you want to adjust the score for your similarity solution, refer to [Update your similarity score threshold](https://www.servicenow.com/docs/access?context=update-similarity-threshold&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

5.  Once you have a satisfactory model, [test the similarity solution prediction](https://www.servicenow.com/docs/access?context=test-similarity-solution-prediction&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

    You can manually provide inputs and select the top similar results outcome values.

6.  Once you have tested the behavior, [configure the user experience](https://www.servicenow.com/docs/access?context=configuring-advanced-settings-ml-solutions&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) layout to show attributed results and actions performed on the results.

    You can configure these results and actions via Workspace UI for Agent assist or via the ServiceNow AI Platform for Contextual Search. Configure actions and search context though **Tables** configuration and user experience and card layout through **Contextual Search** &gt; **Search Result Display Configuration**.

7.  [Integrate trained models by exporting them to production](https://www.servicenow.com/docs/access?context=implement-iterative-solution-updates&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

    **Note:** For details regarding trained use case integration implementation, refer to [Predictive Intelligence Workbench integration and customization](../concept/itsm-piwb-integ-implem-custom.md).

8.  Monitor similarity results and ensure IT agents are providing useful feedback.

    The base-system Predictive Intelligence experience includes a built-in feedback mechanism to discern if the similarity results are useful. Train your IT agents to provide feedback, both online and offline, to capture this data for future reporting. Since this is an unsupervised algorithm, you may need to acquire periodic feedback from the IT agents to check that the similarity model is still providing satisfactory results. This feedback is the only way to determine if the model has drifted and requires new training. Ensure that part of your implementation and integration strategy, as well as your change management process, includes training IT agents to provide similarity results feedback.

9.  Communicate the value of Predictive Intelligence to your stakeholders by linking business key performance indicators \(KPIs\) to machine learning metrics.

    Select one or more KPIs that you think is most beneficial to your IT agents. Create a Performance Analytics dashboard showing the trend of these KPIs. The “likes” you get from your IT agents via the feedback mechanism helps you communicate the value of Predictive Intelligence.

    For information regarding the Predictive Intelligence for Incidents dashboard, refer to [ITSM Predictive Intelligence Workbench dashboard](../../../use/dashboards/application-content-packs/itsm-piwb-incidents-dashboard.md).


