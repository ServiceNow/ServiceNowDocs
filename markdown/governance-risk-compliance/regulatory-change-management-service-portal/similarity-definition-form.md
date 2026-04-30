---
title: Similarity Definition Form
description: Use the Similarity Definition Form form in Compliance Workspace to create a similarity definition for regulatory compliance mapping.
locale: en-US
release: zurich
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Train and use the similarity solution to recommend citations on regulatory alerts, Regulatory alerts, Regulatory Change Management Core UI, Use, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Similarity Definition Form

Use the Similarity Definition Form form in Compliance Workspace to create a similarity definition for regulatory compliance mapping.

## Similarity Definition form

For a description of the field values, see the following table.

<table id="table_o1g_bfj_3fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique name for the similarity solution.

</td></tr><tr><td>

Name

</td><td>

Name of the similarity solution. This field is automatically set to the system-assigned name that is the most similar to your value for the **Label** field.

</td></tr><tr><td>

Word Corpus

</td><td>

Existing word corpus that is relevant to your solution. For this use case, select the **Word Corpus for Issue Assignment** word corpus.**Note:** For word corpora in similarity solutions, the number of records according to table is limited to 300,000.

</td></tr><tr><td>

Table

</td><td>

Table that contains the records that you want to train against and to predict for. When you assign a table value, a link appears in the form. The link shows the number of records that match your current conditions. For this use case, the field is automatically set to the \[`sn_compliance_citation`\] table. Don’t modify this field for this solution definition.

</td></tr><tr><td>

Fields

</td><td>

Field types that are likely to help in recommending the citations. You can select the columns from the table in the **Table** field so that their data helps in predicting the citations more accurately. In this use case, the **Name**, the **Document Name**, **Document Description**, and **Description** fields are selected. These fields are the field types that contain the citation records that you want to recommend.**Note:** You can modify the fields selected here if there are other non-empty important fields on the issue record in your database, such that these fields can help in finding out similar citations for mapping to the regulatory alerts.

</td></tr><tr><td>

Test Table

</td><td>

Table that contains the citations that you want to predict for. For this use case, the field is automatically set to the Issue \[`sn_grc_reg_change_regulatory_feed`\] table.**Note:** The number of records which the Similarity window can retrieve is limited to 10. This field must not be modified for this solution definition.

</td></tr><tr><td>

Test Fields

</td><td>

Fields which are used as input during prediction. In this use case, select **Title** and **Description**.**Note:** You can modify the fields selected here if there are other non-empty important fields on the issue record in your database, such that these fields can help in finding out similar issues for predicting the issue owners.

</td></tr><tr><td>

Filter

</td><td>

Leave this field empty.

</td></tr><tr><td>

Processing Language

</td><td>

Dominant language of the dataset that you are training on the solution definition. If the dataset language is English, choose **English**. By default, English processing is applied to all datasets. For example, if you select **English**, the system processes the data in both English and Italian.

**Note:** The term processing indicates some of the language-specific steps that are used as part of training a solution. These steps include tokenizing words, removing stop words, and stemming.

</td></tr><tr><td>

Stopwords

</td><td>

List of stopwords. When you select your processing language, the system automatically adds a Stopwords list that uses the same language. For example, if your processing language is English, the **Default English Stopwords** option appears. The Default English Stopwords list also appears in your selection. You can add your own custom list of stopwords.

</td></tr><tr><td>

Training Frequency

</td><td>

Frequency of training. The retraining option can range is 180 days.

</td></tr><tr><td>

Update Frequency

</td><td>

Frequency of how often you want to refresh the data that you use to retrieve your similarity results. For example, new citations typically occur frequently throughout the day. If you have new citations, you may want to select an update frequency of **Every 15 minutes**. This frequency can increase the likelihood that new citations are included in the refresh.

</td></tr></tbody>
</table>**Parent Topic:**[Train and use the similarity solution to recommend citations on regulatory alerts](../task/retrain-ml-reg-compliance-mapping.md)

