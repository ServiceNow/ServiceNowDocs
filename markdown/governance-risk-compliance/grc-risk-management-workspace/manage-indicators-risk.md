---
title: Risk indicators, control indicators, and indicator templates
description: Indicators are an important tool used to manage your organization's risks. Indicators collect data to monitor controls and risks, and to collect audit evidence. Indicators monitor a single control or risk. They are used to enhance and facilitate the monitoring, mitigation, and reporting of risks.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Risk Management, Governance, Risk, and Compliance]
---

# Risk indicators, control indicators, and indicator templates

Indicators are an important tool used to manage your organization's risks. Indicators collect data to monitor controls and risks, and to collect audit evidence. Indicators monitor a single control or risk. They are used to enhance and facilitate the monitoring, mitigation, and reporting of risks.

## Indicators

Indicators are useful when you want to know if your organization is compliant before you do an audit. If certain controls are non-compliant, indicators help you identify them and enable you to correct them. Continuous monitoring involves activities related to identifying and creating key risk and control indicators. Indicators are of the following types:

-   Manual: Manual indicators are used for data that cannot be retrieved from a ServiceNow instance because it comes from an external system, such as customer data from a third-party sales system.
-   Basic: Basic indicators are automated indicators based on an indicator source. The indicator source specifies a table and a frequency at which the scores from this table are saved.
-   Scripted: Scripted indicators use a custom script to collect the data.

The **GRC indicator nightly run** job executes the indicators. When an indicator is run, you have the option to collect supporting data. Supporting data refers to the evidence that is collected when an indicator is run. Supporting data or information can be collected for the indicators through automatic data collection or manual tasks.

Indicators yield results when the indicator tasks are closed. Those results are then used to create issues for controls, update risk scores, and provide supporting information for audit activities and control testing. Starting with version 10.1, the system displays the actual historical data for the supporting data records from the indicator results or indicator tasks. For more information on how to create the various types of indicators, see:

-   [Create and run a manual risk indicator in the Risk Workspace](../../grc-workspace-risk/task/create-a-manual-indicator-risk-ws.md)
-   [Create and run a basic risk indicator in the Risk Workspace](../../grc-workspace-risk/task/create-a-basic-risk-indicator-ws.md)
-   [Create and run a scripted risk indicator in the Risk Workspace](../../grc-workspace-risk/task/create-a-scripted-indicator.md)

## Indicator templates

Indicator templates enable you to create multiple indicators for similar controls or risks. You can either use an indicator template to create indicators or you can create independent indicators. Even if you use an indicator template to create an indicator, you can modify or override the details of the indicators.

