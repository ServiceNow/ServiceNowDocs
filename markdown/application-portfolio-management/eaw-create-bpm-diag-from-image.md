---
title: Create a business process map diagram from an image
description: Upload an image of an existing process diagram to generate a new, editable business process map diagram in EA Workspace using the ServiceNow AI Lens Now Assist skill.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-create-bpm-diag-from-image.html
release: australia
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 3
breadcrumb: [Use Now Assist, Now Assist for Enterprise Architecture \(EA\), Enterprise Architecture]
---

# Create a business process map diagram from an image

Upload an image of an existing process diagram to generate a new, editable business process map diagram in EA Workspace using the ServiceNow AI Lens Now Assist skill.

## Before you begin

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

Verify the following conditions are met:

-   The source image is in PNG or JPEG format and does not exceed 1 MB.
-   Role required: sn\_apm.apm\_user

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Modeling page by selecting the Enterprise Modeling and Visualization icon \(\[Omitted image "icon-modeling-logo.png"\] Alt text: Modeling\).

3.  Select **Import image**.

    \[Omitted image "create-diag-modal.png"\] Alt text: Import image to create diagram dialog, showing a drag-and-drop upload area, Link to business process field, Business process name field, and Artifact name field.

4.  In the Import image to create diagram pop-up window, under **Create diagram from image**, select **Add file** and select your source image file.

    Max file size: 1 MB; Supported formats: PNG and JPEG.

5.  From the **Link to business process** drop-down, select **New** to create business process, or select an existing business process.

6.  Enter values for **Business process name** and **Artifact name**.

    **Note:** The artifact name is automatically populated from the **Business process name**.

7.  Select **Create diagram**.

    An Importing image dialog appears. If the request fails or times out, an error message is displayed inside this dialog and you can retry. On success, the diagram canvas opens.

    The canvas opens showing:

    -   The generated diagram in the upper pane with shapes, pools, lanes, and connections identified from the image.
    -   The uploaded source image in the lower pane for reference. To resize the panes, drag the divider between them.
    -   An **AI converted diagram** badge in the canvas header.
    -   A **Shapes with low confidence scores** list in the canvas banner, if any shapes were identified with a confidence score below 70%. Affected shapes are marked with an orange border on the canvas.
    -   **Accept** and **Discard** buttons at the top right of the canvas.
    \[Omitted image "create-diag-output.png"\] Alt text: Screenshot comparing an AI-generated BPM diagram in the upper pane and the uploaded source image in the lower pane.

    **Note:** The **Share** button, **Show Version**, and the more actions menu are hidden while the diagram is in review state.


## What to do next

Review and accept the generated diagram. For instructions, see [Review and accept a Now Assist-generated business process map diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-review-ai-generated-bpm-diag.md).

**Parent Topic:**[Using Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/using-now-assist-for-ea.md)

**Related topics**  


[Business process map diagrams from images](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-bpm-diagram-from-image.md)

[Review and accept a Now Assist-generated business process map diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-review-ai-generated-bpm-diag.md)

[ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens-landing-page.md)

[Configure ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-sn-lens.md)

[Replace a shape in a diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-modeling-replace-shape.md)

