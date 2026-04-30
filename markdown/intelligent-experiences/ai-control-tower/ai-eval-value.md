---
title: Value tab in the Evaluation dashboard
description: The Value tab in the Evaluation dashboard displays the value, efficiency, and time savings of the virtual agent. The information on this tab gives you a transparent and reliable estimation of the value delivered by the virtual agent, focusing on a quality-adjusted calculation of the time saved for users.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-08-13"
reading_time_minutes: 6
breadcrumb: [Evaluation tab, AI Control Tower Home, AI Control Tower dashboard, Exploring AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Value tab in the Evaluation dashboard

The **Value** tab in the Evaluation dashboard displays the value, efficiency, and time savings of the virtual agent. The information on this tab gives you a transparent and reliable estimation of the value delivered by the virtual agent, focusing on a quality-adjusted calculation of the time saved for users.

The **Value** tab shows a robust and realistic evaluation of the virtual agent's value. By incorporating sampling for scalability, rolling averages for stability, and a quality-weighting framework for business relevance, the resulting metrics gives the automation impact and time saved for the organization.

![Value tab.](../image/ai-eval-value.png)

The following widgets are available:

-   Total conversations: Shows the total volume of conversations initiated with the virtual agent for the selected date range. This metric is a direct indicator of user engagement and virtual agent usage.
-   Estimated total hours: Shows the cumulative, quality-adjusted time saved by users interacting with the virtual agent.
-   Estimated VA efficiency \(%\): Calculated as the ratio of the estimated total hours saved to the total duration of all conversations \(Estimate Time Savings/Total Conversation Time\). The estimate indicates how effectively conversation time is converted into value.
-   Gauges by chat size: The gauges show a breakdown of the estimated total hours saved, segmented by the size of the conversation \(long, medium, and short\).

    Conversations are segmented based on their size to accurately correlate effort with value. The principle is that longer, more complex chats that successfully resolve issues save more time than shorter, simpler ones.

    -   Large-size conversations: Conversations with more than 10 messages from the user.
    -   Medium-size conversations: Conversations with more than 4 but fewer than 10 messages from the user.
    -   Small-size conversations: Conversations with 4 or fewer messages from the user.
    **Note:** To change the definition of small, medium, and large conversations, update the property **sn\_na\_conv\_eval.value\_chat\_classifier**. For more information, see [Components installed with the Evaluation dashboard](../reference/ai-eval-components.md).

    ![Breakdown by conversation chat sizes.](../image/ai-eval-value-05.png)

-   Value calculations: Shows the amount saved based on the numbers of hours saved and the hourly rate.

    ![Value calculations widget.](../image/ai-eval-value-04.png)

-   User acceptance score: The average satisfaction score derived from the conversation evaluator, scaled to 100 for easy interpretation. This score reflects the overall user perception of the virtual agent's quality of assistance.

    **Weekly user acceptance trend**

    ![Weekly user acceptance score.](../image/ai-eval-value-01.png)

    The line chart tracks the User acceptance score over time, providing insight into how user satisfaction is evolving on a weekly basis.

-   Weekly efficiency trends:

    ![Value by conversation size.](../image/ai-eval-value-02.png)

    ![Value by content type.](../image/ai-eval-value-03.png)


The weekly efficiency trend charts display the weekly trend of the Estimated Efficiency \(%\) metric, further broken down by both chat size and the type of content \(Knowledge Base \(KB\) article or Service Catalog item\) used during the conversation.

**Note:** Conversation evaluation scores are tagged as of evaluation date and not the actual conversation date. Hence older or historical chat scores are considered as of the day of evaluation for value calculation and not as of the conversation created date.

## Calculating the estimated total hours

The estimated total hours calculated is the result of a multi-step, daily process designed to adjust raw time based on the quality of the interaction. It’s calculated through the following steps:

1.  Data sampling for quality evaluation.

    To limit number of assists, every conversation isn't evaluated. Instead, a daily sampling process is used.

    -   Sample size: 10% of all conversations are selected for evaluation from the previous day.
    -   Daily cap: The sample is capped at a maximum of 50 conversations daily.
    -   Analytical dataset: To identify stable patterns in virtual agent quality, a rolling 30-day window is used for these evaluated chats, which creates a dataset of approximately 1,500 evaluated conversations \(50 chats/day for 30 days\) for analysis.
2.  Categorizing conversation quality.

    Each of the ~1,500 conversations in the 30-day analytical dataset is assigned a quality score by the conversation evaluator. Based on the score, the conversation is categorized into one of five satisfaction levels:

    |Quality category|User satisfaction score range|
    |----------------|-----------------------------|
    |Extremely satisfied|4.5–5.0|
    |Satisfied|3.5–4.5|
    |Average|2.5–3.5|
    |Unsatisfied|1.5–2.5|
    |Extremely unsatisfied|1.0–1.5|

3.  Projecting quality scores onto the daily conversations.

    There might not be a quality score for all virtual agent conversations, which limits the ability to accurately estimate the time saved by the virtual agent. To solve this issue, the quality distribution from the 30-day analytical dataset is projected onto the daily virtual agent conversations.

    1.  Calculate rolling averages: From the ~1,500 evaluated chats, the percentage distribution of total chat time across the five quality categories for each segment is calculated.

        For example, for all short chats, or for all chats that invoked a KB article. Suppose that the 30-day analysis of short chats shows their total duration was 100 minutes. If 25 of those minutes came from chats rated as extremely satisfied, then the extremely satisfied category for short chats has a 25% time-based score.

    2.  Apply averages to the daily conversations: The daily chats are grouped by their segment \(for example, by chat size\). The rolling average percentages are then applied to the total time of these groups.

        For example, if the daily chats contain 400 short chats with a total duration of 4,000 minutes, the rolling average calculated is used to project that 25% of the time \(1,000 minutes = 4000 minutes \* 25%\) was of extremely satisfied quality. The calculation is repeated for all quality levels and all segments.

4.  Applying quality-adjustment weights.

    To convert raw conversation time into a realistic measure of time saved, a weight is applied to the projected time in each quality category. Time from low-quality interactions contributes little to no savings, while time from high-quality interactions contributes 100% of its duration to savings.

    |Conversation quality category|Weight applied to time|
    |-----------------------------|----------------------|
    |Extremely satisfied|1.0 \(100%\)|
    |Satisfied|0.5 \(50%\)|
    |Average|0.25 \(25%\)|
    |Unsatisfied|0.1 \(1%\)|
    |Extremely unsatisfied|0.0 \(0%\)|

    Example continued, the 1,000 minutes of extremely satisfied time calculated in Step 4 is multiplied by a weight of 1.0, resulting in 1,000 minutes of estimated time saved. If another 500 minutes were projected to be satisfied, they would contribute 500 \* 0.5 = 250 minutes of time saved.

5.  Weekly aggregation:

    The daily Final Daily Time Saved figures are aggregated at a weekly level for display on the dashboard's trend charts.


**Important:** Only the chat time before the first live agent invocation is considered for value calculation. That is, the time the user has spent interacting with the virtual agent. The chat time with the live agent isn’t considered for value calculation.

Conversation evaluations scores are tagged as of evaluation date and not the actual conversation date. Hence older or historical chat scores are considered as of the day of evaluation for value calculation and not as of the conversation created date.

If data isn’t updated on the dashboard, perform the following steps.

Role required: admin

1.  Navigate to **All** &gt; **System Definitions** &gt; **Scheduled Jobs**.
2.  Search for and select the **CE Populate Value Aggregates Chats - Daily** scheduled job.
3.  Set it as **Active**.
4.  Execute the scheduled job.
5.  Navigate to **All** &gt; **Platform Analytics** &gt; **Platform Analytics Administration** &gt; **Data Collector** &gt; **Jobs**.
6.  Search for and select the **“\[Conversation Evaluator\] Evaluation Score Daily Data Collection** scheduled job.
7.  Execute the job.
8.  In the Related Lists section, check the **Job Logs** tab to see if the data was collected successfully.

**Related topics**  


[Evaluation dashboard References](../reference/ai-eval-references.md)

