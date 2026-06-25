---
title: ServiceNow AI Lens form auto-filler
description: The ServiceNow AI Lens form auto-filler uses AI image recognition to populate form fields from photos that field service technicians capture in the ServiceNow Agent mobile application. Technicians can auto-fill Input Forms and Scripted Input Forms, such as Smart Assessment questionnaires.Use ServiceNow AI Lens to auto-fill form fields by capturing or uploading an image in the ServiceNow Agent mobile app. The Lens Launcher is available on Input Forms and Scripted Input Forms, such as Smart Assessment questionnaires.Use ServiceNow AI Lens through Now Assist Virtual Agent \(NAVA\) in the ServiceNow Agent mobile application to analyze an image and receive a text summary. This flow does not auto-fill form fields.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/now-assist-for-field-service-management-fsm/c\_form-auto-filler-fsm.html
release: australia
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: concept
last_updated: "2026-05-11"
reading_time_minutes: 8
keywords: [ServiceNow Lens, Form Auto-Filler, Lens Launcher, AI image recognition, Smart Assessment, Now Assist for FSM, mobile, ServiceNow Lens, Lens Launcher, auto-fill, Form Auto-Filler, Smart Assessment, Input Form, mobile, ServiceNow Lens, Now Assist Virtual Agent, NAVA, image analysis, mobile, Now Assist for FSM]
breadcrumb: [Use generative AI skills, Now Assist for FSM]
---

# ServiceNow AI Lens form auto-filler

The ServiceNow AI Lens form auto-filler uses AI image recognition to populate form fields from photos that field service technicians capture in the ServiceNow Agent mobile application. Technicians can auto-fill Input Forms and Scripted Input Forms, such as Smart Assessment questionnaires.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

## ServiceNow AI Lens form auto-filler

The ServiceNow AI Lens form auto-filler reduces the effort of manually entering data by using AI image recognition to extract information from photos and populate form fields automatically.

The feature is a direct implementation of the platform-level ServiceNow AI Lens capability for Field Service Management. Technicians access it from a **Lens Launcher** button on supported forms, or from the ServiceNow AI Lens topic in Now Assist Virtual Agent.

## Supported form types

The ServiceNow AI Lens form auto-filler is available on the following form types in the ServiceNow Agent mobile application:

-   **Input Forms**

    Technicians can launch ServiceNow AI Lens from a record-based Input Form to auto-populate fields with extracted image data.

-   **Scripted Input Forms**

    Technicians can launch ServiceNow AI Lens from a Scripted Input Form, such as Smart Assessment questionnaires to auto-populate fields based on the form's underlying script.


## ServiceNow AI Lens in Now Assist Virtual Agent

Technicians can use in-form auto-fill or access ServiceNow AI Lens through Now Assist Virtual Agent \(NAVA\) in the ServiceNow Agent mobile application. In this process, the technician selects ServiceNow AI Lens from the NAVA topic picker, uploads or captures an image, and receives a text summary response. This flow does not auto-fill form fields. For more information, see [Use ServiceNow AI Lens in Now Assist Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/c_form-auto-filler-fsm.md).

## Plugins

The ServiceNow AI Lens form auto-filler requires the following plugins:

-   `com.sn_ai_lens` — Platform ServiceNow AI Lens plugin.
-   `com.sn.fsm.gen.ai` — Now Assist for FSM plugin. Controls access to the Lens Launcher icon on FSM forms.
-   `com.snc.fsm_smart_asmt_questionnaire` — Smart Assessment Questionnaire plugin. Required for Lens Launcher on Smart Assessment questionnaires.
-   `com.snc.app_lens_util_pack` — Defines who can use the feature, how data is processed, and the field types that ServiceNow AI Lens can populate.

**Parent Topic:**[Using Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/using-now-assist-fsm.md)

**Related topics**  


[Auto-fill a form with ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/c_form-auto-filler-fsm.md)

[Use ServiceNow AI Lens in Now Assist Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/c_form-auto-filler-fsm.md)

[Exploring Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/exploring-now-assist-fsm.md)

[Smart Assessment Questionnaires](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/smart-assessment-questionnaire.md)

## Auto-fill a form with ServiceNow AI Lens

Use ServiceNow AI Lens to auto-fill form fields by capturing or uploading an image in the ServiceNow Agent mobile app. The Lens Launcher is available on Input Forms and Scripted Input Forms, such as Smart Assessment questionnaires.

### Before you begin

Role required: wm\_agent, which inherits the lens\_user role.

### About this task

Auto-filling a form with ServiceNow AI Lens reduces manual data entry on a job site. Capture an image of an asset, document, or equipment, and ServiceNow AI Lens populates the relevant form fields from the image.

**Note:** Review AI-populated form fields for accuracy before submitting. AI-generated results may not be accurate in all cases.

These steps cover filling a Smart Assessment questionnaire for a work order task. The same steps apply when using ServiceNow AI Lens Launcher to fill Input Forms and Scripted Input Forms.

### Procedure

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


### Result

After the files are successfully scanned, some of the fields in the questionnaire are automatically filled. You can review the values and edit them, if required.

### What to do next

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


[ServiceNow AI Lens form auto-filler]()

[Use ServiceNow AI Lens in Now Assist Virtual Agent]()

[Smart Assessment Questionnaires]()

[Configuring Smart Assessment questionnaires for Now Mobile Agent]()

## Use ServiceNow AI Lens in Now Assist Virtual Agent

Use ServiceNow AI Lens through Now Assist Virtual Agent \(NAVA\) in the ServiceNow Agent mobile application to analyze an image and receive a text summary. This flow does not auto-fill form fields.

### Before you begin

Ensure that Virtual Agent is activated for Field Service Management.

Role required: wm\_agent, which inherits the lens\_user role.

### About this task

Use ServiceNow AI Lens through Now Assist Virtual Agent when you need to identify an asset, document, or item from an image and receive a text summary. This flow is useful for on-demand lookup during a job.

**Note:** Review AI-generated responses for accuracy before acting on them. AI-generated results may not be accurate in all cases. Implement human review before using results in production.

### Procedure

1.  Log in to the ServiceNow Agent mobile application.

2.  Select **Now Assist** in the navigation bar to open Now AssistVirtual Agent.

3.  From the topic picker, select **ServiceNow Lens**.

4.  Capture an image, or choose an existing image from the device.

    -   To capture a new image, select the Camera icon \[Omitted image "form-auto-filler-fsm-upload.png"\] Alt text:, then take a photo.
    -   To upload an existing image, select the Image icon \[Omitted image "lens-nava-fsm.png"\] Alt text:, then select an image from the device.
5.  Provide a relevant prompt for NAVA, such as `describe the details of the assets uploaded`, to generate a response.

6.  Review the text summary that Now Assist Virtual Agent returns.

    ServiceNow AI Lens analyzes the image and returns a text summary in the chat. This flow does not auto-fill any form fields. To auto-populate a form using ServiceNow AI Lens, see [Use ServiceNow AI Lens with the form auto-filler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/c_form-auto-filler-fsm.md).


### Result

The chat displays a text-based summary of the captured image, generated by Now Assist Virtual Agent.

**Related topics**  


[ServiceNow AI Lens form auto-filler]()

[Auto-fill a form with ServiceNow AI Lens]()

[Summarize a record using Now Assist in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/summarize-a-record-using-now-assist-virtual-agent.md)

[Create an Assistant for Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/activate-virtual-agent-for-field-service-management.md)

