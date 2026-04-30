---
title: General guidelines for code generation
description: Use these general guidelines for code generation to get better code suggestions and create useful and accurate scripts.
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore Now Assist for Code, Now Assist for Code, Scripting, API implementation, API implementation and reference]
---

# General guidelines for code generation

Use these general guidelines for code generation to get better code suggestions and create useful and accurate scripts.

## Writing prompts

-   **Write clear and specific but concise prompts**

    Specify the expected outcome and context clearly. Include important details like task requirements, specific APIs if you know them, and any limitations.

-   **Experiment with different prompts**
    -   Consider adjusting your task instructions and incorporating examples. Observe how the code suggestions change with different prompt styles and levels of detail.
    -   Keep track of your prompts, along with any modifications and instructions for generating prompts that meet your specifications.
-   **Character limit of the prompts**

    Short and concise prompts generate better outcomes.

    On reaching 200 characters, a message appears to inform you that short, focused, task-oriented directions yield the best results.

    Input beyond 300 characters isn’t allowed.


<table id="table_ryd_22l_yxb"><thead><tr><th>

Weak prompt

</th><th>

Strong prompt

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Get incidents with tasks

</td><td>

Get incidents with related tasks

</td><td>

Includes sufficient detail.

</td></tr><tr><td>

Count P1 incidents between 3-3 and 4-13

</td><td>

Use Glide aggregate to count number of P1 incidents closed between March 3 to April 13 assigned to admin

</td><td>

Includes the API name and more specific language.

</td></tr><tr><td>

Don’t allow changing P1 change requests

</td><td>

If open change request is P1, don’t allow reducing the severity unless it's the creator

</td><td>

Includes more specific instructions on what shouldn't change.

</td></tr><tr><td>

Latest change

</td><td>

Glide record of the most recent change

</td><td>

Includes the API name and more specific language.

</td></tr></tbody>
</table>## Reviewing code

-   **Review code**

    Implement strict and detailed reviews of the AI-generated code to determine its accuracy, efficiency, and how well it adheres to your coding standards.

-   **Test code**

    Validate the code by running it against test cases in controlled environments to verify that it functions according to your requirements.


