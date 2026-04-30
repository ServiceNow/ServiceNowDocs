---
title: Add customized variables in a document template
description: Customize variables at a record producer level, and call out those variables in the HTML document template that you are configuring.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Variables supported in HTML document templates, Document Templates of type HTML, Using Document Templates: HR Service Delivery use case, Document Templates, E-signature applications of HR Service Delivery, HR Service Delivery, Employee Service Management]
---

# Add customized variables in a document template

Customize variables at a record producer level, and call out those variables in the HTML document template that you are configuring.

## Before you begin

Role required: admin

## Procedure

1.  Open a record producer and fill in the required fields.

    Add the variables that you want to use in the **Variables** list.

    ![Variables in a record producer](../image/varibles-rec-pro.png "Example: Variable list in a record producer")

2.  Open an HTML document template that has the same table selected as the record producer.

    Call out the customized variables in the HTML template body by typing in the variable in this format, for example, $ \{variables.start\_date\).

    **Note:** start\_date refers to the exact **Name** of the variable in the **Variables** list in the record producer.

    ![Calling customized variables in an HTML document template](../image/variables-html.png "Example: Calling customized variables in an HTML document template")

    1 refers to variables from the table selected in the HTML document template.

    2 refers to customized variables from the variable list in the record producer.


