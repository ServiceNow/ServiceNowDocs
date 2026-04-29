---
title: Auto-case creation from an email
description: Automatically categorize HR cases submitted by email. Auto-case creation allows for a faster response time and better case resolution for employees.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Auto-case creation from an email

Automatically categorize HR cases submitted by email. Auto-case creation allows for a faster response time and better case resolution for employees.

HR cases can be created via email, phone, or a self-service Service Portal such as the Employee Service Center. By default, an email sent to the general address for HR requests is created as a general inquiry case. An HR agent then has to review and manually recategorize it to the appropriate HR service. With Predictive Intelligence, a predictive model is auto-trained to categorize HR cases submitted by email. The email is routed to the appropriate HR service based on the subject line and body.

**Note:** This feature is available with the HR Professional and HR Enterprise packages when you activate the HR Service Delivery and Predictive Intelligence applications. If you do not want to use this feature navigate to **HR Administration** &gt; **Application Properties** and disable the **Enable HR Case auto categorization** property.

On instances where both Predictive Intelligence and HR Service Delivery are active, the following solution definition and business rule are available to use.

|Solution Definition|Description|
|-------------------|-----------|
|HR Case Categorization|Predicts the **HR service** from the **Short description** and **Description**.|

|Business rule|Table|Description|
|-------------|-----|-----------|
|Predict COE, Service after insert|HR Case \[sn\_hr\_core\_case\]|Generates prediction results for active HR Service Delivery solutions. Runs when a new HR case record submitted by email is inserted.|

By default, the solution definition is configured and the predictive model is auto-trained when the following conditions are met. Auto training happens based on the frequency configuration of solution definition.

-   The Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin is installed.
-   The Predictive Intelligence \(com.glide.platform\_ml\) plugin is installed.
-   There are 10000 records of HR case study matching the filters defined in the solution definition.
-   The **glide.platform\_ml.auto\_training.enabled** system property is set to true.

When any one of the preceding conditions is not met, you must manually configure the solution definition and train the predictive model from the **HR AI configuration** module. If you use domain separation in your instance, you can define the solution definition to use for each domain by creating additional configuration records. See [Configure the HR solution definition and domain](../task/configure-hr-auto-case-categorization.md) for more information.

Once your solution definition is trained, you can test the solution prediction by sending emails to the general email address for HR requests. You can then verify that the corresponding HR cases are automatically categorized to the appropriate HR service. See [Test an HR solution prediction](../task/test-hr-solution-prediction.md) for more information.

