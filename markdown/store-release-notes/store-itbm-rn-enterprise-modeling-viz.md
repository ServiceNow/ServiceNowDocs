---
title: Enterprise Modeling and Visualization release notes
description: Version history for the Enterprise Modeling and Visualization application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-enterprise-modeling-viz.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - Enterprise Architecture release notes, ServiceNow Store release notes]
---

# Enterprise Modeling and Visualization release notes

Version history for the Enterprise Modeling and Visualization application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.2.2 - June 2026 \(Australia\)**
    -   New:
        -   Generate a business process map \(BPM\) diagram in the Enterprise Modeling &amp; Visualization by uploading an image of an existing process diagram.
        -   Replace an existing shape in a modeling diagram with a different shape type
        -   Preview shapes in the Shapes panel by hovering over a shape icon or navigating with arrow keys. A popover appears to the right of the panel showing a larger view of the shape and its label
        -   The width of the right side panel on the modeling diagram canvas is saved as a user preference and persists across sessions
        -   The BPMN shape library is expanded with shapes conforming to the BPMN 2.0 standard
            -   Events- expanded from 3 to 56 shapes
            -   Gateways- include new types
            -   Activities- include new task types and call activity shapes
    -   Align two or more selected shapes to a common edge or center using the alignment options on the diagram toolbar. Distribute three or more selected shapes at equal horizontal or vertical spacing.
    -   Customize connector properties in modeling diagrams using the connector toolbar. You can:
        -   Choose source or destination arrowheads
        -   Select line type - solid or dashed, or dotted
        -   Select icons to be displayed on connector lines
-   **Version 6.2.0 - June 2026 \(Zurich\)**
    -   New:
        -   Replace an existing shape in a modeling diagram with a different shape type
        -   Preview shapes in the Shapes panel by hovering over a shape icon or navigating with arrow keys. A popover appears to the right of the panel showing a larger view of the shape and its label
        -   The width of the right side panel on the modeling diagram canvas is saved as a user preference and persists across sessions
        -   The BPMN shape library is expanded with shapes conforming to the BPMN 2.0 standard
            -   Events- expanded from 3 to 56 shapes
            -   Gateways- include new types
            -   Activities- include new task types and call activity shapes
    -   Align two or more selected shapes to a common edge or center using the alignment options on the diagram toolbar. Distribute three or more selected shapes at equal horizontal or vertical spacing.
    -   Customize connector properties in modeling diagrams using the connector toolbar. You can:
        -   Choose source or destination arrowheads
        -   Select line type - solid or dashed, or dotted
        -   Select icons to be displayed on connector lines
-   **Version 6.1.2 - May 2026 \(Australia\)**

    Fixed: The Architecture Analyzer L1 menu was visible, but the page failed to load.

-   **Version 6.1.1 - May 2026 \(Zurich\)**

    Fixed: The Architecture Analyzer L1 menu was visible, but the page failed to load.

-   **Version 6.1.0 - April 2026**

    New: The new and modified shapes and relationship lines are highlighted on the canvas on comparing two versions of Enterprise Modeling and Visualization diagrams using the diagram change analysis Now Assist skill.

-   **Version 6.0.0 - March 2026**
    -   New:
        -   Generate documents from diagrams using templates with dynamic content.
        -   View all documents generated from diagrams.
        -   Compare any two diagram versions and generate detailed diagram change summary.
        -   Support for new ArchiMate shapes \(OR Junction, AND Junction, Deliverable, Implementation Event, Work Package, Gap, Plateau, Location and General Group\).
        -   Support for multiple labels on a single connector line between shapes.
        -   Added support for Architecture Analyzer.
    -   Changed:
        -   Support for keyboard navigation on all diagram context menu items inside the canvas, and the shapes panel on a diagram page.
        -   Support for screen reader on all diagram context menu items inside the canvas, and the shapes panel on a diagram page.
        -   Edit shape name on a single click.
        -   Supports up to 400% zoom level on the right side panel of the Enterprise Modeling and Visualization diagram page.
        -   Canvas no longer shifts when dropping or selecting shapes.
        -   Support for i18n translations for all canvas and panel tooltips.
    -   Fixed:
        -   Fixed a bug where a swimlane in the BPMN diagram was distorted on dropping new shapes.
        -   Fixed a bug where a swimlane in the BPMN diagram was not auto-expanding on dropping new shapes.
        -   Fixed a bug where the right side panel was displaying a loading state while adding a capability shape to the capability hierarchy diagram.
        -   Fixed padding and cross-button alignment in right side panel on the canvas.
        -   Fixed tooltip display issues on CSDM shapes.
        -   Fixed a bug where the search feature was stuck when typing in the Choose existing search box on the Business capability hierarchy diagram page.
        -   Fixed a bug where a diagram was not displayed in the display theme as selected by the user.
        -   Fixed the add related record behaviour to fetch correct shapes based on Entity and Entity Condition from the Entity Configurations table.
-   **Version 5.0.2 - January 2026**

    Enhanced AI Skill Stability: Improved the reliability of AI-powered features to ensure a smoother experience.

