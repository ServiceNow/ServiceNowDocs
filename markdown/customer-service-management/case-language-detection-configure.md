---
title: Configure language detection
description: Activate the required plugins and flows to use the language detection feature.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Task Intelligence for Customer Service, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Configure language detection

Activate the required plugins and flows to use the language detection feature.

For more information about the languages supported by language detection, see this topic: [Languages supported by Task Intelligence](https://www.servicenow.com/docs/access?context=languages-supported-by-language-detection&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

Follow the steps in the table below to configure the language detection feature for cases.

<table id="table_ih2_hfc_5rb"><thead><tr><th>

Step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ensure that your instance is set up for Predictive Intelligence \(PI\).

</td><td>

Predictive Intelligence is a ServiceNow platform feature that provides a layer of artificial intelligence, which serves as a framework for machine learning models. For more information, see:

-   [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)
-   [Machine learning solutions for Customer Service Management](machine-learning-csm.md)

</td></tr><tr><td>

Activate the Task Intelligence for Customer Service application \(com.snc.csm\_ml\_task\).

</td><td>

The Task Intelligence for Customer Service application enables customers to leverage machine learning algorithms in Customer Service Management. The sentiment analysis feature is included with this application.

 This application automatically activates the following plugins:

-   Predictive Intelligence for Customer Service Management \(com.snc.csm\_ml\)
-   Customer Service \(com.sn\_customerservice\)
-   Skills Management \(com.snc.skills\_management\)
-   Dynamic Translation \(com.glide.dynamic\_translation\)
-   ServiceNow Language Detection Service Spoke \(com.glide.language\_detection\_spoke\)
-   Predictive Intelligence - Task Intelligence \(com.glide.platform\_ml\_task\)
-   Admin Center for Task Intelligence \(com.sn\_ti\_admin\)

</td></tr><tr><td>

Activate the ServiceNow translator.

</td><td>

To activate the translator:1.  Navigate to **Dynamic Translation** &gt; **Translator Configurations**.
2.  Select ServiceNow in the list of configurations.
3.  Enable the **Active** check box and click **Update**.

</td></tr></tbody>
</table>**Related topics**  


[Language detection](case-language-detection.md)

