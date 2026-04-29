---
title: Build the marketing design request form
description: Edit the form view of the Marketing Design Request table.
locale: en-US
release: australia
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2026-03-12"
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

    ![Select Forms view to edit the form for your table.](../image/sns-z-tut-forms-view.png)

3.  Remove the **Configuration item** field from the form by hovering over the field and selecting the delete field icon ![](../../../administer/form-builder/image/fb-delete-icon.png).

4.  Repeat the process in step 3 to remove the following additional fields from the form.

    -   **Active**
    -   **Parent**
5.  In the Add form elements panel, select the **Media type** field and drag it onto the form after the **Assigned to** field.

    ![After adding the Media type field to the form, the field appears highlighted on the form.](../image/sns-z-tut-media-type-field-added.png)

6.  Repeat the process in step 5 to add the following additional fields to the form.

    |Field name|Location on the form|
    |----------|--------------------|
    |**External**|After **State**.|
    |**Project name**|Before **Short description**.|
    |**Design copy**|After **Project name**.|
    |**Special instructions**|After **Design copy**.|

7.  Remove the **Short description** field from the form by hovering over the field and selecting the delete field icon ![](../../../administer/form-builder/image/fb-delete-icon.png).


**Parent Topic:**[ServiceNow Studio tutorial part 1: Begin with an MVP](../concept/sns-z-tutorial-begin-with-mvp.md)

