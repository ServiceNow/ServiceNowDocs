---
title: Business process map diagrams from images
description: Use the ServiceNow AI lens skill to generate a business process map \(BPM\) diagram automatically by uploading an image of an existing process diagram from any tool.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-bpm-diagram-from-image.html
release: australia
topic_type: concept
last_updated: "2026-05-13"
reading_time_minutes: 6
breadcrumb: [Explore, Now Assist for Enterprise Architecture \(EA\), Enterprise Architecture]
---

# Business process map diagrams from images

Use the ServiceNow AI lens skill to generate a business process map \(BPM\) diagram automatically by uploading an image of an existing process diagram from any tool.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

\[Omitted image "create-diag-output.png"\] Alt text: Screenshot comparing an AI-generated BPM diagram in the upper pane and the uploaded source image in the lower pane.The image-to-diagram feature in EA Workspace uses the ServiceNow AI Lens platform Now Assist skill to analyze an uploaded image of a business process and re-create it as a native, editable BPM diagram. This removes the need to manually rebuild diagrams that already exist in other tools.

When you upload an image, AI Lens identifies shapes, pools, lanes, gateways, and the connections between them. It maps recognized shapes to entities in your instance where matching records exist, and creates new records for shapes it can't find a match for, provided you have the appropriate permissions for the tables associated with those shapes. The generated diagram opens in a review state so you can validate, adjust, and then commit it.

**Note:** Image upload is available only when creating a business process map diagram. The **Import image** option is not shown for blank, business application hierarchy, or business capability map diagram types.

## In review state

An AI-generated diagram remains in Review state until you accept or discard it. While in this state:

-   The canvas header displays an **AI converted diagram** badge.
-   The **Share** button, **Show Version**, and the more actions menu are hidden until the diagram is accepted.
-   The canvas is fully editable: you can move, resize, add, or remove shapes, change any shape type, or replace a shape with a different shape.

Selecting **Accept All** transitions the diagram to draft state and closes the reference image pane. New records staged during diagram generation are committed following the standard approval workflow for the respective tables. Selecting **Discard** permanently deletes the diagram, all associated versions, the artifact, and the uploaded image, and returns you to the diagrams list view.

**Important:** Discarding is permanent and cannot be undone.

## Canvas layout in review state

After the diagram is generated, the canvas is divided into two panes:

-   The upper pane displays the generated diagram with all identified shapes, connections, pools, and lanes.
-   The lower pane displays the uploaded source image for reference.

Move the cursor over the divider between the two panes to reveal the **Adjust Pane** control. Drag the divider to resize either pane without overlap. After the diagram is accepted or discarded, the reference image pane closes and the canvas occupies the full area.

The shapes panel on the left is collapsed by default. Select the toggle to expand it and add shapes manually to the canvas.

## How AI Lens generates the diagram

ServiceNow AI Lens processes the uploaded image and performs the following actions:

-   Shape identification: AI Lens identifies BPMN shapes such as tasks, sub-processes, gateways, events, pools, and lanes. Shapes in the image that have no equivalent in the EA Workspace shape library are substituted with a generic rectangle on the canvas.
-   Grouping: Shapes that appear in a grouped arrangement in the source image are also grouped in the generated diagram.
-   Edge and label detection: AI Lens detects connections between shapes and any labels on those connections.
-   Entity sync: For each identified shape, AI Lens checks whether a matching record exists in the corresponding table. If a match is found, the shape is linked to that record automatically. If no match is found, a temporary record is staged for the shape, provided you have the appropriate permissions for the tables associated with those shapes. If you don't have the required permissions, records aren't created for the corresponding shapes.

The uploaded image is stored as an attachment on the architectural artifact record.

## Replacing shapes and updating linked entities

You can replace any shape on the canvas with a different shape type, or update the record a shape is linked to without changing the shape type. Select the shape to open its data panel on the canvas.

-   To change the shape type, select the **Shape Type** list and choose the correct type from the list. All existing connections and their labels are preserved after replacement.
-   To update the linked record without changing the shape type, use the **Choose Existing** or **Create** options in the **Data** panel to re-link the shape to a different record.

After a low-confidence shape is replaced, its orange border is removed and the low-confidence count in the canvas banner is reduced.

## Required Now Assist skills

The image-to-diagram feature requires two Now Assist skills to be active: the **Create diagram from image** Now Assist for Enterprise Architecture \(EA\) skill, and the ServiceNow AI Lens skill for the platform. When either skill is inactive, the **Import image** button is hidden on the Diagrams page.

-   **__Create diagram from image__ \(EA\)**

    Available under **Technology** &gt; **EA** in Now Assist Admin. This skill is active by default. To verify or reactivate, navigate to **Now Assist Admin** &gt; **Now Assist Skills**, expand **Technology**, and select **EA**. Confirm the **Create diagram from image** skill card shows **Active** status. If inactive, select **Activate skill** on the skill card. For configuration details, see [Configure Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/configure-now-assist-ea.md).

-   **ServiceNow AI Lens \(Platform\)**

    Available under **Platform** &gt; **Other** in Now Assist Admin. This skill must be activated by an administrator. AI Lens supports three AI model providers: Google Gemini, Azure OpenAI, and AWS Claude. The active provider is configured at the instance level under **Now Assist Admin** &gt; **Settings** &gt; **Manage model providers**. For more information, see [ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens-landing-page.md) and [Configure ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-sn-lens.md).


**Parent Topic:**[Exploring Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/exploring-now-assist-for-ea.md)

**Related topics**  


[Create a business process map diagram from an image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-create-bpm-diag-from-image.md)

[Review and accept a Now Assist-generated business process map diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-review-ai-generated-bpm-diag.md)

[Exploring Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/exploring-now-assist-for-ea.md)

[Configure Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/configure-now-assist-ea.md)

[ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens-landing-page.md)

[Configure ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-sn-lens.md)

