---
title: Feedback definition form
description: Description of the feedback definition form fields to curate the experience and service feedback widgets in the portal pages.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Employee Center Pro reference, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Feedback definition form

Description of the feedback definition form fields to curate the experience and service feedback widgets in the portal pages.

<table id="table_edn_1vh_tzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the feedback definition

</td></tr><tr><td>

Feedback type

</td><td>

-   **Experience:** Feedback through the drawer widget visible across the portal or through the Virtual Agent.
-   **Service - in page:** Feedback after using any page on the portal.
-   **Service - topic page:** Feedback for a topic page under a taxonomy.

**Note:** Admin must select the topic page where the feedback prompt appears.

-   **Service - workflow:** portal, Virtual Agent, or email where you want to set up the feedback experience.

 **Note:**

-   You can exclude a page on the portal manually from all the feedback types except **Service - topic page**.
-   You can view **Survey** as a feedback type only if you have a **Survey Instances** set up.

For more information on setting up a survey instance, see [Configure a survey in the survey designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_ConfigSurveyInSurveyDesgnr.md).

</td></tr><tr><td>

Widget mode

</td><td>

**Drawer:** Drawer widget shows up on the portal pages.This widget mode is visible when the feedback type is **Experience**.

</td></tr><tr><td>

Widget mode

</td><td>

**Modal:** Feedback widget visible unless there’s an overlay setting in place to stop the reload.**Note:** **Overlay session limit** can be configured from the feedback configuration form.

</td></tr><tr><td>

Widget mode

</td><td>

**Inline:** Feedback widget visible inline on the portal page.

</td></tr><tr><td>

Channel

</td><td>

**Portal**: Channel to receive feedback from the portal pages.

</td></tr><tr><td>

Channel

</td><td>

**Mobile**: Channel to receive feedback from the MESP pages.

</td></tr><tr><td>

Channel

</td><td>

**Email**: Channel to receive feedback via Outlook email.This channel is visible only when **Service - workflow** or **Survey** is selected from the **Feedback type**.

</td></tr><tr><td>

Channel

</td><td>

**Virtual Agent**: Channel to receive the feedback via the Virtual Agent.This channel is visible only when **Service - workflow** or **Survey** is selected from the **Feedback type**.

</td></tr><tr><td>

Active

</td><td>

SelectedOption to keep the feedback definition record active.

</td></tr><tr><td>

Portals

</td><td>

Portal where the feedback shows up. Each feedback definition targets one portal that provides flexibility of creating separate definitions for different portals.This field is only available when the **Channel** is **Portal** or **Mobile**.

</td></tr><tr><td>

Audience

</td><td>

Target audience for the feedback.This field is only available when the **Channel** is **Portal** or **Mobile**.

</td></tr><tr><td>

Order

</td><td>

Order of priority for the feedback.The larger the order in number, the higher is the priority of the feedback definition.

</td></tr><tr><td>

Feedback content

</td><td>

**Use existing survey**: Option to enable the **Survey** field to add a survey to the definition.The check box is available for both **Experience** and **Service - in page** **Feedback type**.

</td></tr><tr><td>

Feedback content

</td><td>

**Question**: Question to provide feedback on that is visible to the user.This field appears only when **Feedback type** is **Service -in page**, **Service - topic page**, or **Service - workflow**.

</td></tr><tr><td>

Feedback content

</td><td>

**Rating**: Type of rating chosen for the feedback.The options available are the following:

-   **Experience**
-   **Numeric - 5 point scale**
-   **Stars - 5 point scale**

</td></tr><tr><td>

Feedback content

</td><td>

**Additional information label**: Text field to write additional feedback. This field is visible when **Allow additional information** box is checked.

</td></tr><tr><td>

Feedback content

</td><td>

**Additional information requirement**: Additional information of varying requirements to be provided.

 The following options are available:

-   **Optional**: Additional information is optional before submitting the feedback.
-   **Mandatory**: Additional information is mandatory before submitting the feedback.
-   **Mandatory based on rating threshold**: Additional feedback is mandatory if the rating is equal to or below the set threshold. The threshold is configurable.

</td></tr><tr><td>

Feedback content

</td><td>

