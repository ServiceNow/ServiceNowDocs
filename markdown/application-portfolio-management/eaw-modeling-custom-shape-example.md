---
title: Custom shapes example
description: Use custom shapes to represent specific elements that are unique to your organization, such as custom business processes, systems, or roles.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Working with custom shapes, Working with Enterprise Modeling and Visualization, Manage, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
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

        ![Upload an image to the database](../../image/eaw-image/modeling/custom-shapes-upload-image.jpg)

    2.  Select **New**.

        ![Create new image record](../../image/eaw-image/modeling/new-image-record.jpg)

2.  In the New image record, enter the name of the image file \(include file format extension\) and fill in other details.

3.  Select **Click to add...**.

    ![Uploading a custom shape to the database](../../image/eaw-image/modeling/custom-shape-new-image-record.jpg)

4.  Create a diagram action for the image in the Enterprise Architecture Workspace.

    1.  Log in as an APM admin user \(sn\_apm.apm\_admin\), navigate to the **Setup** section.

    2.  Under the **Enterprise Modeling and Visualization** section, select **Diagram Actions**.

        ![Diagram action](../../image/eaw-image/modeling/custom-shape-diagram-action.jpg)

    3.  Select New to create a diagram action for the image \(Database.svg\).

    4.  In the Diagram Action form, enter the following details:

        -   Name- Name for the diagram action
        -   Diagram builder configuration- Select APM diagram configuration from the list
        -   Node type- Select node type as ‘Image node container'
        -   Category- Select Default
        -   Sub category- Select Default sub category
        -   Icon- Enter name of the image
        ![Diagram action form](../../image/eaw-image/modeling/custom-shape-diagram-action-form.jpg)

5.  Create a custom shape library specific to your Org to add all the shapes to create diagrams for your organization.

    1.  As an APM Admin user, navigate to **Setup** &gt; **Enterprise Modeling and Visualization** &gt; **Shape Libraries**.

        ![Shape libraries section](../../image/eaw-image/modeling/custom-shape-libraries.jpg)

    2.  Select **New**.

    3.  Enter a name for the shape library, then select **Save**.

        ![New shape library form](../../image/eaw-image/modeling/custom-shape-new-library.jpg)

6.  Add a shape library element to associate the shape and its diagram action to the shape library.

    1.  As an APM Admin user, open the shape library you have created in the previous step.

    2.  Select the **Shape Library Elements** tab.

    3.  Select **New**.

        ![Shape library element](../../image/eaw-image/modeling/custom-shape-library-element.jpg)

    4.  In the Shape library element form, enter the following details:

        -   Tool tip- Enter text that you want to see on hovering the image.
        -   Diagram action- Select the diagram action that you have created in the previous step.
        -   Now icon- Enter the name of the shape or image.
        -   Name- Enter a name for the shape to be displayed in the Enterprise Modeling and Visualization application.
        -   Shape library- This field is automatically selected.
        -   Domain- Optional field.
        -   Entity configuration- Optional field.
        ![Shape library element form](../../image/eaw-image/modeling/custom-shape-library-element-form.jpg)

    5.  Select **Save**.

7.  Create a diagram using the shape uploaded.

    1.  Navigate to **Enterprise Modeling and Visualization** page.

    2.  Select &gt; **New** &gt; **Blank diagram**

        ![Create a blank diagram](../../image/eaw-image/modeling/custom-shape-blank-diagram.jpg)

    3.  Enter a name for the diagram and optionally, you can enter or select an existing architectural category for the diagram.

        ![Create blank diagram modal](../../image/eaw-image/modeling/custom-shape-create-diagram.jpg)

        Observe that the shape library that you created appears in the Shapes pallet. It contains the shape that you uploaded.

    4.  Click on the shape to add it to the canvas.

        ![Adding a custom shape to the canvas](../../image/eaw-image/modeling/custom-shape-add-to-canvas.jpg)

        The selected shape gets added to the canvas.


**Parent Topic:**[Working with custom shapes](../../concept/eaw-concept/eaw-working-custom-shapes.md)

**Related topics**  


[Storing shapes or images to the database](eaw-modeling-store-image-databse.md)

[Create a diagram action for a custom shape](eaw-modeling-action-custom-shape.md)

[Add a custom shape library](eaw-modeling-add-custom-shape-library.md)

[Add a shape library element for a custom shape](eaw-modeling-custom-shape-element.md)

