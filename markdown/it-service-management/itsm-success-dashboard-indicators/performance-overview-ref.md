---
title: Performance overview
description: Performance overview details all the KPIs and metrics that help you analyse the benefits of your ITSM implementation.
locale: en-US
release: zurich
product: ITSM Success Dashboard Indicators
classification: itsm-success-dashboard-indicators
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [ITSM Success Dashboard indicators KPI definitions and formulas, Explore, ITSM Success Dashboard indicators, IT Service Management]
---

# Performance overview

Performance overview details all the KPIs and metrics that help you analyse the benefits of your ITSM implementation.

-   **Self-solved percentage:** Calculated from the daily average number of times your users achieved a resolution without intervention from Tier 1 Agents in the report range. Includes numbers from Self-solved using Virtual Agent, Self-solved using Knowledge and Automated resolutions \(For example, Incident auto-resolution via Virtual Agent\). See the formula:

    ```
    [Self-solved (VA, KB, QnA, Proactive Engagement) + Automated resolutions] / [Total Tickets Resolution + Self-solved (VA, KB, QnA, Proactive Engagement) + Self service using Password Reset apps]*100 
    ```

    -   **Self-solved using Virtual Agent:** Number of automated conversations that helped the user solve their problem. This is determined when users complete a virtual agent conversation and does not engage \(Interactions\) with a human agent in the next 24-hour window.

        Considers both Virtual Agent powered by NLU and LLM \(Now Assist VA\)

        **Note:** To use a different method to determine this KPI, see [Configure Success Dashboard indicators KPIs](../task/config-kpis-sdb.md).

        To update the live agent script include see, [Update the live agent script include](../task/update-live-agent-script-include.md).

    -   **ITSM issues solved using NOW Assist VA \(LLM\):** Number of times the users were able to resolve their issues by interacting with Now Assist Virtual Agent \(NAVA\) conversation. This is determined when a user completes a Now Assist Virtual Agent conversation and doesn't create an incident or engages \(Interactions\) with a human agent in a 24-hour window.

        To update the live agent script include see, [Update the live agent script include](../task/update-live-agent-script-include.md).

    -   **Self-solved using Knowledge:** Number of times users were able to solve their problems by reading knowledge articles. This is determined when users read knowledge article\(s\) and do not create ticket or engages with a human agent in a 24-hour window.

        **Note:** To use a different method to determine this KPI, see [Configure Success Dashboard indicators KPIs](../task/config-kpis-sdb.md).

        To update the live agent script include see, [Update the live agent script include](../task/update-live-agent-script-include.md).

    -   **Self-solved using QnA:** Self-solved using the AI Search when a user interacts with a Virtual Agent or on Portal and gets a summarized answer from AI Search. This is determined when users are presented with a AI Search QnA result and do not go on to create ticket or engage with a human agent in a 24-hour window.

        To update the live agent script include see, [Update the live agent script include](../task/update-live-agent-script-include.md).

    -   **Self-solved using Proactive Engagement for DEX** The number of digital experience issues **Self-solved using Proactive Engagement for DEX**. This is determined when DEX proactively detects issues and Proactive Engagement helps users self-solve them.

        To know more about the Proactive Engagement see, [Proactive Engagement](../../proactive-engagement/proactive-engagement-landing-page.md).

    -   **Automated Resolutions:** Number of times the ticket was resolved automatically. In the base system, the indicators contributing to this metric are Incident Auto Resolution and Request Fulfilled Automatically.

        -   The Incident Auto Resolution value is determined by the deflection node configured in the Issue Auto Resolution Virtual Agent topic.
        -   The Request Fulfilled Automatically value is the number of requested items that are fulfilled using automated workflows. When the catalog item uses an automated workflow, the **Fulfillment automation level** field of the catalog item must be set to **Fully-automated** for it to be included in this metric.
        -   **Accounts unlocked using Password Reset apps**: Number of times users were able to unlock their accounts successfully using Password Reset apps.
        -   **Passwords updated using Password Reset apps**: Number of times users were able to update their account passwords using the Password Reset apps.
        **Note:** To use a different method to determine this KPI or add more sources \(for example, automated catalog workflows\), see [Configure Success Dashboard indicators KPIs](../task/config-kpis-sdb.md).

    -   **Total ticket resolutions:** Number of incidents resolved + Number of requested items closed + Number of Agent interactions not resulting in tickets \(closed\).
