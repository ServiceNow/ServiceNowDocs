---
title: Quick start tests for Risk Management
description: Validate that Risk Management still works after you make any configuration change, such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Risk Management detailed setup, Configure, Risk Management, Governance, Risk, and Compliance]
---

# Quick start tests for Risk Management

Validate that Risk Management still works after you make any configuration change, such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.

GRC: Risk Management quick start tests require activating the Risk Management plugin \(com.sn\_risk\) and loading demo data.

|Test|Description|Release version|
|----|-----------|---------------|
|GRC: Create Profile|Validate profile creation.|Madrid|
|GRC: Create Risk|Validates risk creation.|Madrid|
|GRC: Create Control|Validates control creation.|New York|
|GRC: Create Control Objective and Generate Controls|Validates control objective creation and associates profiles to generate controls.|New York|
|GRC: Create Issue|Validates issue creation|New York|
|GRC: Accept an Issue|Validates all the states of an issue till it is closed by accepting the issue.|New York|
|GRC: Remediate an Issue|Validates issue cannot be closed be with an open remediation task.|New York|
|GRC: ATF Flow for Indicator \(Manual\):|Create an indicator template with type manual and associate a control objective to it. Execute one of the indicators thus formed. Mark the state of the indicator task created as closed and result as failed. The associated control will become non- compliant and an issue will be generated.|New York|
|GRC: ATF flow for Indicator \(Basic\)|Create an indicator template with type basic and result as failed. Associate a control objective to it and give the supporting data. Execute one of the indicators thus formed. The associated control will become non- compliant and an issue will be generated.|New York|
|GRC: ATF flow for indicator \(Script\)|Create an indicator template with type script and enter a script and set the value of result.passed and result.value. Associate a control objective to it. Execute one of the indicators. The associated control will become non-compliant and an issue will be generated.|New York|

**Parent Topic:**[Risk Management detailed setup](../../../product/grc-risk/concept/setup-risk-management.md)

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)

