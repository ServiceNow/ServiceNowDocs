---
title: Evaluate a prompt
description: Use the Now Assist Skill Kit evaluation tools to evaluate the effectiveness of your skill prompts.
locale: en-US
release: yokohama
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Using Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Evaluate a prompt

Use the Now Assist Skill Kit evaluation tools to evaluate the effectiveness of your skill prompts.

## Before you begin

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select the skill that you want to evaluate.

3.  Select the **Prompt performance** tab.

4.  Select the **Evaluation runs** tab.

5.  Create a dataset from a table or data collection.

<table id="table_iv4_kcz_ddc"><thead><tr><th>

Method

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Create a dataset from a table

</td><td>

1.  Give the dataset a name and description.
2.  Select **Table**.
3.  Find the table that you want to use.
4.  Select the maximum number of records that you want to use.
5.  Add conditions.
6.  Select **Generate Preview**.
7.  Select the mappings.
8.  Select **Create**.


</td></tr><tr><td>

Create a dataset from a data collection

</td><td>

1.  Give the dataset a name and description.
2.  Select Data Collection.
3.  Select a data collection that you created in Now Assist Data Kit.
4.  Select **Generate Preview**.
5.  Select the mappings.
6.  Select **Create**.


</td></tr></tbody>
</table>6.  Select the add icon ![add icon](../image/icon-nask-add.png) for **Evaluation Runs**.

7.  Give the evaluation run a name and description.

8.  Select one or more prompts that you want to evaluate.

9.  Select **Save &amp; Next**.

10. Select a dataset.

11. Select **Save &amp; Next**.

12. Expand the **Quality** tab.

13. Select the metrics that you want to evaluate.

    |Evaluation method|Metric|Description|
    |-----------------|------|-----------|
    |Human|Human Feedback|Human evaluation is the default option available for all prompt executions that generate a response. You can rate the response with a thumbs up or thumbs down, based on your satisfaction. You also have the option to provide more detailed feedback to explain your evaluation choice.|
    |Automated|Correctness|The correctness metric assesses the generated response's accuracy, completeness, pertinence, and writing quality relative to the given instruction. This metric helps to check that the text accurately reflects the instruction, covers all important points, remains relevant, and is well written.|
    |Automated|Correctness with Golden Response|The correctness with golden response metric uses a predefined reference to assess the generated response's accuracy, completeness, pertinence, and writing quality relative to the given instruction. This metric helps to check that the text accurately reflects the instruction, covers all important points, remains relevant, and is well written. You should use this metric whenever possible.|
    |Automated|Faithfulness|The faithfulness metric assesses whether a generated response accurately reflects the information and context provided in the given instruction. This metric helps to check that the text contains no hallucinations, fabricated facts, or unsupported conclusions, maintaining alignment with the source material.|

14. Select **Save &amp; Next**.

15. Review the evaluation choices that you made.

16. Select **Save &amp; Evaluate**.

17. Give a human evaluation.

    1.  Select **Human evaluation**.

    2.  Select a record to use in the evaluation.

    3.  Expand the prompt and read the result.

    4.  Select the thumbs up or thumbs down icon ![human evaluation thumbs up or thumbs down icon](../image/icon-nask-thumbs.png) to give your evaluation.

    5.  Add more information and select **Submit**.


**Parent Topic:**[Using Now Assist Skill Kit](../concept/using-now-assist-skill-kit.md)

**Related topics**  


[Create a skill](create-new-skill.md)

[Create a prompt](create-prompt-template.md)

[Use prompt assistance](use-prompt-assistance.md)

[Test a prompt](test-prompt-template.md)

[Finalize and publish a skill](publish-skill.md)

[Activate a skill](activate-skill.md)

[Call a custom skill from a script](call-custom-skill-from-script.md)

