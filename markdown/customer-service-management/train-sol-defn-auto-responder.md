---
title: Train the similarity solution for finding Auto-Responder notification content
description: Update and train a similarity solution definition to enable the Auto-Responder feature to suggest content by comparing the short description of a customer service case with those of existing knowledge articles.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure Auto-Responder notifications, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Train the similarity solution for finding Auto-Responder notification content

Update and train a similarity solution definition to enable the Auto-Responder feature to suggest content by comparing the short description of a customer service case with those of existing knowledge articles.

## Before you begin

Role required: admin

Activate the Predictive Intelligence for Customer Service Management plugin \(com.snc.csm\_ml\). For more information, see Activate a plugin and [Predictive Intelligence for CSM solution definitions](../concept/predictive-intelligence-for-csm.md).

## About this task

A similarity solution definition collects and compares your existing records to new similar records. The Similar Knowledge Articles All similarity solution selects knowledge articles for customer service cases from the predefined knowledge bases in the consumer service portal and customer service portal. To select knowledge articles from any custom knowledge base in a portal or from a knowledge base in any custom portal, you must modify this similarity solution.

For a similarity solution to work correctly, the Knowledge \[kb\_knowledge\] table in the Knowledge View \[sn\_customerservice\_knowledge\_view\] database view must have at least the required number of records set in the configuration of your ServiceNow instance. The default minimum number required is 10,000.

If the Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) is activated, the tables for knowledge article templates \(such as FAQ, How to, What Is, KCS Article\) are also added to the Knowledge View \[sn\_customerservice\_knowledge\_view\] database view. For a similarity solution to show results from each template type, each of the tables for the template type must have at least the required number of records. If a table doesn’t have the required number of records, you might not see the results from that table. For more information, see Database View support for Predictive Intelligence.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solution Definitions**.

2.  In the Similarity Definitions list, search for and select the Similar Knowledge Articles All solution definition \(ml\_sn\_sn\_customerservice\_global\_similar\_knowledge\_view\_articles\).

3.  On the Similarity Definition form, verify the default field values for knowledge articles.

    **Note:** If the application scope isn't set to Customer Service application, you cannot edit the form and a warning message appears. To make the form editable, click the word **here** at the end of the message.

<table id="table_bxj_sbx_4jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique name for your similarity solution.

</td></tr><tr><td>

Word Corpus

</td><td>

Defines which knowledge articles and cases are selected.By default, the **All Articles and Cases** word corpus is available to search for knowledge articles similar to a customer service case short description.

**Note:** Modify the word corpus to use the knowledge base defined for your portal. If you have defined custom tables for knowledge articles and article templates, you must include their fields in the word corpus content. For more information about the word corpus and word corpus content, see Create a word corpus.

</td></tr><tr><td>

Table

</td><td>

Table or database view that contains the knowledge article records. Set the value to the Knowledge View \[sn\_customerservice\_knowledge\_view\] database view unless you use a different table or database view for storing knowledge articles. This database view joins the Knowledge \[kb\_knowledge\], What Is \[kb\_template\_what\_is\], How To \[kb\_template\_how\_to\], FAQ \[kb\_template\_faq\], and KCS Article \[kb\_template\_kcs\] tables for viewing all fields in a knowledge article.After you assign a table value, the number of records that match the filter conditions is displayed as a link.

 **Note:** The What Is \[kb\_template\_what\_is\], How To \[kb\_template\_how\_to\], FAQ \[kb\_template\_faq\], and KCS Article \[kb\_template\_kcs\] tables are available only if the Knowledge Management Advanced plugin is activated. For more information, see Activate the Knowledge Management Advanced plugin.

</td></tr><tr><td>

Fields

</td><td>

Fields from the Knowledge View \[sn\_customerservice\_knowledge\_view\] database view selected for similarity comparison with the case short description. The fields must be the same as the fields you define for the Word corpus content.

</td></tr><tr><td>

Filter

</td><td>

Filter conditions applied on the database view to filter knowledge article records for Auto-Responder recommendations.

 Click **Add Filter Condition** to apply conditions to the Field records you're using as a base to retrieve your similarity results. For example, for the customer service portal, you would set a **\[Workflow\] \[is\] \[Published\] AND \[Knowledge base\] is \[Customer Service\]** filter condition.

 For a custom portal, you select the knowledge base of the custom portal in the **\[Knowledge base\]** condition.

</td></tr><tr><td>

Test Table

</td><td>

Table that contains the case records that you want to compare with knowledge article records. Set the value to the Case \[sn\_customerservice\_case\] table unless you use a different table for storing case records.

</td></tr><tr><td>

Test Fields

</td><td>

Fields from the case selected for similarity matching with knowledge article fields. By default, the short description field of a customer service case is used for the similarity match with knowledge article fields.

</td></tr><tr><td>

Processing Language

</td><td id="processing">

Dominant language of the dataset you're training on the solution definition. By default, English processing is applied to all datasets. For example, if you select Italian, the system processes the data in both English and Italian.**Note:** The term "processing" indicates some of the language-specific steps used as part of training a solution. These steps might include tokenizing words, removing stop words, and stemming.

</td></tr><tr><td>

Stopwords

</td><td id="stopwords">

Common terms in the processing language that are excluded from the search, for example, prepositions.When you select your processing language, the system automatically adds a Stopwords list that uses the same language. For example, if your processing language is Italian, the **Default Italian Stopwords** list appears. The **Default English Stopwords** list appears by default.

</td></tr><tr><td>

Training Frequency

</td><td>

Frequency with which the model for the similarity solution definition must be retrained.

</td></tr><tr><td>

Update Frequency

</td><td>

Frequency with which to include new records in the model for the similarity solution definition.

</td></tr></tbody>
</table>    For more information, see Create and train a similarity solution.

4.  In the Training Request Schedule related list, update the schedule for training the Similar Knowledge Articles All solution definition.

    By default, the training request schedule is **Periodically** and runs after every 30 days.

5.  Click **Update &amp; Retrain**.

6.  Open the Similar Knowledge Articles All solution definition \(ml\_sn\_sn\_customerservice\_global\_similar\_knowledge\_view\_articles\) and in the ML Solutions related list, view the training solution progress in the **Progress** column.

    When **Progress** is 100%, in the ML Solutions related list, you can include more useful content in the Auto-Responder notification by reviewing the similarity examples based on the similarity score and updating the similarity score threshold value.

7.  Update the similarity score threshold.

    1.  In the **Active** column, click the link for the solution.

    2.  Review the similarity examples by clicking the **Similarity Examples** related link on the ML Solution form.

        For more information, see Review solution similarity examples.

    3.  In the Solution Statistics related list on the ML Solution form, enter the required value in the **Similarity Score Threshold** field, right-click the ML Solution form, and then click **Save**.

        For more information, see Update your similarity score threshold.


## Result

When the solution is complete, the knowledge articles similar to the fields selected for a customer service case are sent as Auto-Responder recommendations.

**Related topics**  


[bundle-platcap.knowledge-article-templates]

