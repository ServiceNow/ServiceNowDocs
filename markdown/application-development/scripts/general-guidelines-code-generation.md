---
title: General guidelines for code generation
description: Use these general guidelines for code generation to get better code suggestions and create useful and accurate scripts.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring code generation, Now Assist for code generation, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# General guidelines for code generation

Use these general guidelines for code generation to get better code suggestions and create useful and accurate scripts.

## Writing prompts

-   **Write clear and specific but concise prompts**

    Specify the expected outcome and context, including necessary details like task requirements, specific APIs if you know them, and any constraints.

-   **Experiment with different prompts**

    As you refine and experiment, the Now LLM Service uses this feedback to learn and improve.

    -   Try adjusting task instructions and incorporating examples, and then observe how code suggestions differ with different prompt styles and levels of detail.
    -   Try including a short code snippet as an example of how to start the script with a single-shot prompt.
    -   Keep track of your prompts, including any modifications, and instructions for generating prompts to meet your specifications. This tracking enables easy regeneration of past results for comparative analysis.

<table id="table_ryd_22l_yxb"><thead><tr><th>

Strong prompt

</th><th>

Weak prompt

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Get incidents with related tasks

</td><td>

Get incidents with tasks

</td><td>

Includes sufficient detail.

</td></tr><tr><td>

Use glide aggregate to count number of P1 incidents closed between 3rd March to 13 April assigned to admin

</td><td>

Count P1 incidents between 3-3 and 4-13

</td><td>

Includes the API name and more specific language.

</td></tr><tr><td>

If open change request is P1, do not allow reducing the severity unless it's the creator

</td><td>

Don’t allow changing P1 change requests

</td><td>

Includes more specific instructions on what shouldn't change.

</td></tr><tr><td>

Gliderecord of the most recent change

</td><td>

Latest change

</td><td>

Includes the API name and more specific language.

</td></tr></tbody>
</table>## Reviewing code

-   **Review code**

    Implement strict and detailed reviews of the AI-generated code to determine its accuracy, efficiency, and how well it adheres to your coding standards.

-   **Test code**

    Validate the code by running it against test cases in controlled environments to ensure that it functions according to your requirements.