**Rating threshold**: Rating threshold below which additional information is mandatory to submit the feedback.

 This field is only visible when the **Additional information requirement** is **Mandatory based on rating threshold**.

</td></tr><tr><td>

Feedback content

</td><td>

**Survey**: Existing survey to be added to the **Feedback type**.To use a survey for the **Email** **Channel**, Outlook Actionable Messages must be selected in the survey definition.

To use a survey for the **Virtual Agent** **Channel**, **Chat Survey** must be selected in the survey definition. For more information about chat surveys, see [Create chat surveys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/create-chat-surveys.md).

For more information about survey definitions, see [Modify a survey definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_ModifySurveyDefinitions.md).

</td></tr><tr><td>

Feedback content

</td><td>

**Survey rating metrics**: Survey question type that is used to gauge customer satisfaction. It captures feedback data for the User Experience Dashboard. **Note:** A feedback task is generated when the rating provided is beneath or equal to the value set for the **Rating threshold** field.

The question must have a numeric answer type. Text-type answers aren’t supported in this field.

This field is available only when a **Survey** is selected from the list of surveys in the **Survey** field.

</td></tr><tr><td>

Page selection

</td><td>

**All pages:** SelectedOption to choose all pages for a **Feedback type**.

</td></tr><tr><td>

Page selection

</td><td>

**Included pages:** Pages where the feedback type is available. This field is visible when the **All pages** check box is cleared.

</td></tr><tr><td>

Page selection

</td><td>

**Excluded pages:** Pages the feedback type isn’t added.The **Included pages** field is replaced by the **Excluded pages** field when **All pages** is checked.

</td></tr><tr><td>

Overlay settings

</td><td>

Overlay settings for the feedback to determine how and when it shows up to the user.**Widget trigger:** Trigger type for the overlay settings. The following are the available widget triggers.

**Manual:** Feedback widget is only available when selected.

This field is only available for **Widget mode** **Drawer**.

**Delay:** Feedback widget is available after an allotted delay.

**On scroll:** Feedback widget is available on scrolling.

**On load**: Feedback widget is available on loading the page.

**Widget delay**: Delay in loading the feedback widget measured in seconds.

This field appears only when **Delay** is selected in **Widget trigger**.

</td></tr><tr><td>

User Engagement

</td><td>

**Feedback Exclusion Period**: Period of time selected as a buffer when the user won't be reminded to provide feedback when they land on a page.

</td></tr><tr><td>

Post-feedback Configuration

</td><td>

**Rating threshold**: Rating value below which a feedback task is generated.**Note:** Feedback task for any feedback type is generated when the rating provided is beneath or equal to the value set for the **Rating threshold** field.

**Assignment groups**: Group that receives the feedback task when generated.

**Create feedback task**: Selected

Option to create a feedback task post-feedback submission.

</td></tr></tbody>
</table>**Parent Topic:**[Employee Center Pro reference](emp-center-pro-reference.md)

**Related topics**  


[Block content form](block-content-form.md)

[Campaign overview and Campaign analytics dashboards](../concept/ecpro-content-automation-content-pack.md)

[Components installed with Employee Center Pro](components-installed-with-employee-center-pro-1.md)

[Components installed with Content engagement](installed-content-engagement.md)

[Components installed with Content Experiences](installed-with-content-auto.md)

[Components installed with Content Publishing](installed-with-content-delivery.md)

[Components installed with Content Governance](ec-installed-content-governance.md)

[Components installed with Content Analytics](ecpro-installed-content-analytics-1.md)

[Content Analytics dashboards](../concept/content-analytics-dashboards.md)

[Content engagement dashboard](../concept/ec-pro-content-engagement-dashboard.md)

[Content Library Overview dashboard](../concept/content-library-overview-dashboard.md)

[Employee Center Pro widgets](employee-center-pro-widgets-list.md)

[Feedback configuration form](ex-feedback-new-record.md)

[Link content form](link-content-form.md)

[Notification content form](notification-content-form.md)

[Properties installed with Content Experiences](properties-installed-with-content-auto.md)

[Properties installed with Content Governance](properties-installed-content-governance.md)

[Properties installed with Content Publishing](properties-with-content-delivery.md)

[Standard banner and icon sizes](ec-portal-images-size.md)

[To-do content form](to-do-content-form.md)

