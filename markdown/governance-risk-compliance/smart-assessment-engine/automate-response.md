---
title: Automate response
description: Set up default responses for questions so that assessors can complete assessments quickly and provide quality results.
locale: en-US
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
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
    You can select a default response that doesn't have a condition or one that is dependent on multiple conditions. Assessors can then verify, adjust, or keep these default responses.

-   **Scripts**

    Enables you to create dynamic automated responses. You can create scripts that retrieve, transform, and map data from various sources, such as other questions, tables, or templates. You can then integrate this data into the response. With these scripts, you can:

    -   Generate dynamic default responses based on other questions, creating real-time adaptability.
    -   Query tables to fetch specific data and incorporate it into the response, confirming relevant information is included.
    -   Set up conditions within the script to handle different scenarios, enabling complex and dynamic automation workflows.
    ![Setting up a default response for a question using a script.](../image/automate-response-script.png)


When setting up the automated response, you can use if-then conditions to build the required criteria for the response. For more information, see [Configure an automatic response for a question](../task/configure-automatic-response-for-a-question.md).

