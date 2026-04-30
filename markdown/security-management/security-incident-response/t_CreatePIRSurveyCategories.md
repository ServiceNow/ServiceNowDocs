---
title: Create post incident review questionnaire categories
description: You can use the questionnaire categories that come with the base system or create your own categories.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Perform a questionnaire-based post incident review, Manage post incident activities, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create post incident review questionnaire categories

You can use the questionnaire categories that come with the base system or create your own categories.

## Before you begin

Role required: sn.si\_admin

## About this task

To create a new category of questions:

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Post Incident Review**.

2.  Click **Review Questions**.

    A list of categories is displayed, along with their order and filters that define under what conditions the questions are asked \(for example, only when the security incident category is Criminal activity\). Each category is a section in the post incident review questionnaire and the questions in each category are included only when the security incident matches the Condition filter. For example, for a category of questions applying only to Linux servers, you would set up a filter that selected security incidents where the affected resource type was Linux Server. In that category, you would then create all questions needed when a security incident was on a Linux Server. You use one of the categories supplied in the base system or create a new category. This procedure assumes that you want to create a new category before defining questions.

3.  Click **New** in the list of categories.

4.  Fill in the fields on the form, as appropriate.

<table id="table_vks_thr_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the category that appears on the security incident questionnaire.

</td></tr><tr><td>

Type

</td><td>

Post Incident Review is the default.

</td></tr><tr><td>

Create Stakeholders

</td><td>

Unused by Security Incident Response.

</td></tr><tr><td>

Table

</td><td>

This field is auto-assigned once the form is submitted.

</td></tr><tr><td>

Filter

</td><td>

Enter the condition that determines when questions in this category are used. If a security incident record matches this filter, the questions is included in a post incident review for that security incident. Filters can use any data on the record, or on other records linked to this record. For example, the department of the requesting user’s manager.

</td></tr><tr><td>

Application

</td><td>

Scope application for the incident.

</td></tr><tr><td>

Weight

</td><td>

Numeric value that represents the importance of this metric relative to other metrics in the same category. By default, the weight is 10.

</td></tr><tr><td>

Total Metrics

</td><td>

Number of metrics used by the category.

</td></tr><tr><td>

Description

</td><td>

Description of the questionnaire.

</td></tr></tbody>
</table>5.  Click **Submit** to save the category.


