---
title: ServiceNow AI Creator skills
description: The ServiceNow AI Creator skills dashboard provides insight into how your organization uses AI-powered creator skills—automated code generation, documentation, and testing capabilities—to boost developer productivity. Monitor skill satisfaction, usage patterns, and outcomes to optimize adoption and identify high-performing skills across your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/measure-snow-ai-creator-skills.html
release: zurich
topic_type: concept
last_updated: "2026-08-03"
reading_time_minutes: 3
breadcrumb: [ServiceNow AI dashboard, Measure AI impact and value, Measure AI impact, AI Control Tower, Enable AI experiences]
---

# ServiceNow AI Creator skills

The ServiceNow AI Creator skills dashboard provides insight into how your organization uses AI-powered creator skills—automated code generation, documentation, and testing capabilities—to boost developer productivity. Monitor skill satisfaction, usage patterns, and outcomes to optimize adoption and identify high-performing skills across your instance.

## Creator skills overview

Creator skills are AI-powered agents within ServiceNow that assist users by automating repetitive development tasks. These skills use large language models and ServiceNow specific training to generate code, compose unit tests, write API documentation, and perform other knowledge-intensive tasks. By integrating creator skills into your workflow, your team can accelerate development velocity, reduce manual effort, and maintain consistency across projects.

Creator skills operate within generative AI and are governed by ServiceNow's AI governance and control framework. Each suggestion is tracked, and users can accept, reject, cancel, or ignore recommendations. This feedback loop helps improve skill performance and informs adoption metrics.

To view the ServiceNow AI Creator skills dashboard on AI Control Tower, navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Insights** &gt; **ServiceNow AI** &gt; **Creator skills**.\[Omitted image "aict-snow-ai-creator-skills.png"\] Alt text: The ServiceNow AI Creator skills dashboard with different widgets displaying the insights.

## Skill Satisfaction

Skill satisfaction measures the overall approval rate of creator skill suggestions based on user usage and approvals. This metric reflects the ratio of accepted suggestions to total suggestions across all creator skills in your instance.

A satisfaction score indicates that users accepted or approved all AI-generated suggestions. Compare this metric over time to track improvements in suggestion quality and relevance.

You can view the creator skills performance for the available skills and set the time period selecting the external link icon. On the Creator skills performance page, you can see the total number of calls, calls accepted, cancelled, rejected, calls that were empty, and the satisfaction score. To change the time period, select the calendar drop-down, choose the time period, and select **Apply**.

## Top 5 most used creator Skills

This section ranks creator skills by total assists delivered over the selected time period. High usage indicates strong adoption and integration into developer workflows.

Each skill displays both absolute assist count and satisfaction percentage. Skills with high usage and high satisfaction are strong candidates for broader promotion and training programs.

## Instance with highest skill Usage

This metric identifies which instance in your ServiceNow environment has generated the most creator skill assists. High usage may indicate:

Use this insight to understand which instances are leading adoption and to share best practices from high-usage instances with others in your organization.

## Designation with highest creator calls

This metric shows which user roles or designations use creator skills most frequently. Tracking creator skill usage by designation helps identify which personas and job roles benefit most from AI-powered assistance.

Use this information to tailor training and enablement programs to designations with lower adoption, and to understand where creator skills deliver most value.

## Creator call outcomes

This section breaks down all creator skill suggestions into four outcome categories:

-   Accepted: User accepted the suggestion and used it in their work.
-   Rejected: User explicitly rejected the suggestion or indicated it was not useful.
-   Cancelled: User cancelled or abandoned the creator skill session before completing the suggestion.
-   Empty: No usable suggestion was generated \(null or incomplete response\).

The total count of creator calls represents the cumulative demand for AI assistance across your instance. Monitor outcome ratios to identify quality issues, user satisfaction trends, and skill performance over time.

## Creator calls breakdown

This visualization shows the distribution of outcomes \(accepted, rejected, cancelled, empty\) for each creator skill. Use this breakdown to:

-   Identify which skills have the highest acceptance rates
-   Detect skills with high cancellation rates, which may indicate usability or performance issues
-   Compare skill quality and reliability
-   Prioritize skills for enhancement or training

Skills with consistently high acceptance and low rejection rates are performing well and are good candidates for expanded adoption. Skills with high rejection or empty response rates may require tuning, additional training data, or user education.

**Note:** You can view the creator calls breakdown by the following metrics:

-   By skill
-   By title/designation
-   By code development
-   By instance name

