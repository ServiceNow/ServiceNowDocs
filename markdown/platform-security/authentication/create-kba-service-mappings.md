---
title: Assign KBA questions to your AI voice agent service
description: Specify the questions that should be used for user identification and authentication with a specific voice agent. 
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-11-18"
reading_time_minutes: 1
breadcrumb: [Configure KBA, Knowledge-based authentication, Configure authentication factors, Authentication factors, Authentication, Access Management]
---

# Assign KBA questions to your AI voice agent service

Specify the questions that should be used for user identification and authentication with a specific voice agent. 

## Before you begin

Role required: auth\_factors\_admin

## Procedure

1.  Navigate to **All** &gt; **Authentication Factors** &gt; **Knowledge Based Factor** &gt; **Question Service Mappings**.

2.  Select **New** on the Knowledge Based Question Service Mappings page.

3.  Specify the following fields on the form:

<table id="table_gtp_xb1_jhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Profile Table

</td><td>

Select the table for your service.

</td></tr><tr><td>

Application

</td><td>

Global application scope is selected by default.

</td></tr><tr><td>

Service Profile

</td><td>

Select the service profile. Example: Choosing a voice agent: **Now Assist Voice Deployment - 22**.

</td></tr><tr><td>

Type

</td><td>

Select the type for which you would use the service mapping. Options:-   Authentication
-   Identification
**Note:** The **Type** field is the only differentiating factor between **Identification** and **Authentication** configuration using KBA.

</td></tr><tr><td>

Answer Column

</td><td>

Select the question that you want to use for the service verification.

</td></tr><tr><td>

Active

</td><td>

Select to set the configuration active.

</td></tr></tbody>
</table>    ![Knowledge Based Question Service Mapping](../images/configure-kba-question-answer-service.png "Knowledge Based Question Service Mapping")

4.  Select **Submit**.


## Result

You’re redirected to the Knowledge Based Question Service Mappings list view. Verify if your mapping is successfully added.

![Knowledge Based Question Service Mapping - Result](../images/configure-kba-question-answer-service-result.png "Knowledge Based Question Service Mappings - list")

