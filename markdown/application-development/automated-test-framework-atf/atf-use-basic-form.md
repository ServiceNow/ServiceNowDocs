---
title: Automated Test Framework use case: test basic form operations
description: This use case illustrates testing basic form operations with the Automated Test Framework.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automated Test Framework use case examples, Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Automated Test Framework use case: test basic form operations

This use case illustrates testing basic form operations with the Automated Test Framework.

## Before you begin

Role required: atf\_test\_admin

## About this task

![Test steps](../image/atf-use-cat-task-steps.png "Steps in test")

## Procedure

1.  Impersonate a user with the permissions needed to perform these steps, in this example ATF.User.

    ![Impersonate user test step](../image/atf-use-bf-impersonate.png "Test step 1 - Impersonate")

2.  Open a form, in this example a Catalog Task form.

    ![Form for Open a New Form using the Catalog Task form](../image/atf-use-bf-open-form.png "Test step 2 - Open a new Form")

3.  On the open form, set field values, including for any mandatory fields.

    This example sets field values for **Assigned to**, **Short description**, and **Description**.

    ![Form for Set Field Values](../image/atf-use-cat-task-field-values.png "Test step 3 - Set Field Values")

4.  Submit the open form.

    ![Form for Submitting a Form](../image/atf-use-cat-task-submit.png "Test Step 4 - Submit a Form")


**Parent Topic:**[Automated Test Framework use case examples](../concept/atf-use-cases.md)

