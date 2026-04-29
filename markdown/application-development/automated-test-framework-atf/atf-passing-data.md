---
title: Passing data from one automated test step to another
description: Some automated test steps create data that you can use as an input to a subsequent step.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Passing data from one automated test step to another

Some automated test steps create data that you can use as an input to a subsequent step.

You can pass data from one test step to another using input variables and output variables.

The term input variables is another name for the field values associated with a step. These values are input variables because they provide the input the step needs to accomplish its task. For example, the Open Form step has these input variables: **Table**, **Record**, and **View**.

![Existing record Test Step form](../image/atf-use-backref-form.png "Example test step showing input variables")

Some step types also have output variables. These are the values that later steps in the same test can use as input. For example, the Record Insert step has an output variable called Record which contains the sys\_id of the newly created record.

**Note:** Input data can also be passed to an automated test case from an external source such as a `.csv` file.

The test step form doesn't indicate if a test step has output variables or not. You can easily tell if any output variables are available to provide a value to any given input variable. If you can map the value of one step's output variable to the current step's input variable, the system displays the mapping icon \(![mapping icon](../image/rem-value-icon.png)\) to the right of that input field. When you click the variable mapping icon, the system displays a tree giving you access to any available output variables from previous steps.

![Available output variables](../image/atf-use-backref-icon-clked.png "Example test step showing output variables")

For step-by-step instructions on how to assign the value of an output variable to another step's input variable, see [Pass values from one automated test step to another](../task/atf-retrieve-value.md).

For an example of a test that passes variables using input and output variables, see [Automated Test Framework use case: reference a value from a previous step](../task/atf-use-backref.md).

-   **[Pass values from one automated test step to another](../task/atf-retrieve-value.md)**  
Assign a form field the value of an output variable returned from a previous step.

**Parent Topic:**[Building and running automated tests with the Automated Test Framework](atf-build-overview.md)

