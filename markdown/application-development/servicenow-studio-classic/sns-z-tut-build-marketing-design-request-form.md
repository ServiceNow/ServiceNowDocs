---
title: Build the marketing design request form
description: Edit the form view of the Marketing Design Request table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/servicenow-studio-classic/sns-z-tut-build-marketing-design-request-form.html
release: zurich
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Tutorial part 1: Begin with an MVP, ServiceNow Studio tutorial, Explore, ServiceNow Studio, Developing your application, Building applications]
---

# Build the marketing design request form

Edit the form view of the Marketing Design Request table.

## Before you begin

Role required: admin

## Procedure

1.  Open the Marketing Design Request table, if it isn't open already.

2.  Select **Forms** in the top ribbon.

    \[Omitted image "sns-z-tut-forms-view.png"\] Alt text: Select Forms view to edit the form for your table.

3.  Remove the **Configuration item** field from the form by hovering over the field and selecting the delete field icon \(\[Omitted image "fb-delete-icon.png"\] Alt text: Delete form element.\).

4.  Repeat the process in step 3 to remove the following additional fields from the form.

    -   **Active**
    -   **Parent**
5.  In the Add form elements panel, select the **Media type** field and drag it onto the form after the **Assigned to** field.

    \[Omitted image "sns-z-tut-media-type-field-added.png"\] Alt text: After adding the Media type field to the form, the field appears highlighted on the form.

6.  Repeat the process in step 5 to add the following additional fields to the form.

    |Field name|Location on the form|
    |----------|--------------------|
    |**External**|After **State**.|
    |**Project name**|Before **Short description**.|
    |**Design copy**|After **Project name**.|
    |**Special instructions**|After **Design copy**.|

7.  Remove the **Short description** field from the form by hovering over the field and selecting the delete field icon \(\[Omitted image "fb-delete-icon.png"\] Alt text: Delete form element.\).


**Parent Topic:**[ServiceNow Studio tutorial part 1: Begin with an MVP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/servicenow-studio-classic/sns-z-tutorial-begin-with-mvp.md)

