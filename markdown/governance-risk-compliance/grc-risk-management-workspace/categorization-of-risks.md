---
title: Categorizing risks with the Governance, Risk, and Compliance: Predictive Intelligence plugin
description: By using the Governance, Risk, and Compliance: Predictive Intelligence plugin, you can predict the risk statements for your orphan risks \(the risks that don't have risk statements\) on the risk records for your organization. You can then identify the correct risk statement for the risks and then aggregate them into manageable categories.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Categorizing risks with the Governance, Risk, and Compliance: Predictive Intelligence plugin

By using the Governance, Risk, and Compliance: Predictive Intelligence plugin, you can predict the risk statements for your orphan risks \(the risks that don't have risk statements\) on the risk records for your organization. You can then identify the correct risk statement for the risks and then aggregate them into manageable categories.

Usually, the first line of employees or the risk champions within an organization identify the risks for the business.

**Note:** A risk champion is an executive who is in charge of identifying and reporting risks within an organization.

As the risk champions identify these risks, they manually associate the risks with the correct risk statement. The organization's senior management gets visibility into the organization's risk profile because these operational risks are aggregated into the enterprise risks.

However, your risk champions must manually search the complete risk library to identify the correct risk statement for the identified risks. This activity is time-consuming and is an inefficient use of resources. When the risk champions search for risk statements manually, they tend to select whatever is the earliest match rather than search for the entire library, which results in the incorrect categorization of risks with risk statements.

## Predicting risk statements on risk records

The Governance, Risk, and Compliance: Predictive Intelligence plugin uses artificial intelligence \(AI\) and machine learning \(ML\) to predict the related risk statements on the risk records. The Predictive Intelligence plugin uses the similarity capability in the Predictive Intelligence engine to compare the risk name and description with the risk statements. With this plugin, your organization can reduce the effort that is required to search and identify the risk statements to associate with the identified risks. Your organization also gets higher accuracy in risk aggregation and reporting and visibility into the organization's risk profile.

The following example shows the recommended risk statements on the risk record. ![Recommended risk statement.](../image/risk-statement-recommendation.png)

**Note:** A risk user \(sn\_risk.user\) can only see the risk statement recommendations when the risk statement isn’t defined on the risk record. Based on the recommendations, a risk user can associate the risk with a related risk statement.

## Benefits of risk categorization with risk statements

By categorizing your organization's risks with the risk statement, the following benefits are provided to different users:

-   Risk owners: Identify the correct risk statement for the orphan risks to group risks into manageable categories.
-   Risk managers: Reduce the number of orphan risks that were created by the first line of employees or risk champions. The risk managers get visibility into the organization's risk profile and can analyze the impact due to the similar type of risks.
-   Risk administrator: Configure the solution definition to predict the risk statements that are based on the organizational needs.

## Setting up the feature

A risk administrator with the ml\_admin role can set up the risk categorization in the Risk Workspace application. Before your organization can use this feature, the risk administrator must install and activate the following applications and plugins:

-   Risk Management
-   Risk Workspace
-   Predictive Intelligence
-   Recommended Actions - Advanced

A risk administrator can train a default similarity solution for the risks in your organization by using the Predictive Intelligence plugin.

**Note:** A similarity solution is a machine-learning solution to collect and compare your existing records to new similar records.

For more information, see [Create and train a similarity solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/create-similarity-solution.md).

**Note:** You must have at least 1000 risk records for the similarity algorithm to work.

A risk administrator with the ml\_admin role can review the default similarity solution definition for risk and modify it based on your organizational needs.

**Parent Topic:**[Using the Risk Workspace](using-risk-workspace.md)

