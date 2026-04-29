---
title: Automate response
description: Set up default responses for questions so that assessors can complete assessments quickly and provide quality results.
locale: en-US
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Automate response

Set up default responses for questions so that assessors can complete assessments quickly and provide quality results.

Response automation aims to make the assessment process efficient by reducing manual data entry and providing a static response or script-based approach to automate responses. A template manager can make the responses read-only or editable. You can set up the automated responses with the following:

-   **Default Response field**

    Enables you to set default answers for the following question types:

    -   Text
    -   Drop-down lists
    -   Radio buttons
    -   Check boxes
    -   Date
    -   Date &amp; time
    -   Number
    -   Code
    You can select a default response that doesn't have a condition or one that is dependent on multiple conditions. Assessors can then verify, adjust, or keep these default responses.

-   **Scripts**

    Enables you to create dynamic automated responses. You can create scripts that retrieve, transform, and map data from various sources, such as other questions, tables, or templates. You can then integrate this data into the response. With these scripts, you can:

    -   Generate dynamic default responses based on other questions, creating real-time adaptability.
    -   Query tables to fetch specific data and incorporate it into the response, confirming relevant information is included.
    -   Set up conditions within the script to handle different scenarios, enabling complex and dynamic automation workflows.
    ![Setting up a default response for a question using a script.](../image/automate-response-script.png)


## Set resonse as editable

Under Additional options, the Set response as editable setting controls whether the respondent can modify the automated response and how re-evaluation behaves:

-   **Enabled \(default\)**

    The respondent can edit the automated response. Response automation conditions are evaluated when the assessment is created and re-evaluated when a dependent question changes. However, if the respondent has manually modified the response, the re-evaluated automated value is not applied and the respondent's manual entry is preserved.

-   **Disabled**

    The response is read-only and the respondent cannot modify it. Response automation conditions are evaluated when the assessment is created and re-evaluated every time a dependent question changes. Because the respondent cannot edit the response, the re-evaluated value always overwrites the current response.


**Note:** When Set response as editable is disabled, the Required toggle on the question is automatically turned off, since the system provides the response.

When setting up the automated response, you can use if-then conditions to build the required criteria for the response. For more information, see [Configure an automatic response for a question](../task/configure-automatic-response-for-a-question.md).

