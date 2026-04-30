---
title: Factors in Advanced Risk Assessment
description: Factors are questions that you can use to analyze risks. Factors appear on a risk assessment instance.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Advanced Risk Assessment, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Factors in Advanced Risk Assessment

Factors are questions that you can use to analyze risks. Factors appear on a risk assessment instance.

Factors are questions that appear during the risk assessment. To use Advanced Risk Assessment, you must first define these factors and configure a risk assessment methodology \(RAM\). For more information on RAMs, see [Configure a risk assessment methodology](../task/configure-ram.md). Each factor or question has a response. There are different types of factors:

-   Manual factor: A factor that requires human input. The response is a manual response. An example is your name.
-   Automated factor: A factor whose response is automatically calculated. An example is the temperature in your city today. The information is fetched from external sources.
-   Scripted automated factors: A factor that is used to write scripts.
-   Group factor: A set of factors that are grouped logically.

These factor types are explained more in the following sections. After you define the factors and publish them, you can configure a RAM and associate the factors to the assessment types within the RAM. The RAM forms the basis of the risk assessment. Publish each of the selected assessment types, and then publish the RAM. Users with the sn\_risk.user role can select the assessment types for which the assessment must be performed.

Your risk assessment instance is then created. Its properties depend on the assessment types and options that you selected for your RAM. The risk assessment instance is where the risk assessor evaluates the risks. As a question, a factor can be used in multiple assessment types. For example, a question such as "What is the probability of a building getting flooded?" can be a part of either an inherent assessment or a residual assessment after the control effectiveness assessment.

**Note:** A factor can be used in multiple assessment types, but it can be used in only one RAM. A factor that is created and used in one RAM cannot be reused in other RAMs.

## Types of factor contributions

An assessor provides responses to factors. Risk assessors can contribute to factors in the following ways:

-   Qualitative: Losses are in the form of subjective terms such as high, medium, and low. The losses can also be in the form of a numerical score that is converted into a rating.
-   Quantitative: Losses are in a numerical form. They can be incurred from a risk in monetary terms. They contribute to the inherent Annual Loss Expectancy \(ALE\).
-   Both: Losses have both a qualitative risk rating and a quantitative dollar value. These ratings are also called semi-quantitative.

For more information on understanding qualitative, quantitative, and semi-quantitative ratings, see [Types of risk rating methodologies](qual-vs-quant.md)

## Manual factors

In a risk assessment, questions that need human responses from the respondents are called manual factors. In manual factors, the response is subjective and difficult to classify. Some questions require human intelligence and assessment. Therefore, a manual factor is a subjective assessment of a person's view. Examples of manual factors are reputational impact, expected speed of onset, and so on. In manual factors, users can provide the following types of responses:

-   Text: A descriptive answer. For example, feedback. This choice does not contribute toward the risk score calculation​.
-   Choice: User-defined choices to the questions in the assessment. For example, users can select risk ratings from low, medium, or high.
-   Number: A numeric value. For example, the number of open issues.
-   Currency: An amount in the local currency of the user. For example, the financial impact of a certain risk.
-   Percentage: A percentage value for the questions in the assessment. For example, the percentage of employees satisfied with the organization strategies.

## Group factors

When factors are grouped logically, they are called group factors. A group factor's score depends on the responses of the corresponding manual factors​. For example, organizations are affected from financial risks and non-financial risks. You can create some factors for financial risks, and other factors for non-financial risks. You can combine these two sets of factors into a single group factor called Overall Impact. Like manual factors, group factors can contribute either to a numerical risk score that is converted to a qualitative contribution, or to the ALE values as a quantitative contribution.

## Automated factors

Automated factors automatically fetch the latest data, during an assessment, from any of the data sources such as tables or database views. Automated factors help to automate the risk assessment process. They do not rely on manual inputs, and thus reduce subjectivity. For example, a risk assessor wants to perform an assessment for different locations. One of the automated factors is the political condition of a country, and this information is publicly available on a website. Because this data does not reside within ServiceNow, the assessor can use automated factors to fetch the data. Some other examples of automated factors are the following:

-   The number of employees on a project.
-   The revenue of a business unit.
-   The business criticality of a process.

## Scripted automated factors

Automated scripted factors are used to write scripts. The scripts fetch the data from either ServiceNow records or from external sources. Scripted automated factors automatically provide the responses for factors during risk assessment.

The following use cases demonstrate an example of how you can model scripted factors. For example, if you want to use the results from the compliance function to assess the mitigation effectiveness of the controls, there are two ways for assessing the controls:

-   Individual assessment of controls
-   Control environment assessment.

In the individual assessment of controls, each control is separately assessed. To understand control assessment in the context of scripted factors, consider the example of money laundering as a risk. In this example, the control effectiveness is assessed based on the percentage of the failed controls. The values of the failed controls are then transformed into a rating to calculate the control effectiveness of that control. For example, the risk of money laundering has three mitigating controls:

-   Employee training
-   Internal audit on employees
-   Customer due diligence

Assume that you have defined the control effectiveness criteria in the following manner:

|Control Design Effectiveness Failure|Control Effectiveness|
|------------------------------------|---------------------|
|0%-30%|Effective|
|30%-60%|Needs improvement|
|&gt; 60%|Ineffective|

Now, assume that out of the three controls, one control passed and two controls failed. The failure of two controls translates into a 66.67% failure rate. Based on the transformation and based on the previous table, the control effectiveness rating is ineffective. You can use this defined script to automate the response to the factor to assess the risk of money laundering.

As for control environment assessment, you can assess the complete control environment instead of assessing each control individually. To understand control environment assessment, consider the following example. Assume that you want to assess the control environment based on two aspects: design effectiveness and operating effectiveness. To calculate the design effectiveness, you can fetch the related controls that are related to the risk of money laundering. You can then look at the test results to understand how many of the controls had failed. Assume that you have defined the control effectiveness criteria in the following manner:

|Control Design Effectiveness Failure|Control Effectiveness|
|------------------------------------|---------------------|
|0%-30%|Effective|
|30%-60%|Needs improvement|
|&gt; 60%|Ineffective|

Now, assume that two controls failed and one control passed. Thus, the control design effectiveness failure rate is 33.33%. Based on the previous table, this low value of 33.33% means that the control design needs improvement. This response can be automatically scripted in the automated scripted factor because it does not need any human calculation or intervention.

**Parent Topic:**[Advanced Risk Assessment](advanced-risk-assessment.md)