-   **Call deflection:** Calculated from the number of times per day requesters performed the actions, Ticket submissions using Service Catalog, Ticket submissions using Virtual Agent, Self-solved using Virtual Agent and Self-solved using Knowledge without Tier 1 agent intervention. See the formula:

    ```
    [Catalog ticket submissions + VA ticket submissions + Self-solved (VA) + Self-solved (KB)]/ [Total tickets submitted + Self-solved (VA) + Self-solved (KB)] x 100 
    ```

    -   **Catalog ticket submissions:** Incidents and requested items submitted using Service Catalog in Service Portal or Now Mobile app.
    -   **VA ticket submissions:** Number of times the ticket was submitted using Virtual Agent. In the base system, this is determined by the `ITSM - Triage & Created` deflection pattern instrumented in the Virtual Agent topic. The topics shipped with ITSM VA Conversations already have these nodes instrumented but must be instrumented in all other topics that create incidents.

        **Note:** If you use a different method to determine this KPI or add more sources \(for example, automated catalog workflows\), you can use the steps described in [Configure Success Dashboard indicators KPIs](../task/config-kpis-sdb.md).

    -   **NOW Assist ticket submissions:** Number of times the ticket was submitted using NOW Assist. In the base system, this is determined by the `ITSM - Triage & Created` deflection pattern instrumented in the NOW Assist topic. The topics shipped with NOW Assist Conversations already have these nodes instrumented but must be instrumented in all other topics that create incidents.
    -   **Total tickets submitted:** Incidents created + RITMs created.
-   **Structured tickets:** Total number of requested items completed successfully in the report range.
-   **Productivity moments per user:** Productivity Moment is calculated when the ServiceNow products helped a user to be more productive while working in their day to day operations.

    -   **Productivity in search per user**: The number of times the NLU prediction model accurately understood the intent of the user's conversation or auto-selected a topic.
    -   **Productivity in routing per user**: Successful predictions of incident fields such as assignment group, or category by Predictive Intelligence solutions, counted when the prediction made by the solution is the same as final value when the incident was closed.
    -   **Productivity in fulfilment per user**: Includes any productivity gains achieved where ServiceNow is helping the employees to save time to resolve a ticket.
        -   **Incident summarization - Now Assist** Number of times Now Assist helped the agents by summarizing the Incidents that they worked on.
        -   **Interaction summarization - Now Assist** Number of times Now Assist helped the agents by summarizing the Interactions that they worked on.
        -   **Incident resolution note Generation - Now Assist** Number of times Now Assist helped the agents by providing resolution note and code.
        -   **Successful Change Risk Explanation - Now Assist** Number of times Now Assist helped the agents by explaining the Risk Assessment for a Change Request that they worked on.
        -   **Successful Change Summarization - Now Assist** Number of times Now Assist helped the agents by summarizing the Change Request that they worked on.
    -   **Productivity in knowledge articles generation** Includes the number of knowledge articles drafted and published using Now Assist.

        **Knowledge Articles created using Now Assist** Number of times Now Assist helped the agents in creating Knowledge Article.

    **Note:** If you use a different method to determine this KPI, you can do so using the steps described in [Configure Success Dashboard indicators KPIs](../task/config-kpis-sdb.md).


**Parent Topic:**[ITSM Success Dashboard indicators KPI definitions and formulas](sd-kpi-formulae.md)

