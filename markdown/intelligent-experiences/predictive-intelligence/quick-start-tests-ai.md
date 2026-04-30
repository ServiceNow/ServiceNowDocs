---
title: Quick start tests for Predictive Intelligence
description: Validate that Predictive Intelligence still works after you make any configuration change such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: zurich
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Quick start tests for Predictive Intelligence

Validate that Predictive Intelligence still works after you make any configuration change such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.

Predictive Intelligence quick start tests require activating the Predictive Intelligence \[com.glide.platform\_ml\] plugin. In order to execute critical upgrade tests on existing machine learning solutions, you need to create a basic authorization profile named ml\_atfin the Basic Auth Configurations table \(sys\_auth\_profile\_basic.list\). To run the tests successfully, the user attached to the ml\_atf authorization profile must have the ml\_admin role.

|Test|Description|
|----|-----------|
|PI: Presence of ML model artifacts persisted in glide|Verify all the trained ML model artifacts are persisted in glide \(sys\_attachments table\) after model training/instance cloning so that ML prediction calls are successful.|
|PI: Valid setup of ML user \(sharedservice.worker\) in glide|Validate if the ML user in glide \(sharedservice.worker\) is active and not logged out so that model training is successful.|
|PI: Glide upgrade test for Classification solution|Validate that the classification model prediction on existing active models is producing the same class membership and confidence value results after a glide upgrade.|
|PI: Glide upgrade test for Similarity solution|Validate that the similarity model prediction API calls on active models are successful after a glide upgrade.|

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

