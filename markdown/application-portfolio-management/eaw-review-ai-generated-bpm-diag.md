---
title: Review and accept a Now Assist-generated business process map diagram
description: After ServiceNow AI lens generates a business process map \(BPM\) diagram from an uploaded image, review the diagram and resolve any low-confidence shapes, and accept or discard it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-review-ai-generated-bpm-diag.html
release: australia
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 5
breadcrumb: [Use Now Assist, Now Assist for Enterprise Architecture \(EA\), Enterprise Architecture]
---

# Review and accept a Now Assist-generated business process map diagram

After ServiceNow AI lens generates a business process map \(BPM\) diagram from an uploaded image, review the diagram and resolve any low-confidence shapes, and accept or discard it.

## Before you begin

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Before you begin

An AI-generated business process map diagram exists in review state. For instructions on creating a diagram from an image, see [Create a business process map diagram from an image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-create-bpm-diag-from-image.md).

Role required: sn\_apm.apm\_user

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Modeling page by selecting the Enterprise Modeling and Visualization icon \(\[Omitted image "icon-modeling-logo.png"\] Alt text: Modeling\).

3.  Open the BPM diagram that is in review state.

    The canvas header displays an **AI converted diagram** badge. The upper pane shows the generated diagram and the lower pane shows the uploaded source image. The **Accept** and **Discard** buttons are visible at the top right. \[Omitted image "create-diag-output.png"\] Alt text: Screenshot comparing an AI-generated BPM diagram in the upper pane and the uploaded source image in the lower pane.

    **Note:** The **Share** button, **Show Version**, and the more actions menu are hidden until the diagram is accepted.

4.  Verify that shapes, pools, lanes, and connections are correctly identified by comparing the generated diagram in the upper pane against the source image in the lower pane.

    Check the following:

    -   Node accuracy: Confirm shape types and names match the source image. AI Lens extracts names from the image text.
    -   Events, gateways, and activities: Confirm that event, gateway, and activity shapes from the image are correctly represented with the corresponding shape types in the diagram.
    -   Edge accuracy: Confirm connections between shapes are correctly placed and that any labels on those connections are correctly captured.
    -   Pools and lanes: Confirm the number of pools and lanes in the diagram matches the source image.
    -   Grouping: Confirm shapes that were grouped in the source image are also grouped on the canvas. You can resize pools and lanes by dragging their borders.
    -   Generic rectangles: Shapes that AI Lens could not match to a known type in the shape library appear as generic rectangles. Identify the intended shape type and replace them using the **Shape Type** drop-down in the **Data** panel.
5.  To replace a shape with a different type, select the shape on the canvas and then select the open the side panel icon \(\[Omitted image "icon-open-side-panel.png"\] Alt text: Open side panel\).

    The **Data** panel is diplayed.

6.  In the **Shape Type** field, open the drop-down and select the correct shape type from the list.

    The shape updates to the selected type. All existing connections to the shape and their labels are retained.

7.  To update the ServiceNow® record a shape is linked to without changing its shape type, perform the following: select the shape to open its **Data** panel, then use **Choose Existing** to link it to a different existing record, or **Create new** to stage a new record.

    1.  Select the shape on the canvas and then select the open the side panel icon \(\[Omitted image "icon-open-side-panel.png"\] Alt text: Open side panel\).
    2.  Select **Choose Existing** to link it to a different existing record.
    3.  Select **Create new** to link to an existing record.
    This allows you to correct entity links independently of shape types.

8.  If the **Shapes with low confidence scores** drop-down is visible in the canvas banner, select it to view the list of shapes identified with a low confidence score.

    Affected shapes are marked with an orange border on the canvas. Select each affected shape to open its **Data** panel, then take one of the following actions:

    -   Change the **Shape Type** in the **Data** panel to the correct type. The orange border is removed and the low-confidence count in the banner disappears.
    -   Select **Accept** to accept all AI-generated shapes as-is and clear all low-confidence indicators at once.
9.  Verify entity sync for shapes that represent records, by selecting each shape and checking the **Data** panel.

    -   **Choose Existing**: AI Lens found a matching record in the corresponding database table and linked the shape to it automatically.
    -   **Create new**: No matching record was found. A temporary record is staged for the shape and will be committed following the standard approval workflow for that table, provided you have the appropriate permissions for that table.
    **Note:** Users without access to create records in a given database table will not have new records committed for the corresponding shapes, even after accepting the diagram.

10. When satisfied with the diagram, take one of the following actions:

    -   To accept the diagram, select **Accept** at the top right of the canvas.

        The diagram transitions to draft state and the reference image pane closes. New records staged during diagram generation are committed following the standard approval workflow for the respective tables.

    -   To permanently delete the diagram, select **Discard** at the top right of the canvas. On the Discard Review dialog box, select **Discard** to confirm.

        **Important:** Discarding an AI-generated diagram deletes the diagram, all associated versions, the artifact, and the uploaded image. You're returned to the diagrams list view. This action can't be undone.


## What to do next

After accepting, the diagram is in draft state and behaves as any other diagram in EA Workspace. The **Share** button, **Show Version**, and the more actions menu are restored. You can share the diagram with other users, associate it with an architectural artifact, and continue editing it as needed.

**Parent Topic:**[Using Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/using-now-assist-for-ea.md)

**Related topics**  


[Business process map diagrams from images](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-bpm-diagram-from-image.md)

[Create a business process map diagram from an image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-create-bpm-diag-from-image.md)

[ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens-landing-page.md)

[Configure ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-sn-lens.md)

