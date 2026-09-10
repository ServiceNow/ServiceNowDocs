---
title: Auto-fill a form with ServiceNow AI Lens
description: Use ServiceNow AI Lens to auto-fill form fields by capturing or uploading an image in the ServiceNow Agent mobile app. The Lens Launcher is available on Input Forms and Scripted Input Forms, such as Smart Assessment questionnaires.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/work-order-management/t\_use-form-auto-filler-fsm.html
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-05-11"
reading_time_minutes: 2
keywords: [ServiceNow Lens, Lens Launcher, auto-fill, Form Auto-Filler, Smart Assessment, Input Form, mobile]
breadcrumb: [ServiceNow AI Lens form auto-filler, Prioritizing on ServiceNow Agent, ServiceNow Agent mobile app, Completing work on mobile, Use, Field Service Management]
---

# Auto-fill a form with ServiceNow AI Lens

Use ServiceNow AI Lens to auto-fill form fields by capturing or uploading an image in the ServiceNow Agent mobile app. The Lens Launcher is available on Input Forms and Scripted Input Forms, such as Smart Assessment questionnaires.

## Before you begin

Role required: wm\_agent, which inherits the lens\_user role.

## About this task

Auto-filling a form with ServiceNow AI Lens reduces manual data entry on a job site. Capture an image of an asset, document, or equipment, and ServiceNow AI Lens populates the relevant form fields from the image.

**Note:** Review AI-populated form fields for accuracy before submitting. AI-generated results may not be accurate in all cases.

These steps cover filling a Smart Assessment questionnaire for a work order task. The same steps apply when using ServiceNow AI Lens Launcher to fill Input Forms and Scripted Input Forms.

## Procedure

1.  Log in to the ServiceNow Agent mobile application.

2.  Select **My Work**.

3.  In the **My Tasks** section, select **See All**.

4.  Select the required task.

5.  Select **Start work**.

6.  Select **Take questionnaire**.

    The questionnaire associated with the work order task is displayed.

7.  Select the questionnaire to start filling it.

8.  Select the Lens icon \[Omitted image "use-form-auto-filler-fsm.png"\] Alt text: in the toolbar.

9.  In the **Add files** section, select the file to scan, such as an image, from your local device.

    You can add multiple files to be scanned at once, but the limit is 10.

10. Select the Camera icon \[Omitted image "form-auto-filler-fsm-upload.png"\] Alt text: to capture an image with your device camera and add it for scanning.

11. Select **Add** to directly add the files for scanning or **View selected** to review the files before adding.

12. After the files are added, in the ServiceNow AI Lens page, select **Start**.


## Result

After the files are successfully scanned, some of the fields in the questionnaire are automatically filled. You can review the values and edit them, if required.

## What to do next

If ServiceNow AI Lens cannot process the image, one of the following error messages appears:

<table id="table_lhg_55j_kjc"><thead><tr><th>

Scenario

</th><th>

Error or warning

</th></tr></thead><tbody><tr><td>

The Lens Launcher icon is unavailable in the Smart Assessment questionnaire.

</td><td>

No error message.To resolve this, ensure that all the necessary plugins are active. After activating them, relaunch the questionnaire.

</td></tr><tr><td>

The Lens Launcher icon is available, but displays an error.

</td><td>

An error message is displayed when the icon is selected.To resolve this, ensure that the ServiceNow AI Lens AI lens skill is enabled by navigating to **Now Assist Skill Admin** &gt; **Platform Skills**, and relaunch the questionnaire.

</td></tr></tbody>
</table>**Related topics**  


[ServiceNow AI Lens form auto-filler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/c_form-auto-filler-fsm.md)

[Use ServiceNow AI Lens in ServiceNow Otto Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/t_use-lens-nava-fsm.md)

[Smart Assessment questionnaires](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/smart-assessment-questionnaire.md)

[Configuring Smart Assessment questionnaires for Now Mobile Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/mobile-experience-for-field-service-management-glide-family/configuring-smart-assessment-questionnaire.md)

