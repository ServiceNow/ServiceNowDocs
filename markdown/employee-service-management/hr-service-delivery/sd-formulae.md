---
title: HR Success Dashboard indicators KPI definitions and formulae
description: Enable HR Success Dashboard indicators and configure to determine and use the Key Performance Indicators \(KPIs\) and formulae.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [HR Success Dashboard indicators reference, HR Success Dashboard indicators, HR Service Delivery, Employee Service Management]
---

# HR Success Dashboard indicators KPI definitions and formulae

Enable HR Success Dashboard indicators and configure to determine and use the Key Performance Indicators \(KPIs\) and formulae.

## Performance Overview

HR Success Dashboard indicators uses the following KPIs and definitions:

-   **Self-solved:** Calculated from the daily average number of times your users achieved a resolution without intervention from Tier 1 Agents in the report range. Includes numbers from Self-solved using Virtual Agent, Self-solved using Knowledge and Automated resolutions \(For example, HR tickets auto-resolution via Virtual Agent\). See the formula:

    ```
    [Self-solved using Virtual Agent + Self-solved using Knowledge + Automated resolutions] / [Total ticket resolutions + Self-solved (VA) + Self-solved (KB)] x 100 
    ```

    -   **Self-solved using Virtual Agent:** Number of automated conversations that helped the user solve their problem. In the base system. This is determined by the instrumented deflection node in the VA topic.
        -   **HR issues self-solved using Virtual Agent:** Number of times users solved their issues or requests in a Virtual Agent conversation. This is recorded in the deflection metrics table by the **HR VA Self-Resolving** deflection pattern instrumented in the conversation.
        -   **Note:** To use a different method to determine this KPI, see [Configure Success Dashboard indicators KPIs](https://www.servicenow.com/docs/access?context=config-kpis-sdb&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

    -   **Self-solved using Knowledge:** Number of times users are able to solve their problems by reading Knowledge articles. This is determined when users read Knowledge articles and do not create a ticket in a 24-hour window.
        -   **HR issues self-solved using Knowledge:** Number of times users solved their issues or requests on their own by reading Knowledge Base articles. This is determined when the user opened provided article\(s\) and did not create a case in a 24-hour window. This is recorded in the deflection metrics table with the **HR case deflection using Knowledge** deflection pattern.
        -   **Note:** To use a different method to determine this KPI, see [Configure Success Dashboard indicators KPIs](https://www.servicenow.com/docs/access?context=config-kpis-sdb&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

    -   **Automated Resolutions definition:** Number of times the ticket is resolved automatically using automated workflows or by Issue Auto Resolution.
        -   The Isuue Auto Resolution value is determined by the deflection node configured in the Issue Auto Resolution Virtual Agent topic.
        -   The Request Fulfilled Automatically value is the number of requested items that are fulfilled using automated workflows. When the catalog item uses an automated workflow, the **Fulfillment automation level** field of the catalog item must be set to **Fully-automated** for it to be included in this metric.
            -   **HR cases automatically fulfilled:** HR cases that are fulfilled using automated workflows. When the catalog item uses an automated workflow, the fulfillment automation level field of the record producer level item must be set to Fully automated. Once such an item is submitted, the automation level gets recorded.
            -   **Note:** To use a different method to determine this KPI or add more sources \(for example, automated catalog workflows\), see [Configure Success Dashboard indicators KPIs](https://www.servicenow.com/docs/access?context=config-kpis-sdb&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

    -   **Total ticket resolutions:** The number of HR issues resolved.
-   **Call deflection:** Calculated from the number of times per day requesters performed the actions, Ticket submissions using Service Catalog, Ticket submissions using Virtual Agent, Self-solved using Virtual Agent and Self-solved using Knowledge without Tier 1 agent intervention. See the formula:

    ```
    [Catalog ticket submissions + VA ticket submissions + Self-solved (VA) + Self-solved (KB)]/ [Total tickets submitted + Self-solved (VA) + Self-solved (KB)] x 100 
    ```

    -   **Catalog ticket submissions:** HR cases submitted using the Service Catalog in the Service Portal or the Now Mobile app.
        -   **HR Cases submitted using Service Catalog:** Number of HR case submissions from the Service Portal or Now Mobile app, as recorded in the HR case table with source as Self Service.
        -   **Note:** If you use a different method to determine this KPI or add more sources \(for example, automated catalog workflows\), see [Configure Success Dashboard indicators KPIs](https://www.servicenow.com/docs/access?context=config-kpis-sdb&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

    -   **VA ticket submissions:** Number of times the ticket was submitted using the Virtual Agent. This is determined by the deflection node instrumented in the Virtual Agent topic.
        -   **HR Cases submitted using VA:** Number of HR case submissions from Service Portal or Now Mobile app, as recorded in the HR case table with the source as Virtual Agent.
        -   **Note:** If you use a different method to determine this KPI or add more sources \(for example, automated catalog workflows\), see [Configure Success Dashboard indicators KPIs](https://www.servicenow.com/docs/access?context=config-kpis-sdb&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

    -   **Self-solved deflections:** Number of issues or requests users solved on their own using the Virtual Agent and the Knowledge Base articles.

        ```
        [Self-solved using Virtual Agent + Self-solved using Knowledge Articles]
        ```

        -   **HR issues self-solved using Virtual Agent:** Number of times users solved their issue or requests in a Virtual Agent conversation. This is recorded in the deflection metrics table by the HR **VA Self-Resolving** deflection pattern instrumented in the conversation.
        -   **HR issues self-solved using knowledge:** Number of times users solved their issues or requests on their own by reading Knowledge Base articles. This is determined when the user opened provided articles and did not create a case in a 24-hour window. This is recorded in the deflection metrics table with the **HR case deflection using Knowledge** deflection pattern.
        -   **Note:** If you use a different method to determine this KPI or add more sources \(for example, automated catalog workflows\), see [Configure Success Dashboard indicators KPIs](https://www.servicenow.com/docs/access?context=config-kpis-sdb&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

-   **Structured tickets completed:** Total number of HR cases completed successfully in the report range.
    -   **Structured HR Cases Closed:** Number of HR cases with a state of **Closed complete** where the associated HR Service has any Fulfilment Type other than **Manual**.
    -   **Note:** If you use a different method to determine this KPI, see [Configure Success Dashboard indicators KPIs](https://www.servicenow.com/docs/access?context=config-kpis-sdb&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

-   **Successful predictions:** Successful predictions works by Predictive Intelligence solutions, counted when the prediction made by the solution is the same as the final value. In the base system, this value is determined when the system uses classification to predict and the final value in the case table is the same as the predicted value.
    -   **Successful predictions:** Total successful predictions by Predictive Intelligence and the Natural Language Understanding \(NLU\) solutions.
    -   **Successful NLU predictions:** Successful prediction of the number of times the NLU prediction model accurately understood the intent of the user's conversation or auto-selected a topic.
        -   **Successful HR case predictions:** Number of times successful predictions have been made by the Predictive Intelligence solutions. It is counted when the prediction made by the solution is the same as the final value of the field in the HR case table.
        -   **Note:** If you use a different method to determine this KPI, see [Configure Success Dashboard indicators KPIs](https://www.servicenow.com/docs/access?context=config-kpis-sdb&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).


## Service Quality

-   **Customer satisfaction score:** It is the average of the customer satisfaction scores based on the surveys conducted after the issue was resolved.

    **HR Average CSAT:** HR case normalized satisfaction score or the HR Service Delivery Survey instances.

-   **Mean time to resolve:** It is the average of the time between the ticket creation and the ticket closure.

    **HR Case MTTR:** The sum duration of the closed HR cases or the number of closed HR cases.

-   **% Breached SLA:** It is the percentage of the issues that were resolved after the Service Level Agreement \(SLA\)s was breached.

    **HR cases Breached SLA%:**

    ```
    (Number of Closed HR cases with Breached SLAs / Number of Closed HR cases) * 100
    ```

-   **% Tickets resolved without reassignment:** It is the percentage of tickets that are resolved without reassigning the ticket to a different user.

    **% HR cases closed without reassignment:** It shows the HR cases that were closed and has reassignment count as zero.