-   **Version 5.0.0 - December 2025**
    -   New:
        -   Improved visual appearance of all enterprise modeling shapes by adding:
            -   Color styling
            -   Refined dimensions
            -   Improved icons
            -   Better content positioning inside shapes
        -   Introduced AI Inventory Product Model entities within CSDM shape library
            -   AI Dataset Product Model
            -   AI Model Product Model
            -   AI Prompt Product Model
            -   AI System Product Model
        -   Enhanced shape library panel. The left-side panel for shape libraries now includes:
            -   Improved icon dimensions and color styling
            -   Sub-libraries for better categorization \(as applicable\)
            -   User-configurable library reordering
            -   Expand or collapse options for each library
            -   Toggle between Grid View and List View for improved usability
            -   Collapsible left panel: Users can now show or hide the entire left-side panel for a cleaner design workspace
        -   Improved drag-and-drop experience: Dragging shapes from the left panel to the canvas now shows an object that matches the actual size, shape, and color of the final element for placement onto the canvas
        -   Added AWS standard shapes and AWS group shapes to support aws cloud architecture modeling
        -   Updated the existing Enterprise Architecture shape library and aligned the shapes associated with CSDM 5 standards
        -   Enhanced general shapes to support grouping behavior \(except shapes such as Junction, Sticky Notes, Text Box, Actor\)
            -   Switch between normal and groupable shape modes
            -   Add other shapes or entities inside a group shape
            -   Expand or collapse  a group shape
        -   Improved new entity creation flow:
            -   Create new entities entering only the display name
            -   Fill in the mandatory fields on the entity form while committing the diagram
        -   Enhanced early error detection
            -   After submitting a diagram for approval:
                -   Shapes with errors are highlighted with a red border and an error icon
                -   Update the shape content to resolve errors
            -   After approval:
                -   A new error summary dropdown in the top-right header shows the number of shapes which have errors
                -   Select a shape from the errors list to open its content in the side panel to update the details
        -   Business process details on Business Process Diagram
            -   Added Modify business process details icon on the header of the business process diagram to view and update business process details
        -   Enhanced capability map auto-resizing
            -   Capability maps now automatically resize based on canvas area and zoom level. This helps in optimal use of space, better content visibility, and improved readability
        -   Export diagram as an image file: Download diagrams directly as image files and use them for sharing and documentation
        -   Enhanced the right-hand side panel to allow resizing
    -   Removed: Existing Enterprise Architecture Shape library is removed. All those shapes are now part of CSDM and EA Extended shape libraries.
-   **Version 4.1.0 - August 2025**
    -   New:
        -   Undo and redo your recent actions on the diagram canvas
        -   Associate both upstream and downstream entities for a shape using the Add related records action.
        -   Drag and drop shapes from the shapes palette to the canvas
        -   Add text to the relationship lines between shapes
        -   Resize all shapes. The minimum size represented by an icon
        -   Business process shape added under the Enterprise Architecture category in the shapes palette on the diagram page
        -   AI Dataset Digital Asset, AI Model Digital Asset, AI Prompt Digital Asset, and AI System Digital Asset shapes added under the Enterprise Architecture category in the shapes palette on the diagram page
        -   Delete diagrams directly from the Enterprise Modeling and Visualization home page. It removes the artifact and all associated versions
    -   Changes:
        -   Enhanced overall BPMN diagram usability
        -   Duplicate BPMN diagrams and associate them with existing or new business processes
        -   Add description, label, and target date while creating new versions
-   **Version 4.1.1 - August 2025**

    Updates to the diagram builder dependency to version 28.0.2. This ensures the compatibility with the ServiceNow Platform versions such as Yokohama and Zurich.

-   **Version 4.0.1 - June 2025**
    -   Fixed:
        -   When a new shape is added to the business capability map while a business capability shape is already selected, it will be placed as a sibling of the selected shape.
        -   Issue where diagrams were not created for capabilities without a hierarchy ID.
        -   Out-of-the-box \(OOB\) shapes such as ArchiMate shapes are restricted for editing.
        -   Issue where a business capability did not appear on the canvas when creating a business hierarchy map when both value stream and project entities were related to the same capability.
        -   Issue where the Add Related Records feature briefly displayed outdated values before updating to the current ones.
        -   Issue where the sticky notes were not being added to the canvas in the business hierarchy map.
-   **Version 3.2.0 - February 2025**
    -   New:
        -   Blank diagram option is added in the New diagram drop-down menu on the Enterprise Modeling and Visualization home page
        -   Read access is granted to the sn\_apm.apm\_read role
    -   Fixed:
        -   General shapes resizing and rotation issues are fixed
        -   Security issues are fixes
-   **Version 3.1.0 - November 2024**
    -   New:
        -   Support for Business capability map
        -   Support for industry-standard ArchiMate shapes and ArchiMate relationship types to create modeling diagrams. \(ArchiMate is a registered trademark of The Open Group\)
        -   Support for adding related records \(CI relationships or references\) for a business hierarchy map within the diagram
        -   Support for new link types between CSDM and ArchiMate shapes
        -   Apply colors to business capability shapes in the capability hierarchy map
        -   Support for initiating modeling directly from the ServiceNow Unified map using the Enterprise Modeling and Visualization
-   **Version 2.0.0 - August 2024**
    -   The Enterprise Modeling and Visualization functionality in Enterprise Architecture Workspace helps you with diagramming and modeling capabilities. It enables you to model the future state of your IT business applications to assess the impact of proposed business application changes, evaluate different scenarios, and identify potential risks before implementing application strategies.
    -   For existing business applications, you can create business application hierarchy diagrams and save them as an existing architectural artifact or a new one.
    -   You can create diagrams to determine complex enterprise application structures, processes, and their relationships.

