---
title: NLU Model Performance
description: Use NLU Model Performance to see how well your models predicted intents in Virtual Agent \(VA\) based on end-user confirmation.
locale: en-US
release: xanadu
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2025-02-04"
reading_time_minutes: 8
breadcrumb: [NLU Workbench - Advanced Features, Natural Language Understanding, Enable AI experiences]
---

# NLU Model Performance

Use NLU Model Performance to see how well your models predicted intents in Virtual Agent \(VA\) based on end-user confirmation.

## Summary usage

The NLU Model Performance application provides an analysis and report of how well your NLU models predict VA users' intents from their utterances. As NLU models for VA are updated, published, and deployed, you can use NLU Model Performance to review the efficacy of the intent predictions they make. If these predictions are skipped, it’s because they're unable to predict an intent with a high enough confidence score for the model. To improve VA topic prediction, the system groups unsupported VA utterances into clusters for an analysis and then generates a report that identifies the outcome of the analysis.

To access this application, use the nlu\_admin or admin role and navigate to **All** &gt; **NLU Workbench** &gt; **Performance**.

**Note:** To use NLU Model Performance, you must first have at least 5,000 VA utterances in your instance. With the nlu\_admin role, you can modify this limit by resetting the **sn\_nlu\_workbench.glide.nlu.performance.min\_clustering\_records** property.

## Installation

