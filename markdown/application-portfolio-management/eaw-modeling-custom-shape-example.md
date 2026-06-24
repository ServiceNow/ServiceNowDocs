---
title: Custom shapes example
description: Use custom shapes to represent specific elements that are unique to your organization, such as custom business processes, systems, or roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-portfolio-management/eaw-modeling-custom-shape-example.html
release: yokohama
topic_type: task
last_updated: "2025-02-17"
reading_time_minutes: 3
breadcrumb: [Custom shapes support in the Enterprise Modeling and Visualization, Enterprise Modeling and Visualization in the EA Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Custom shapes example

Use custom shapes to represent specific elements that are unique to your organization, such as custom business processes, systems, or roles.

## Before you begin

Role required: System Administrator \(to upload images to the database\), APM admin \(to create diagram actions, custom shape library, add shape library element\).

## About this task

In this example, you will learn how to upload an image or shape to the database, create diagram action for the image or shape, create a custom shape library, add shape to the shape library, create a shape library element, and create a diagram using the shapes.

Create the shapes that represent the elements you want to include in your diagrams. Ensure the images are clear, simple, and visually distinct. The compatible format is .SVG. In this example, we use the ‘Database.svg’ image.

## Procedure

1.  Upload the image or shape to the database.

    1.  Navigate to **All** &gt; **System UI** &gt; **Images**.

        \[Omitted image "custom-shapes-upload-image.jpg"\] Alt text: Upload an image to the database

    2.  Select **New**.

        \[Omitted image "new-image-record.jpg"\] Alt text: Create new image record

2.  In the New image record, enter the name of the image file \(include file format extension\) and fill in other details.

3.  Select **Click to add...**.

    \[Omitted image "custom-shape-new-image-record.jpg"\] Alt text: Uploading a custom shape to the database

4.  Create a diagram action for the image in the Enterprise Architecture Workspace.

    1.  Log in as an APM admin user \(sn\_apm.apm\_admin\), navigate to the **Setup** section.

    2.  Under the **Enterprise Modeling and Visualization** section, select **Diagram Actions**.

        \[Omitted image "custom-shape-diagram-action.jpg"\] Alt text: Diagram action

    3.  Select New to create a diagram action for the image \(Database.svg\).

    4.  In the Diagram Action form, enter the following details:

        -   Name- Name for the diagram action
        -   Diagram builder configuration- Select APM diagram configuration from the list
        -   Node type- Select node type as ‘Image node container'
        -   Category- Select Default
        -   Sub category- Select Default sub category
        -   Icon- Enter name of the image
        \[Omitted image "custom-shape-diagram-action-form.jpg"\] Alt text: Diagram action form

5.  Create a custom shape library specific to your Org to add all the shapes to create diagrams for your organization.

    1.  As an APM Admin user, navigate to **Setup** &gt; **Enterprise Modeling and Visualization** &gt; **Shape Libraries**.

        \[Omitted image "custom-shape-libraries.jpg"\] Alt text: Shape libraries section

    2.  Select **New**.

    3.  Enter a name for the shape library, then select **Save**.

        \[Omitted image "custom-shape-new-library.jpg"\] Alt text: New shape library form

6.  Add a shape library element to associate the shape and its diagram action to the shape library.

    1.  As an APM Admin user, open the shape library you have created in the previous step.

    2.  Select the **Shape Library Elements** tab.

    3.  Select **New**.

        \[Omitted image "custom-shape-library-element.jpg"\] Alt text: Shape library element

    4.  In the Shape library element form, enter the following details:

        -   Tool tip- Enter text that you want to see on hovering the image.
        -   Diagram action- Select the diagram action that you have created in the previous step.
        -   Now icon- Enter the name of the shape or image.
        -   Name- Enter a name for the shape to be displayed in the Enterprise Modeling and Visualization application.
        -   Shape library- This field is automatically selected.
        -   Domain- Optional field.
        -   Entity configuration- Optional field.
        \[Omitted image "custom-shape-library-element-form.jpg"\] Alt text: Shape library element form

    5.  Select **Save**.

7.  Create a diagram using the shape uploaded.

    1.  Navigate to **Enterprise Modeling and Visualization** page.

    2.  Select &gt; **New** &gt; **Blank diagram**

        \[Omitted image "custom-shape-blank-diagram.jpg"\] Alt text: Create a blank diagram

    3.  Enter a name for the diagram and optionally, you can enter or select an existing architectural category for the diagram.

        \[Omitted image "custom-shape-create-diagram.jpg"\] Alt text: Create blank diagram modal

        Observe that the shape library that you created appears in the Shapes pallet. It contains the shape that you uploaded.

    4.  Click on the shape to add it to the canvas.

        \[Omitted image "custom-shape-add-to-canvas.jpg"\] Alt text: Adding a custom shape to the canvas

        The selected shape gets added to the canvas.


**Parent Topic:**[Custom shapes support in the Enterprise Modeling and Visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-modeling-custom-shapes.md)

