---
title: Configure the GOV.UK Design System Service Portal Question Page Pattern Journey
description: Configurable portal widgets provide you with the ability to configure the behavior, content, and layout of the GOV.UK Design System Service Portal by configuring widget settings and instance options. Use the base system widgets included with the GDS Service Portal to get started configuring portal pages.Use the question page pattern as a template to set up a question journey for your constituents using the GDS Service Portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-config-govuk-dev-tk-portal-question.html
release: brazil
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 8
breadcrumb: [Configure page patterns, Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the GOV.UK Design System Service Portal Question Page Pattern Journey

Configurable portal widgets provide you with the ability to configure the behavior, content, and layout of the GOV.UK Design System Service Portal by configuring widget settings and instance options. Use the base system widgets included with the GDS Service Portal to get started configuring portal pages.

The GDS Service Portal question pages are formatted around the GOV.UK "one question per page" page pattern journey. Page patterns are "best practice design solutions to user-specific focused tasks." A citizen answers a short series of pages, each with one question, and when the constituent selects Submit, a case is created and every answer is recorded as a summary comment within the case.

This app ships the following two examples that may be cloned and used as a template. Both sample tiles should appear on the catalog page by default— "Report an abandoned vehicle \(GDS-question-pages-pattern example\)" and "Report a missed waste collection \(GDS-question-pages-pattern example\)" — alongside the two record producers they sit next to.

|Journey|Case table|Questions|Mapped to case columns|
|-------|----------|---------|----------------------|
|Report Abandoned Vehicle \(Private Property\)|`sn_gsm_service_request_case`|13|9|
|Report a Missed Waste Collection|`sn_gsm_government_service_case`|13|5|

A constituent filling out a form using the default GDS Service Portal question page journey will see the following:

1.  A journey **tile** on the services catalog page, beside the ordinary request forms.
2.  A **landing page** explaining the service, with a **Start** button. Each question journey needs its own landing page.
3.  A series of **question pages**, one question at a time, with Back links.
4.  A **full summary of questions and answers** before submitting.
5.  A **confirmation**.

A constituent filling out a form using the default GDS Service Portal question page journey will see the following:

-   **A short description naming the journey**. For example, an agent will see:

    ```
    Report Abandoned Vehicle (Private Property) (GDS-question-pages-pattern example): someone
              has left a car outside my house
    ```

    The journey name comes first so an agent knows which service the case was opened under.

-   **Selected answers written to real case fields**\(address, postcode, contact\) so they can be searched, filtered and reported on.
-   **A comment listing every question and answer**, including answers that aren't written to a field. An answer only becomes reportable if a matching column exists on the case table.
-   **A link to a read-only copy of the submitted journey**, rendered in the portal as the constituent answered it, with any uploaded files as download links. Only the citizen who submitted it, and staff who can read the case, can open that view.

## Configure the GOV.UK Design System Service Portal Question Page Pattern Journey

Use the question page pattern as a template to set up a question journey for your constituents using the GDS Service Portal.

### Before you begin

Before creating a service journey, plan the following:

1.  The citizen-facing service name.
2.  Introductory guidance.
3.  The target case table.
4.  The question pages or sections.
5.  The questions in each section.
6.  Which questions are mandatory.
7.  The control required for each question: text, text area, number, date, Yes/No, radios, dropdown, checkboxes, reference lookup, or attachment.
8.  Which answers must map to case fields.
9.  Who should be able to discover and start the service.
10. A short outcome-oriented service name, such as **Report a blocked public footpath**.

Role required: admin

### Procedure

1.  Navigate to **Assessments** &gt; **Metric Types** to view the Classic Assessment metric-type list, where you will create a metric type with the following values:

    |Field|Value|
    |-----|-----|
    |Name|Citizen-facing journey name|
    |Active|true|
    |Evaluation method|Survey|
    |Publish state|Published|
    |Portal pagination|Category|
    |Schedule type|On demand|
    |Allow retake|false, unless the service explicitly requires it|
    |Roles|Empty|
    |Source table|The case table selected during planning|
    |Introduction|Introductory guidance for the citizen|

    Save the record and copy the **sys\_id**, which is the journey identifier used in the portal URLs.

    1.  After saving, re-open the record and verify the following:

        -   `roles` is empty. The **OOTB Create Survey Records** business rule may add the `survey_admin`and `survey_reader`. Remove those roles if they appear.
        -   `schedule_type` is `on_demand`.
        -   `publish_state` is `published`.
        -   `source_table` is populated before mapping questions to fields.
        **Note:** Creating the metric type normally creates a default metric category with:

        -   A name that matches the journey name character-for-character
        -   Order `1`
        -   Empty questions
        Do not delete this category. It does not render as a citizen-facing page, but the assessment engine uses it to resolve the journey. Verify it exists by viewing the metric type's related lists, or from **Assessments** &gt; **Metric Types** &gt; **Categories**.

2.  Create an assessment metric category for each page or logical group of questions.

    For each category, set the fields to the following values:

    |Field|Guidance|
    |-----|--------|
    |Metric type|The journey created in Step 1|
    |Name|Page heading \(e.g, `Location details`\)|
    |Order|Sequential values with substantial gaps \(e.g., `100, 200, 300`\)|

    Because portal pagination is set to category per GOV.UK GDS guidelines, each category is rendered as a separate question page.

3.  Create assessment metrics under the appropriate category.

    For each question, configure the following values:

    |Field|Guidance|
    |-----|--------|
    |Metric type|The journey metric type|
    |Category|The question-page category|
    |Question|Citizen-facing question text|
    |Name|same as Question|
    |Method|Assessment|
    |Condition question|`Always`, unless conditional logic is deliberately configured|
    |Active|`true`|
    |Mandatory|As required|
    |Scored|`false` \(for normal service-request questions\)|
    |Weight|`10` \(suitable for non-scored questions\)|
    |Order|Sequential values with substantial gaps \(e.g., `100, 200, 300`\)|
    |Source field|Optional case field mapping|

    The following is a list of supported question types that allow for one-question-per-page organization.

    |Desired control|Metric datatype|Additional setting|
    |---------------|---------------|------------------|
    |Text input|`string`|String option `short` or `wide`|
    |Textarea|`string`|String option must be `multiline`|
    |Number|`long` or `percentage`|—|
    |Date|`date`|Uses the browser's native date input|
    |Yes/No radios|`boolean`|—|
    |Single checkbox|`checkbox`|—|
    |Dropdown|`choice`|Add metric definitions. For a small list, use a `scale`radio group instead of a `choice` dropdown, in line with GOV.UK guidance.|
    |Radio group|`scale` or `numericscale`|Add metric definitions. For a small list, use a `scale`radio group instead of a `choice` dropdown, in line with GOV.UK guidance.|
    |Checkbox group|`multiplecheckbox`|Add metric definitions|
    |Reference autocomplete|`reference`|Set the reference table|
    |File upload|`attachment`|—|

    **Note:** Conditional questions are supported only within the same category/page. Set **Depends on** to the controlling question, and **Displayed when** to the option values that reveal the dependent question. Classic Assessment cannot skip a later category based on an answer from an earlier page.

4.  Add the options for the choice questions; for `choice`, `scale`, `numericscale`, and `multiplecheckbox` questions, add assessment metric definitions through the question's related list.

    For every choice option, set the following values:

    |Field|Guidance|
    |-----|--------|
    |Metric|Enter the question text.|
    |Display value|Enter the citizen-facing option label.|
    |Value|Enter the stable internal value.|
    |Order|Sequential values with substantial gaps \(e.g., `100, 200, 300`\)|

5.  Map the question answers to case fields in the case table.

    To copy an answer into a case field, set the question metric's `Source field`.

    To proceed, both of these conditions must be met:

    1.  The metric type has the correct **Source table**.
    2.  The selected field exists on that table and accepts the question's value.
    For example, when the target is `sn_gsm_service_request_case`, address answers can be mapped to fields such as `street`, `city`, `province`, or `zip`, **if**those fields exist on that table.

    Inherited fields are valid mappings, but fields defined only on a child table are not available when the journey targets its parent. Verify the effective field set for the selected target table in **System Definition** &gt; **Tables &amp; Columns** before saving the mapping.

    Unmapped answers are still included in the case's question-and-answer summary, but they are **not** available as separate reportable case fields. An answer only becomes reportable if it contains a matching field in the table.

    Set the source table before mapping any questions. If the source table is changed later, the OOTB **Wipe Metric Source Fields** rule can clear every mapping in the journey. Re-open all questions and restore their Source field values after any source-table change.

6.  Configure a dedicated assessment page for case creation.

    The shared `ukgds_assessment` page is useful for testing, but its widget options are shared by every journey using that page. Do not set a journey-specific case table on the shared instance unless every journey on it should create the same kind of case.

    For a configuration-only service:

    1.  Open Service Portal → Service Portal Configuration → Designer.

    2.  Clone the existing `ukgds_assessment` page.

    3.  Assign a unique page ID, for example `ukgds_blocked_footpath_assessment`.

    4.  Open the UK GDS Assessment widget instance options on the cloned page.

    5.  Set **Metric type sys\_id** \(`metric_type_sys_id`\) to the metric type created in Step 1.

    6.  Set **Case target table** \(`case_target_table`\) to the intended case table.

    7.  Set **Allow resume** according to the service policy.

        `True` lets a citizen resume an in-progress assessment.

    8.  Enable or disable the step indicator, inline answer summary, section descriptions, and question guidance as required.

    9.  If completed submissions should link to the read-only answer view, set **Case view page ID** to `ukgds_assessment_view`.

    10. Save and test the cloned page directly.

    Because the widget instance pins `metric_type_sys_id`, the cloned page URL does not need the `type` parameter. The configured `case_target_table` supplies the journey-to-case registration that would otherwise require a source-code map entry.

7.  After submitting, locate the newest case on the configured target table.

    Verify that:

    -   A case was created on the expected table.
    -   `opened_by` identifies the submitting citizen.
    -   The short description identifies the journey.
    -   `correlation_id` contains the assessment instance sys\_id.
    -   Mapped answers populated the intended case fields.
    -   The case comments contain the complete question-and-answer summary.
    -   Attachments are available to the agent where applicable.

