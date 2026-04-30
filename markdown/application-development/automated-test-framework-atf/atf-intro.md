---
title: Getting started with the Automated Test Framework
description: If you are new to the Automated Test Framework, read this overview to learn what the framework can do. Next, follow the tutorial to create and run a test that uses the most basic of ATF features. After you feel comfortable with the basics, explore more advanced features provided by the ATF.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Exploring Automated Test Framework, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Getting started with the Automated Test Framework

If you are new to the Automated Test Framework, read this overview to learn what the framework can do. Next, follow the tutorial to create and run a test that uses the most basic of ATF features. After you feel comfortable with the basics, explore more advanced features provided by the ATF.

ATF features provide flexibility in how you test your instance.

## Test step configuration categories

<table id="table_bgz_wcg_kfb"><thead><tr><th>

Category

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Catalog in Service Portal

</td><td>

Perform end-to-end testing for a catalog item in the Service Portal.-   Open a record producer, catalog item, or order guide.
-   Set variable values and catalog item quantity.
-   Validate variable values, states, price, and items included in an order guide.
-   Navigate in an order guide.
-   Open and toggle catalog items in an order guide.
-   Add an item or an order guide to a shopping cart.
-   Order a catalog item or an order guide.
-   Submit a record producer.

</td></tr><tr><td>

Application Navigator

</td><td>

Create tests to check navigation features.-   Verify that application menus are listed in the left navigation bar.
-   Verify that application modules are listed in the left navigation bar.
-   Navigate to a module as if a user clicked the module in the left navigation bar.

</td></tr><tr><td>

Custom UI

</td><td>

Create simple tests that mimic user actions with no scripting.-   Set component values.
-   Assert that specified text is or is not on a page.
-   Validate component values.
-   Click components.
-   Validate the states of components \(read-only or not read-only\).

</td></tr><tr><td>

Form

</td><td>

Create tests of forms.-   Open a new form or an existing record.
-   Set field values.
-   Validate field values or field states \(such as mandatory, not mandatory, read only, not read only, visible, and not visible\).
-   Validate whether a UI action is visible.
-   Click a button on a modal page.
-   Click a UI action.
-   Submit a form.

</td></tr><tr><td>

Service Catalog

</td><td>

Perform end-to-end testing for a catalog item.-   Open a catalog item or a record producer.
-   Search for a catalog item.
-   Set variable values and catalog item quantity.
-   Validate variable values, states, and price.
-   Add an item to a shopping cart.
-   Order a catalog item.
-   Submit a record producer.

</td></tr><tr><td>

Forms in Service Portal

</td><td>

Create tests of forms in the Service Portal.-   Open a form.
-   Set field values.
-   Validate field values or field states \(such as mandatory, not mandatory, read only, not read only, visible, and not visible\).
-   Validate whether a UI action is visible.
-   Click a UI action.
-   Submit a form.

</td></tr><tr><td>

REST

</td><td>

Create and send an Inbound REST request and verify the response.-   Test any REST endpoint on the instance.
-   Use a REST request to create records, as well as retrieve, update, or delete records created in a previous test step or that already existed on the instance.
-   Verify the response status code, response headers, response time, and response payload.

</td></tr><tr><td>

Server

</td><td>

Perform more complex operations, including the following:-   Perform unit tests using JavaScript, including tests using the Jasmine test framework.
-   Test business rules, script includes, and other scripts.
-   Create tests that operate on data that you define.

</td></tr></tbody>
</table>## Output variables

Many test steps return output variables whose values you can use as inputs to a later step. For example, you can use output variables to accomplish the following tasks:

-   Perform a server-side assert on a record that you previously inserted.
-   Create a record as one user, and then reopen its form as a different user.

## Custom test step configurations

In addition to the steps built into the Automated Test Framework, you can create custom test step configurations. These custom steps can take input variables and return output variables that you define.

**Note:** You can only define custom test steps that run on the server. The Automated Test Framework does not support creating custom step configurations that run on the browser.

## Data preservation

The Automated Test Framework automatically tracks and deletes any data created by running tests, and automatically rolls back changes after testing.

## Test suites

Test suites enable you to execute a batch of tests in a specified order. In addition, test suites can be hierarchical, with suites nested within other suites. You can associate test suites with schedules that determine when the system runs the test suites.

-   **[Build and run your first automated test](../task/atf-tut-build-first.md#)**  
Follow these step-by-step instructions to create and run your first automated test. This test creates a new user record.
-   **[Next steps with the Automated Test Framework](atf-next-step-concepts.md)**  
After you feel comfortable creating and running simple tests, explore the more advanced features of the Automated Test Framework.
-   **[Domain separation and Automated Test Framework](domain-separation-auto-test-framework.md)**  
Domain separation is supported in the Automated Test Framework. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[Exploring Automated Test Framework](automated-test-framework.md)

