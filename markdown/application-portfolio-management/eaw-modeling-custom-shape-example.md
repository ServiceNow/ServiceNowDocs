---
title: Custom shapes example
description: Use custom shapes to represent specific elements that are unique to your organization, such as custom business processes, systems, or roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-modeling-custom-shape-example.html
release: australia
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 6
breadcrumb: [Working with custom shapes, Working with Enterprise Modeling and Visualization, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Custom shapes example

Use custom shapes to represent specific elements that are unique to your organization, such as custom business processes, systems, or roles.

## Before you begin

Roles required: System Administrator \(to upload images to the database\), sn\_apm.apm\_admin \(to create diagram actions, entity configurations, custom shape library, and add shape library elements\), sn\_apm\_mdtl\_com.mdtl\_com\_admin \(to create reference relationships\).

## About this task

In this example, you will learn how to upload an image or shape to the database, create a diagram action for the image or shape, create an entity configuration, create a custom shape library, add a shape library element that maps the shape to the entity configuration, create a reference relationship between entities, and create a diagram using the shapes.

Create the shapes that represent the elements you want to include in your diagrams. Ensure the images are clear, simple, and visually distinct. The compatible format is .SVG. In this example, we use the 'Database.svg' image.

**Tip:** To display a properties side panel when a shape is selected on the canvas, you must set the node type to **CI Item** in the diagram action, create an entity configuration for the target table, and map the entity configuration to the shape library element. Steps 4, 5, and 7 in this example cover this workflow.

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

        -   Name — Name for the diagram action.
        -   Diagram builder configuration — Select APM diagram configuration from the list.
        -   Node type — Select **CI Item** if you want the shape to display a properties side panel showing data from a platform entity when selected on the canvas. Select **Image node container** if you want the shape to be a standalone visual element with no entity data.
        -   Category — Select Default.
        -   Sub category — Select Default sub category.
        -   Icon — Enter name of the image.
        \[Omitted image "custom-shape-diagram-action-form.jpg"\] Alt text: Diagram action form

5.  Create an entity configuration to link the shape to a platform entity table.

    An entity configuration defines the platform table that the shape represents. When you map an entity configuration to a shape library element, selecting the shape on the canvas opens a properties side panel that shows field data from the corresponding entity record. This step is required if you set the node type to **CI Item** in the previous step.

    For field information, see [Entity configuration form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-entity-config-form.md).

    1.  Open the Setup page by selecting the Setup icon \(\[Omitted image "eaw-icon-setup.png"\] Alt text: setup icon.\).

    2.  Select the expand row icon \(\[Omitted image "ExpandIcon.png"\] Alt text: expand row icon.\) next to **Enterprise Modeling and Visualization**.

    3.  Select **Entity Configurations**.

    4.  Select **New**.

    5.  On the Entity Configuration form, fill in the fields.

        -   Name — Enter a name for the entity configuration. For example, `Epic`.
        -   Entity — Select the platform table that this entity represents. For example, `rm_epic` for Epics.
        -   Display field — Enter the field name to display in the Enterprise Modeling and Visualization. For example, `name`.
        -   Diagram action — Select the diagram action that you created in step 4.
    6.  Select **Save**.

6.  Create a custom shape library specific to your Org to add all the shapes to create diagrams for your organization.

    1.  As an APM Admin user, navigate to **Setup** &gt; **Enterprise Modeling and Visualization** &gt; **Shape Libraries**.

        \[Omitted image "custom-shape-libraries.jpg"\] Alt text: Shape libraries section

    2.  Select **New**.

    3.  Enter a name for the shape library, then select **Save**.

        \[Omitted image "custom-shape-new-library.jpg"\] Alt text: New shape library form

7.  Add a shape library element to associate the shape and its diagram action to the shape library.

    1.  As an APM Admin user, open the shape library you have created in the previous step.

    2.  Select the **Shape Library Elements** tab.

    3.  Select **New**.

        \[Omitted image "custom-shape-library-element.jpg"\] Alt text: Shape library element

    4.  In the Shape library element form, enter the following details:

        -   Tool tip — Enter text that you want to see on hovering the image.
        -   Diagram action — Select the diagram action that you created in step 4.
        -   Now icon — Enter the name of the shape or image.
        -   Name — Enter a name for the shape to be displayed in the Enterprise Modeling and Visualization.
        -   Shape library — This field is automatically selected.
        -   Domain — Optional field.
        -   Entity configuration — Select the entity configuration that you created in step 5. This field is required if you set the node type to **CI Item** in step 4. Selecting an entity configuration maps this shape to the corresponding platform entity table so that the properties side panel is displayed when the shape is selected on the canvas.
        \[Omitted image "custom-shape-library-element-form.jpg"\] Alt text: Shape library element form

    5.  Select **Save**.

8.  Create a reference relationship between the entities to enable the shape to reference and retrieve entity records on the canvas.

    A reference relationship defines how the entity associated with the custom shape relates to other entities in the platform. This step is required if you set the node type to **CI Item** in step 4.

    For field information, see [Relationship configuration form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-relationship-form.md).

    1.  Open the Setup page by selecting the Setup icon \(\[Omitted image "eaw-icon-setup.png"\] Alt text: setup icon.\).

    2.  Select the expand row icon \(\[Omitted image "ExpandIcon.png"\] Alt text: expand row icon.\) next to **Enterprise Modeling and Visualization**.

    3.  Select **Relationships**.

    4.  Select **New**.

    5.  On the Relationship form, fill in the fields.

        -   Relationship Type — Select **Reference**.
        -   Base Entity — Select the entity that is the source of the relationship. For example, the entity representing the custom shape you created.
        -   Base Reference — Define the reference field on the base entity table.
        -   Related Entity — Select the entity that the base entity relates to.
        -   Base Entity Configuration — Select the entity configuration that you created in step 5.
    6.  Select **Save**.

9.  Create a diagram using the shape uploaded.

    1.  Navigate to **Enterprise Modeling and Visualization** page.

    2.  Select &gt; **New** &gt; **Blank diagram**

        \[Omitted image "custom-shape-blank-diagram.jpg"\] Alt text: Create a blank diagram

    3.  Enter a name for the diagram and optionally, you can enter or select an existing architectural category for the diagram.

        \[Omitted image "custom-shape-create-diagram.jpg"\] Alt text: Create blank diagram modal

        Observe that the shape library that you created appears in the Shapes pallet. It contains the shape that you uploaded.

    4.  Click on the shape to add it to the canvas.

        \[Omitted image "custom-shape-add-to-canvas.jpg"\] Alt text: Adding a custom shape to the canvas

        The selected shape gets added to the canvas. If you configured the node type as **CI Item** and mapped an entity configuration to the shape library element, select the shape and then select the **Info** icon on the right side of the canvas to display the properties side panel showing entity record data.


**Parent Topic:**[Working with custom shapes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-working-custom-shapes.md)

**Related topics**  


[Storing shapes or images to the database](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-store-image-databse.md)

[Create a diagram action for a custom shape](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-action-custom-shape.md)

[Add a custom shape library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-add-custom-shape-library.md)

[Add a shape library element for a custom shape](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-custom-shape-element.md)

[Add or edit an entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-add-edit-entity.md)

[Add or edit a relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-add-edit-relationship.md)