NLU Model Performance is an application available on the ServiceNow® Store. To use this application, ensure that the NLU Workbench - Advanced Features \(sn\_nlu\_workbench\) plugin is active on your instance. For more information, see [Install NLU Workbench - Advanced Features](../task/install-nlu-workbench-adv-features.md) and [Activate the NLU Workbench](../task/activate-nlu-workbench.md). Because NLU Model Performance relies on data coming in from VA, ensure that the Glide Virtual Agent \(com.glide.cs.chatbot\) plugin is also active. See [Activate Virtual Agent](https://www.servicenow.com/docs/access?context=activate-virtual-agent&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

## Configuring Conversational Interfaces settings for ServiceNow NLU

To help with tracking NLU performance, you must first configure the Conversational Interfaces \(CI\) settings in Virtual Agent. To access these settings, navigate to the top of the **NLU Model Performance for Virtual Agent** landing page and click **Conversational Interfaces Settings**. This action takes you to the CI settings page in Virtual Agent, as shown in the image below.

![Setting Conversational Interfaces settings](../images/nlu-model-performance0.png)

To configure the settings, you need to use the virtual\_agent\_admin or admin role. For configuration guidance, see [Implement NLU in Virtual Agent](https://www.servicenow.com/docs/access?context=implement-nlu-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US) and [Enable NLU languages in Virtual Agent settings](https://www.servicenow.com/docs/access?context=enable-langs-va-gen-settings&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

## Reviewing the user interface \(UI\)

The NLU Model Performance UI is comprised of the listed parts below, which are highlighted in the following image that shows the NLU Model Performance default landing page.

-   -   The **Performance** tab and its colored chart which shows data describing scenarios that occur when users interact with VA. This chart is segmented in shades of three colors, each representing a user scenario. The rows in the chart that have text and percentages are referred to as the legend. The three scenarios in the first row of the legend have two outcome scenarios beneath them in the second row. The bars underneath the legend correspond to the colors of the scenarios above them. These bars range in size based on the percentage value for each scenario.
-   For example, the dark blue bar shows you that 10% of this batch of VA users confirmed that the system presented them the correct topic to use for their VA chatbot conversation, and that 58 % of the users \(represented by the dark red bar\) confirmed that the topic presented to them was incorrect. Residing between these two scenarios is a scenario showing that 32% of the users \(represented by the dark brown bar\) didn't make any confirmation at all.
-   It's a good idea to toggle the **Show all bars** filter back and forth at any time to see or hide the colored bars and their associated scenarios in the chart. Note also that when you first access NLU Model Performance, the default view of the chart shows only the first row of scenarios and the first row of bars.
-   There are also other views you can see depending on which scenario you're viewing. For example, when you first access NLU Model Performance and you click a scenario in the first row of the legend, the system hides the bars of the other two scenarios. This helps to keep the UI less cluttered because it partially isolates the scenario you're focusing on from the rest of the scenarios. These actions don't change any data, they simply show you different views of the legend and bars within the chart.
-   The **Unsupported utterances** tab, which shows utterances that are grouped into clusters for use in the performance analysis. This section of the UI is where you can navigate to and return from the Expert Feedback Loop application, and also where you can run the analysis.

    Unsupported utterances are different from irrelevant utterances. For more information, see [Irrelevance detection in NLU](irrelevance-detection-nlu.md).

-   The **Performance Details** section located underneath the bar chart. This section has these four columns: **Utterance**, **Predicted intent**, **Prediction model**, and **Prediction outcome**. The details shown in this section interact with the legend data and bar data above them.

![NLU Model Performance](../images/nlu-model-performance00.png)

## Reviewing the VA user scenarios

In the legend section of the UI, the text and percentages are accompanied by Information icons. Point to an icon to invoke the definition for its user scenario. Refer to the table below to see the definitions.

|Scenario|Definition|
|--------|----------|
|**User confirmed as correct**|The correct topic was presented to the end user and the end user has confirmed it is correct.|
|Topic launched, user confirmed as correct|The topic was launched and the user confirmed it is the topic they needed.|
|Topic menu presented, user selected one|Multiple topics were shown as a menu to the user and the user chose one of the topics to address their need.|
|**User made no confirmation**|The topic was launched but the user did not confirm whether or not it met their need.|
|No prediction made, fallback topic launched|No predictions were made and the fallback topic was launched.|
|Topic launched, no user confirmation|The topic was launched but the user did not confirm whether it was correct.|
|**User confirmed as incorrect**|The topic\(s\) presented did not address the end user's needs, and the user has confirmed it is not correct.|
|Topic launched, user confirmed as incorrect|The topic was launched and the user confirmed it was not correct.|
|Topic menu presented, user selected none|Multiple topics were shown as a menu to the user and the user decided none of the topics were relevant and did not choose any topic.|

## Using the Language and Model filters

On the Performance tab, you can see the Language and Model filters. Next to them, you can also see the most recent Date range values you set above the legend and bars of the chart. Click the **Language** filter to see all languages that are available in NLU. Click the **Model** filter to see all prediction models that are available in your instance. The default setting for the **Language** filter is **All languages**, and the default setting for the **Model** filter is **All models**.

The Language and Model filters interact with each other. For example, if you choose `French-fr` in the **Language** filter, the **Model** filter automatically shows all prediction models in your instance that use the French language, as shown in the following image. ![The Language and Model filters interact with each other.](../images/nlu-model-performance1.png)

There are other interactions. For example, from the default view of the NLU Model Performance landing page:

-   If you select a specific model from the **Model** filter, the **Language** filter value is updated to display the language of the selected model.
-   If you select a specific language from the **Language** filter, the **Model** filter only displays models of that selected language.

Underneath the Language and Model filters, you can see the **Include translated conversations** switch. To include the performance of VA conversations that were translated to your primary language using dynamic language translation, toggle the switch to the right so it changes color from grey to green. When you do this, the bars in the charts legend may also change position and colors. You can manage dynamic language translation in the **Conversational Interfaces Settings**.

## Setting the Date range

On the Performance tab, use the **Date range** to define how far back you want the system to pull VA data from. Choose **Past 30 days**, **Past 60 days**, **Past 90 days**, or **Custom range**. The further back you go in the date range, the more data you will have in your analysis.

![If you want your report to cover data that extends back beyond 90 days, then use the Custom range.](../images/nlu-model-performance3.png)

## Running an analysis

To run a performance analysis, click the **Unsupported utterances** tab. This section of the UI shows rows of expandable clusters containing VA utterances where NLU didn't make a topic prediction, or where the VA end-user confirmed that the predicted topic was incorrect. The next thing you want to do is to click **Expert Feedback Loop**. This action takes you to the [NLU Expert Feedback Loop](nlu-expert-feedback-loop.md) application where you review and provide feedback on the utterances that were pulled in from VA.

![Navigating to the Expert Feedback Loop and returning to NLU Model Performance](../images/nlu-model-performance4.png "Reviewing unsupported utterances")

When you leave the Expert Feedback Loop application and return to NLU Model Performance, click the **caret** icon in any cluster to open it. Within the cluster you can then see the top most representative VA utterances, as shown in the following image.

![Opening a cluster of utterances so you can see the VA utterances inside it.](../images/nlu-model-performance5.png "Reviewing the top representative utterances in a cluster")

Click **Run analysis** or **Rerun analysis**, whichever is available. Each time you run an analysis, the system pulls the most recent VA utterances into the analysis.

**Parent Topic:**[NLU Workbench - Advanced Features](nlu-workbench-advanced-features.md)

**Related topics**  


[Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)

[Natural Language Understanding in Virtual Agent](https://www.servicenow.com/docs/access?context=va-NLU&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)

