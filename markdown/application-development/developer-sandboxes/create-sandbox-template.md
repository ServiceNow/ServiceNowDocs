---
title: Create a sandbox template
description: Create a Developer Sandboxes template to reuse generated data in your sandbox, without manually inputting data every time.
locale: en-US
release: australia
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administering, Developer Sandboxes, Developing your application, Building applications]
---

# Create a sandbox template

Create a Developer Sandboxes template to reuse generated data in your sandbox, without manually inputting data every time.

## Before you begin

Role required: admin or sandbox\_manager

## About this task

Developer Sandboxes templates enable delegated developers to reuse the data so that they can test their changes without manually inputting the data every time. For example, for developers working on ITSM code, admins can create a template specific to the standard ITSM apps and tables.

You can create a template once, and reuse any existing templates when creating sandboxes.

## Procedure

1.  Navigate to **All** &gt; **Sandbox Management** &gt; **Sandbox Templates**.

2.  Select **New**.

    ![Select New to add a template.](../image/dev-sbx-template-new.png "Sandbox Templates page with New button")

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for your template.|
    |Data Generation Profile|Leave this field empty.|

    ![Complete the field to add a template](../image/dev-sbx-templ-add-repo2.png "Create a template")

4.  Select **Submit**.

5.  Add a repository to the template.

    For more information on repositories, see [ServiceNow application repository](../../applications/concept/app-repo.md).

    1.  Select the **Name** of the template you just created.

        ![Select the template you just created](../image/dev-sbx-templ-add-repo1.png "Select the template to add a repo to")

    2.  Select **New** for the Sandbox Template Repository related list.

        ![Select the New button](../image/dev-sbx-add-repo-new-btn.png "Add a repository to a template")

    3.  Search for and select the repository URL.

    4.  Select **Submit**.


