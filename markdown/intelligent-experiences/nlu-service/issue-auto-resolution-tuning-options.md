---
title: Issue Auto Resolution tuning options
description: When you are tuning your Issue Auto Resolution model in NLU Workbench, you can adjust the output for several goals: precision, automation, or a balance of the two. Compare how your choice of tuning options affect match rate and coverage, before committing.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Issue Auto Resolution Tuning in NLU, NLU Workbench - Advanced Features, Natural Language Understanding, Enable AI experiences]
---

# Issue Auto Resolution tuning options

When you are tuning your Issue Auto Resolution model in NLU Workbench, you can adjust the output for several goals: precision, automation, or a balance of the two. Compare how your choice of tuning options affect match rate and coverage, before committing.

## Summary usage

By default, Issue Auto Resolution tuning in NLU Workbench optimizes for precision. Depending on your business requirements, you can also tune the model for other objectives. In the **Analyze** step of Issue Auto Resolution tuning, the tuning goals list enables you to adjust for **Precision**, **Automation**, or **Balance**. As you select one of these options, the projected Match rate and IAR coverage percentages change accordingly, so you can compare possible outcomes.

To access the **Analyze** step of IAR tuning, use the nlu\_admin role and navigate as follows.

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.
2.  Select the Issue Auto Resolution tab, then select the model name. The tuning experience opens to step 1 \(Feedback\) initially.
3.  Provide feedback, then select the **Analyze** button. Step 2 \(Analyze\) opens.
4.  In the section **Here are your tuning options and projected results**, using the list **You can tune for precision, automation, or balance**, select options to see projected scenarios. You can also select the link **Learn about tuning goals** to open the following window.

![In the Analyze step of IAR Tuning in NLU Workbench, the window What do you want to tune for? is open.](../images/issue-auto-resolution-tuning-options020V.png)

## Precision

When tuned for precision, the IAR model makes predictions only when its confidence is relatively high. This results in lower error rates, but also in fewer incidents resolved.

Precision is the recommended tuning option for the IAR ITSM model, so this option is selected by default.

## Automation

When tuned for automation, the IAR model makes predictions at a lower confidence threshold. This results in more predictions, so more incidents are resolved. However, higher error rates are possible.

## Balance

When tuned for balance, the IAR model attempts to strike a balance between precision and automation.

## Match rate

The match rate is defined as the number of Incidents where the intent was predicted correctly, divided by the number of predictions for that intent. This ratio is averaged across all intents except for **NO\_INTENT**.

## IAR Coverage

Coverage is defined as the percentage of Incidents that would be resolved because the model was able to make predictions above its confidence threshold. The predictions may contain some errors.

## Using tuning options

Select several different tuning options to compare projected results. Depending on the option you select, the system presents scenarios for projected Match rates and IAR coverage rates. Also the system displays how much these rates change according to your selection.

Review further information in the **Here's a detailed breakdown** section of Analyze. Here you can drill down into results that are specific for each intent in the model.

Note that the intents are grouped into mapped and unmapped intents, depending on whether they have been mapped to Virtual Agent topics. After providing feedback in IAR Tuning, you may wish to activate some intent-to-topic mappings. To do so, expand **See unmapped intents**, then select the **Map more intents** button. This opens the IAR Admin Console.

When you have decided the optimum tuning option for your requirements, select the **Save choice** button in the **Learn about tuning goals** window. Then, select the **Tune and publish model** button to advance to the next step.

