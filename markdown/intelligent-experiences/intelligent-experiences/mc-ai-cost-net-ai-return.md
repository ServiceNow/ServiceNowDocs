---
title: AI cost and net AI return
description: The AI Control Tower tracks the cost of your AI systems and subtracts it from the productivity value to show the net AI return. Cost is tracked by vendor from token consumption or a direct cost.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
---

# AI cost and net AI return

The AI Control Tower tracks the cost of your AI systems and subtracts it from the productivity value to show the net AI return. Cost is tracked by vendor from token consumption or a direct cost.

## AI cost and net AI return overview

The AI Control Tower \(AICT\) reports the productivity value of your AI systems as productivity gains, which it derives from your value templates and can express in currency. It also tracks the cost of running those AI systems. The net AI return is the money saved minus the cost.

## Key benefits

AI cost tracking provides the following benefits:

-   Show the return of your AI systems by comparing value against cost.
-   Track cost automatically for integrated vendors through the trace integration.
-   Record cost as token consumption or as a direct cost.
-   Break down cost by vendor and by AI system.

## How cost is calculated

The AI Control Tower calculates cost at the vendor level, because usage details for external vendors are available for the vendor rather than for each agent. For each vendor, the calculation uses the unit consumption, such as tokens, and the cost. A breakdown at the AI system level appears where that data is available.

Integrated vendors, such as ServiceNow, the Vertex AI service, the Amazon Bedrock service, and the Azure Foundry service, use the trace integration to capture token consumption. When the API endpoint and the validation key are configured, the AI Control Tower tracks cost for those vendors automatically.

You can define cost in two ways. Input and output token cost applies a separate rate to every million input tokens and output tokens. Direct cost applies a total cost that you enter, without a unit consumption.

To express value in currency, you configure an hourly rate, which is the total workforce cost divided by the total workforce hours. You can set a single hourly rate or set a rate for each persona.

**Note:**

-   Cost configurations use effective dates. A configuration for a future date is a draft, the current configuration is active, and a past configuration is expired.
-   Cost is calculated for the previous day, so a new cost configuration appears on the dashboard after the next scheduled run.

## Why cost tracking matters

Cost tracking connects the productivity hours that AI systems save to their financial impact, so that you can answer key business questions:

-   Are we getting value? How much money are we saving with AI?
-   What are we paying? How much do the AI systems actually cost?
-   Is it profitable? Are savings exceeding costs?
-   How long to payback? When will AI investments pay for themselves?
-   Where are the costs? Which vendors cost the most?

Without cost tracking, you can see hours saved but can't connect them to financial impact. With it, you have complete visibility into AI net returns.

## Three pillars of the Cost framework

The Cost framework rests on three interconnected pillars that together enable complete financial visibility and net return analysis:

-   **Savings**

    Quantifies the value \(benefits\) delivered by AI systems.

    The Savings pillar converts productivity into currency. AI systems are evaluated for the number of work hours they save. An average hourly rate defines the labor cost per hour. Money saved is calculated by multiplying the hours saved by the average hourly rate.

    For example, 40 hours saved × $100/hour = $4,000 in weekly savings.

-   **Cost**

    Tracks all expenses associated with running AI systems, across LLM token costs, Assist costs, integration costs, and infrastructure costs.

-   **Net returns**

    Calculates the net financial benefit as savings minus cost. A positive result is profitable, zero is breakeven, and a negative result means the investment is not yet profitable.

    For example: $4,000 savings − $500 cost = $3,500 net returns \(profitable\); $2,000 − $2,000 = $0 \(breakeven\); $1,000 − $2,000 = −$1,000 \(not yet profitable\).


## Cost categories tracked

The Cost pillar tracks the following categories of expense:

-   **LLM token costs**

    Charges from LLM providers based on token usage. Token costs vary by the model used \(more advanced models cost more\), the usage volume \(more interactions mean higher cost\), and vendor pricing \(different providers have different rates\).

-   **Assist costs**

    ServiceNow AI Assist charges for running AI agents and assistants. These recurring costs are based on the number of active agents, the frequency of usage, and the complexity of tasks.


## How costs are tracked

The system tracks costs automatically as follows:

1.  Captures all LLM API calls and token usage from integrated systems.
2.  Records token costs based on vendor pricing models.
3.  Aggregates Assist costs from configuration and usage tracking.
4.  Groups costs by system, vendor, department, and time period.
5.  Calculates trends and period-over-period comparisons.

Costs are updated in real-time, although dashboards typically show consolidated daily or hourly summaries.

## Complete calculation flow

The Cost framework calculates financial metrics in the following sequence:

1.  The system collects productivity metrics \(hours saved from AI automation\).
2.  The system looks up the average hourly rate configured for your organization.
3.  The system calculates money saved as hours saved × hourly rate.
4.  The system aggregates total cost as token costs + Assist costs.
5.  The system calculates net returns as money saved − total cost.

All of these calculations feed the dashboards and reports used for stakeholder analysis.

## Key assumptions and considerations

The Cost framework relies on several assumptions. Verify them regularly and adjust configurations as needed:

-   Productivity measurement accuracy: Hours saved must be captured accurately from AI system activity logs.
-   Hourly rate accuracy: The average hourly rate must reflect the true labor cost, or a documented business rationale must support different rates.
-   Cost completeness: All relevant costs must be captured.
-   Time period consistency: Savings and costs must cover the same time period for a valid comparison.

