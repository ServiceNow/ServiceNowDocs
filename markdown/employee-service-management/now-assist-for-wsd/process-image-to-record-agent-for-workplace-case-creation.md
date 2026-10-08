---
title: Process image to record agent for workplace case creation
description: The Process image for new tasks workflow enables workplace users to report workplace issues by capturing and uploading images through the virtual agent interface. The system automatically analyzes the image and creates a workplace case with populated fields including short description, description, and priority.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/now-assist-for-wsd/process-image-to-record-agent-for-workplace-case-creation.html
release: brazil
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Using AI agent workflows in ServiceNow Otto for WSD, ServiceNow Otto for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Process image to record agent for workplace case creation

The Process image for new tasks workflow enables workplace users to report workplace issues by capturing and uploading images through the virtual agent interface. The system automatically analyzes the image and creates a workplace case with populated fields including short description, description, and priority.

The Process images for new tasks agentic workflow allows workplace users to quickly report workspace issues by uploading or capturing an image from ServiceNow Otto for Virtual Agent on web or ServiceNow® mobile. Users submit a photo—such as a liquid spillage, damaged furniture, or a facilities concern. This eliminates the requirement to manually enter case details.

The workflow automatically creates a well‑categorized workplace case with relevant information extracted from the image.

This workflow is a platform-shipped, base system agentic workflow available in AI Agent Studio under the Platform AI Agents and Skills scope. It is generic and supports all task and task‑extended tables. For Workplace Service Delivery, the workflow is configured to create records in the Workplace Case table. The skill configuration maps the Workplace User role to that table.

Required roles:

-   sn\_uxc\_gen\_ai.platform\_ai\_image\_processor
-   sn\_wsd\_core.workplace\_user

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**
2.  Select Process images for new tasks.

## Prerequisites and setup

To access this workflow, you must have Now Assist for Platform installed on your instance.

Users must have the **sn\_uxc\_gen\_ai.platform\_ai\_image\_processor** role to invoke the agentic workflow.

To allow users to create workplace cases from images using Now Assist for Virtual Agent, activate the Image Processor Agent and the Document and visual insights AI agent. Set the display to include Virtual Agent. This agentic workflow can't be discovered in Virtual Agent, so you must enable the individual AI agents that comprise it.

## Skill configuration

The Image Processor Agent reads a skill configuration to determine which task table to use when creating a record. Add a mapping entry that maps the Workplace User role to the Workplace Case table \(sn\_wsd\_case\_workplace\_case\).

-   Go to the Now Assist Skill Config \[sn\_nowassist\_skill\_config\] table.
-   Open the record named **Image to task config**.
-   In the Now Assist Skill Config Var Set related list, select the **Tables Mapping** configuration variable set.
-   Set the variables for the configuration type.
-   Save the Var Set.

\[Omitted image "nowassist-skill-config.png"\] Alt text:

## Define security controls

In the Define data access settings, add the necessary roles to enable reading of the tables for the records you want to create tasks on. For example, you can add the workplace user \[sn\_wsd\_core.workplace\_user\] role to the agentic workflow so that it can access case records.

## Select channels and status

-   Enable the ServiceNow Otto for Virtual Agent channel so users can trigger the workflow from the virtual agent chat.
-   Ensure the Virtual Agent is active on the portals where users will access it.

## Sample utterance

The following sequence describes the end-to-end flow from image upload to workplace case creation.

1.  Access the ServiceNow Otto for Virtual Agent on web or ServiceNow mobile app.
2.  To trigger the Process images for new tasks agentic workflow, enter `Create a workplace case from an image` or similar phrases in the ServiceNow Otto panel or on the ServiceNow mobile app to trigger the workflow.
3.  When prompted by the Image Processor Agent, upload an existing image or use your device camera to capture a photo of the workspace issue. Supported file types: JPEG, PNG.
4.  Review the AI-generated summary and the details extracted from the image.
5.  Select **Proceed** to confirm case creation.

A workplace case record is created with the **Short Description**, **Description**, and **Priority** fields populated from image analysis. The Workplace Service defaults to General Workplace Inquiry, the Requested For defaults to your user profile, and the Workplace Location defaults to your primary workplace location. The uploaded image is attached to the case record.

## AI agents used in the Process image for tasks workflow

The following table lists the agents that are part of the Process image for new tasks agentic workflow.

|Agent|Description|Role required|
|-----|-----------|-------------|
|Document and visual insights AI agent|Extracts information from images.| |
|Image Processor Agent|Analyzes the uploaded image to extract contextual details about the issue. Generates the short description, description, and priority based on the image content.| |

**Parent Topic:**[Using AI agent workflows in ServiceNow Otto for WSD](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/now-assist-for-wsd/now-assist-wsd-using-agentic-use-cases.md)

**Related topics**  


[Manage temporary space closures agentic workflow]()

[Help manage workplace reservations agentic workflow]()

[Optimize cleaning activities agent overview]()

[Automate map updates agentic workflow]()

[Workplace Concierge agentic workflow]()

[Implement Autonomous L1 Agent for Workplace]()

