---
title: ServiceNow Studio tutorial part 3: Expand to a departmental solution
description: Your first request-fulfill workflow is the first step toward full automation-not just a standalone process. To maximize its impact, take a strategic approach to scaling workflow automation, improving efficiency, and streamlining service delivery to enhance and support the initial workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/servicenow-studio-classic/sns-z-tutorial-expand-departmental-solution.html
release: zurich
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [ServiceNow Studio tutorial, Explore, ServiceNow Studio, Developing your application, Building applications]
---

# ServiceNow Studio tutorial part 3: Expand to a departmental solution

Your first request-fulfill workflow is the first step toward full automation-not just a standalone process. To maximize its impact, take a strategic approach to scaling workflow automation, improving efficiency, and streamlining service delivery to enhance and support the initial workflow.

This expansion transforms the initial request process into a fully scalable departmental solution. Here are key workflows that can complement and expand your automation efforts.

\[Omitted image "sns-z-tut-expand-workflows.png"\] Alt text: Requests and services, inquiries, issues, and other custom workflows all expand the automation efforts set out in this tutorial.

## Add additional workflows

By expanding your workflows strategically, you create a seamless, efficient service experience, reducing manual effort and ensuring consistent service delivery across your organization. Follow the steps from the marketing design request to configure workflows for inquiries and issues.

1.  **Create tables**. Both tables should start from a blank table and extend the Task table the same way as the Marketing Design Request table.

    1.  Table label: Marketing Inquiry
    2.  Auto-number: Selected
    3.  Prefix: MKTINQ
    4.  Permissions: Same as the Marketing Design Request table
    \[Omitted image "sns-z-tut-mktinq-table.png"\] Alt text: Configure the options for the Marketing inquiry table.

    1.  Table label: Marketing Issue
    2.  Auto-number: Selected
    3.  Prefix: MKTISS
    4.  Permissions: Same as the Marketing Design Request table
    \[Omitted image "sns-z-tut-mktiss-table.png"\] Alt text: Configure the options for the Marketing issue table.

2.  **Add fields** to your tables.

    1.  **Label**: `Inquiry summary`
    2.  **Type**: `String`
    3.  **Max length**: `160`
    \[Omitted image "sns-z-tut-inquiry-summary.png"\] Alt text: Add fields to the Marketing Inquiry table.

    1.  **Label**: `Issue summary`
    2.  **Type**: `String`
    3.  **Max length**: `160`
    \[Omitted image "sns-z-tut-issue-summary.png"\] Alt text: Add fields to the Marketing Issue table.

3.  **Configure the form**.
    1.  Remove the same fields from the form as you did for the Marketing Design Request form.
        -   **Configuration item**
        -   **Parent**
        -   **Active**
        -   **Short description**
    2.  Add the **Inquiry summary** field above the **Description** field.

        \[Omitted image "sns-z-tut-inquiry-summary-form.png"\] Alt text: Configure the form for Marketing Inquiry with an Inquiry summary field.

    3.  Add the **Issue summary** field above the **Description** field, and replace the **Priority** field with the **Impact** field.

        \[Omitted image "sns-z-tut-issue-summary-form.png"\] Alt text: Configure the Marketing Issue form with an Issue summary field and an impact field.

4.  **Create the record producer**.
    1.  **Catalog**: `Service Catalog`
    2.  **Category**: `Departmental Services`
    3.  Add the following questions for inquiries and issues:
        -   Inquiry/Issue summary \(Single line\)
        -   Description \(Multi-line\)
            -   **Item name**: `Marketing Inquiry`
            -   **Destination** \(record submission table\): `Marketing Inquiry`

                \[Omitted image "sns-z-tut-inquiry-summary-question.png"\] Alt text: Insert inquiry summary and description questions for your Marketing Inquiry table.

            -   **Item name**: `Marketing Issue`
            -   **Destination** \(record submission table\): `Marketing Issue`

                \[Omitted image "sns-z-tut-issue-summary-questions.png"\] Alt text: Insert Issue summary, Impact, and Description questions for the Marketing Issue form.

            -   Configure the **Impact** question the same way that you configured the **Media type** in the previous record producer, using the following choices:
                1.  **Display name**: `High`, **Value**: `1`
                2.  **Display name**: `Medium`, **Value**: `2`
                3.  **Display name**: `Low`, **Value**: `3`
    4.  Select **Map to specified field on table**, and fill in the **Table**, **Question**, and **Name** fields.

        **Note:** Name should be all lowercase with underscores instead of spaces.

5.  Submit both record producers when complete.

-   **[Create the Marketing department taxonomy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-z-tut-create-marketing-dept-taxonomy.md)**  
Create a marketing department taxonomy on the ServiceNow AI Platform.
-   **[Add departmental workflows to your workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-z-tut-add-dept-workflow-workspace.md)**  
A well-structured workspace improves task visibility, reduces response times, and ensures that fulfillers have all the necessary tools and information in one place. By using Workspaces, departments can standardize processes, reduce manual effort, and improve collaboration—leading to better service delivery, higher productivity, and organization-wide operational improvements.

**Parent Topic:**[ServiceNow Studio tutorial: Zurich](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-z-tutorial-landing.md)

