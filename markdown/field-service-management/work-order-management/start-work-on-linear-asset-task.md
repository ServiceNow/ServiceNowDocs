---
title: Start work on a linear asset task
description: Examine the linear asset specified in the work order task to pinpoint or select segments or areas in need of attention or maintenance, and generate a corresponding work order.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Linear assets, ServiceNow Agent mobile app, Completing work on mobile, Use, Field Service Management]
---

# Start work on a linear asset task

Examine the linear asset specified in the work order task to pinpoint or select segments or areas in need of attention or maintenance, and generate a corresponding work order.

## Before you begin

Ensure the following setup:

-   The work order task is either in the **Work In Progress** or **Accepted** state.
-   Enable location tracking from your mobile device to record your location in the geo history table. For more information, see [Using location tracking for mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-location.md).

Role required: wm\_agent

## Procedure

1.  Navigate to the ServiceNow Agent application.

2.  Tap **My Work**.

3.  In the **My Tasks** section, display all the work order tasks by selecting **See All**.

4.  Select and open the desired work order task.

5.  View the linear asset segments to be inspected by tapping the **Related** tab and going to the **Assets** section.

    Each segment displays the asset name and a sequential number along with the start and location details.

6.  On the segment that you want to start inspecting, tap **Start Work**.

7.  Open the asset page and review the asset details by tapping the selected segment.

8.  View the linear asset segment on the map by tapping the Google Maps launcher icon \(![Google Maps launcher icon](../image/mab-icon-launch-weblink-sol.png)\) in the Start location field.

    The map launches and the linear asset location is displayed. The linear segment is highlighted in dark blue color for better identification.

9.  Provide additional information about the affected linear asset by tapping **Take questionnaire**.

    For more information, see [Complete a questionnaire for a work order task](complete-questionnaire-mobile-app.md).

10. If you identify an issue for a linear asset when inspecting a segment, create a new work order.

    1.  Tap **Create Work Order**.

    2.  Provide additional information related to the identified issue by uploading an attachment such as photo, image, or document in the **Add attachment** field.

    3.  On the form, fill in the fields.

<table id="id_tjz_rdc_b1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Location

</td><td>

The live location of the agent.This field is auto-populated with the agent's current location.

</td></tr><tr><td>

Lat long

</td><td>

The latitude and longitude for the marker.This field is automatically populated with the latitude and longitude value of the agent current location. You can edit these values if required.

</td></tr><tr><td>

Asset

</td><td>

List of linear asset segments linked to the work order task.

</td></tr><tr><td>

Issue

</td><td>

Descriptive name for the issue. For example, a pothole on the road.

</td></tr><tr><td>

Issue Description

</td><td>

Detailed description of the issue.

</td></tr></tbody>
</table>    4.  Select **Submit**.

11. Tap **Mark Complete**.

12. Inspect more segments by repeating the steps starting with step 6.


## Result

You have successfully inspected the selected linear asset segments in a work order task and created corresponding work orders for any segments requiring attention or maintenance.

