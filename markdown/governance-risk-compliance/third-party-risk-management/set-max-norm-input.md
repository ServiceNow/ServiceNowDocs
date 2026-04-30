---
title: Normalize the scores for metrics
description: You can use the Maximum normalization input setting to use normalized values to calculate assessment scores for questions \(metrics\).
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Classic assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Normalize the scores for metrics

You can use the **Maximum normalization input** setting to use normalized values to calculate assessment scores for questions \(metrics\).

## When Maximum normalization input applies

The **Maximum normalization input** field appears only when:

-   The data type of the question is either **Choice** or **Multiple Selection**.
-   The **Scored** check box is not selected.

To use normalized scoring, the value assigned to each metric definition \(possible answer\) for each metric \(question\) must be unique.

In the following examples, the **Scale definition** is **High** \(larger numerical values are good\).

## Choice type questions

-   **When Maximum normalization input is not selected**

    ![Option to select maximum normalization input.](../../grc-vendor-risk/image/tprm-q-choice-no-max-norm-input.png)

    Formula: \(\[Value of the response\] – \[Lowest value\] \) / \( \[Highest value\] – \[Lowest value\]\) \* 100.

    In this example, the question allows a choice among answers with values of `1`, `2`, and `4`.

    |Response|Calculation|Score|
    |--------|-----------|-----|
    |Dog|\[\(1-1\)/\(4-1\)\] \* 100|0|
    |Cat|\[\(2-1\)/\(4-1\)\] \* 100|33|
    |Goldfish|\[\(4-1\)/\(4-1\)\] \* 100|100|

-   **When Maximum normalization input is selected**

    ![Option to select maximum normalization input.](../../grc-vendor-risk/image/tprm-q-choice-max-norm-input.png)

    Formula: `([Value of the response]/ [Highest value]) * 100`.

    In this example, the question allows a choice among answers with values of `1`, `2`, and `4` and normalization input values of `3`, `5`, and `9` respectively.

    |Response|Calculation|Score|
    |--------|-----------|-----|
    |Dog|\(1 / 4\) \* 100|25|
    |Cat|\(2 / 4\) \* 100|50|
    |Goldfish|\(4 / 4\) \* 100|100|


## Multiple selection type questions

-   **When Maximum normalization input is not selected**

    ![Option to select maximum normalization input.](../../grc-vendor-risk/image/tprm-q-multi-sel-no-max-norm-input.png)

    Formula: `([Sum of the normalization input values for the selected responses] / [Sum of all the normalization input values]) * 100`.

    In this example, the question allows for multiple selections among answers with values of `1`, `2`, and `4` and normalization input values of `3`, `5`, and `9` respectively.

    |Response|Calculation|Score|
    |--------|-----------|-----|
    |Dog and Cat|\(\[3+5\] / 17\) \* 100|47|
    |Cat|\(5 / 17\) \* 100|29|
    |Cat and Goldfish|\(\[5+9\] / 17\) \* 100|82|
    |Goldfish|\(9 / 17\) \* 100|53|

-   **When Maximum normalization input is selected**

    ![Option to select maximum normalization input.](../../grc-vendor-risk/image/tprm-q-multi-sel-max-norm-input.png)

    -   The system uses the value `0` for the response that has the lowest value. In this example, the **Dog** response is assigned the value `0`.
    -   Formula for each selection: `([Highest normalization input value for the selected responses] / [Maximum of the normalization input values]) * 100`.
    -   The score for the metric \(question\) is the maximum calculated score among all responses.
    In this example, the user selects **Dog** and **Cat**.

    -   The score for the **Dog** response is `(0 / 9) * 100 = 0`.
    -   The score for the **Cat** response is `(5 / 9) * 100 = 55.5`.
    -   The score for the overall metric is `55.5`.
    Formula: `(Highest of the normalization input values for the selected responses / Highest of all the normalization input values) * 100`.

    In this example, the question allows for multiple selections among answers with values of `1`, `2`, and `4` and normalization input values of `3`, `5`, and `9` respectively.

    |Response|Calculation|Score|
    |--------|-----------|-----|
    |Dog and Cat|\(5 / 9\) \* 100|56|
    |Cat|\(5 / 9\) \* 100|56|
    |Cat and Goldfish|\(9 / 9\) \* 100|100|
    |Goldfish|\(9 / 9\) \* 100|100|


