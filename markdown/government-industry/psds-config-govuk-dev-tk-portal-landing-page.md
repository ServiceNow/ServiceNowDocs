---
title: Configure a GOV.UK Design System Service Portal citizen-facing landing page
description: Create a catalog anchor landing page that lets constituents find a question-page journey on the GDS Service Portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-config-govuk-dev-tk-portal-landing-page.html
release: brazil
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 8
breadcrumb: [Configure page patterns, Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure a GOV.UK Design System Service Portal citizen-facing landing page

Create a catalog anchor landing page that lets constituents find a question-page journey on the GDS Service Portal.

## Before you begin

Role required: admin

## About this task

A question or service request journey lives on its own instance page, and, by default, without an anchor, nothing in the catalog will point at it and render it reachable. Create a catalog anchor item on the services page \(by default, `uk_gds_services`\) to ensure that the question or service request journey appears as a listed catalog item. You can use **Service Portal Designer** to create or copy a page.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Designer**.

3.  Select UK Government Portal to switch to editing or designing pages for the GDS Service Portal.

    \[Omitted image "psds\_service\_portal\_designer\_select\_portal.png"\] Alt text:

4.  From the Service Portal Designer, select an existing GOV.UK journey landing page, and select **Copy**.

5.  Give it a unique page ID, such as `uk_gds_blocked_footpath`.

6.  Update the heading and introductory content.

7.  Configure its Start link to open the dedicated assessment page created for the question journey.

    For more information, see the last step of this procedure: [Configure the GOV.UK Design System Service Portal Question Page Pattern Journey](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-config-govuk-dev-tk-portal-question.md).

8.  Restrict the page to **snc\_external** and/or **snc\_internal**.

    **Note:** Mark the page public **if** anonymous users are allowed to use the service.

9.  To make the journey discoverable from the Services page, create a content item in the Service Catalog by entering the following values:

    |Field|Value|
    |-----|-----|
    |Name|Journey name|
    |Active|true|
    |Content type|External|
    |URL|`?id=<landing_page_id>`|
    |Access type|Restricted|
    |Catalog|UK Government catalog|
    |Category|Appropriate service category|
    |Available on desktop|true|
    |Visible standalone|true|

    Navigate to the **Not Available For** and **Available For** related lists to set the user criteria for the intended audiences. The user criteria can be set to:

    -   users with `SNC External` role to allow both registered and unregistered constituents to access the question or service request journey from the catalog landing page.
    -   users with `snc_internal` role to allow only registered constituents to access the question or service request journey from the catalog landing page.
    **Note:** **Not Available For** overrides **Available For**. Access to the catalog landing page is configured separately.

10. Create the assessment metric type.

    1.  Navigate to **Assessments** &gt; **Metric Types**. The menu location can vary by instance.
    2.  Create a record with these values:

        |Field|Value|
        |-----|-----|
        |Name|Citizen-facing journey name, for example *Report a blocked public footpath*|
        |Active|true|
        |Evaluation method|Survey|
        |Publish state|Published|
        |Portal pagination|Category|
        |Schedule type|On demand|
        |Allow retake|false, unless the service requires it|
        |Roles|Empty|
        |Source table|The case table you selected during planning|
        |Introduction|Introductory guidance for the citizen|

    3.  Save the record and copy its `sys_id`. This is the journey identifier used in portal URLs.
    4.  Reopen the record and verify that `roles` is empty, `schedule_type` is `on_demand`, `publish_state` is `published`, and `source_table` is populated. The out-of-the-box **Create Survey Records** business rule can add `survey_admin,survey_reader` to `roles`. Remove those roles, otherwise citizens cannot open the journey.
11. Keep the default metric category.

    Creating the metric type creates a default category whose name matches the journey name exactly, with order `1` and no questions. Do not delete or rename it. It does not render as a citizen-facing page, but the assessment engine uses it to resolve the journey. If it is missing or renamed, the portal can report *No questions were generated for you*.

12. Create one assessment metric category for each question page.

    Set **Metric type** to the journey, **Name** to the page heading \(for example, *Location details*\), and **Order** with gaps such as 100, 200, and 300. Because portal pagination is set to `category`, each category renders as a separate question page.

13. Create the questions under each category.

    Create an assessment metric for each question with these values:

    |Field|Value|
    |-----|-----|
    |Metric type|The journey metric type|
    |Category|The question-page category|
    |Question|Citizen-facing question text|
    |Name|Usually the same as Question|
    |Method|Assessment|
    |Condition question|Always, unless you deliberately configure conditional logic|
    |Active|true|
    |Mandatory|As required|
    |Scored|false for normal service-request questions|
    |Weight|10 for non-scored questions|
    |Order|100, 200, 300 within the category|

    Set the metric datatype for the control you need:

    |Control|Datatype and setting|
    |-------|--------------------|
    |Text input|`string`, string option `short` or `wide`|
    |Textarea|`string`, string option `multiline` \(not `multi_line`\)|
    |Number|`long` or `percentage`|
    |Date|`date` \(browser native date input\)|
    |Yes/No radios|`boolean`|
    |Single checkbox|`checkbox`|
    |Dropdown|`choice`, add metric definitions|
    |Radio group|`scale` or `numericscale`, add metric definitions|
    |Checkbox group|`multiplecheckbox`, add metric definitions|
    |Reference autocomplete|`reference`, set the reference table|
    |File upload|`attachment`|

    For a small list, use `scale` radios instead of a `choice` dropdown, in line with GOV.UK guidance.

    For `choice`, `scale`, `numericscale`, and `multiplecheckbox` questions, add assessment metric definitions from the question's related list. For each option set the metric, a citizen-facing display value, a stable internal value, and a display order. Set the metric's maximum value to the number of options where the assessment form requires it.

    Conditional questions work only within the same category. Set **Depends on** to the controlling question and **Displayed when** to the option values that reveal the dependent question. Classic Assessment cannot skip a later category based on an answer from an earlier page.

14. Optional: Map answers to case fields.

    Set the question metric's **Source field**. The metric type must have the correct **Source table**, and the selected field must exist on that table and accept the question's value. Inherited fields are valid mappings. Fields defined only on a child table are not available when the journey targets its parent. Verify the effective field set in **System Definition** &gt; **Tables &amp; Columns**.

    Unmapped answers still appear in the case's question-and-answer summary, but not as separate reportable case fields.

    **Important:** Set the source table before you map any questions. If you change the source table later, the out-of-the-box **Wipe Metric Source Fields** rule can clear every mapping in the journey. Restore all Source field values after any source-table change.

15. Test the journey directly.

    Open `https://<instance>/<portal>?id=ukgds_assessment&type=<metric_type_sys_id>` as a real `snc_external` portal user. Admin can bypass security rules and hide access problems.

    Verify that the introduction appears, each category is a separate page, questions are in the expected order, mandatory validation works, choice labels and values are correct, attachments upload, and submission completes without an authorization error.

    If the portal reports that no questions were generated, check that the metric type is published, active, on demand, has the default category, and is not restricted by roles.

16. Configure a dedicated assessment page for case creation.

    The shared `ukgds_assessment` page shares its widget options across every journey that uses it, so do not set a journey-specific case table on it.

    1.  Navigate to **Service Portal** &gt; **Service Portal Configuration** &gt; **Designer**.

    2.  Clone the `ukgds_assessment` page and give it a unique page ID, for example `ukgds_blocked_footpath_assessment`.

    3.  Open the UK GDS Assessment widget instance options on the cloned page.

    4.  Set **Metric type sys\_id** \(`metric_type_sys_id`\) to the metric type that you created.

    5.  Set **Case target table** \(`case_target_table`\) to the intended case table.

    6.  Set **Allow resume** according to service policy. When true, a citizen can resume an in-progress assessment.

    7.  Enable or disable the step indicator, inline answer summary, section descriptions, and question guidance as required.

    8.  To link completed submissions to the read-only answer view, set **Case view page ID** to `ukgds_assessment_view`.

    9.  Save the page and test it at `https://<instance>/<portal>?id=<dedicated_assessment_page_id>`.

        The URL does not need the `type` parameter because the widget instance pins `metric_type_sys_id`.

17. Verify case creation.

    Submit the journey, then find the newest case on the target table. Confirm that:

    -   The case was created on the expected table.
    -   `opened_by` identifies the submitting citizen.
    -   The short description identifies the journey.
    -   `correlation_id` contains the assessment instance sys\_id.
    -   Mapped answers populated the intended case fields.
    -   The case comments contain the complete question-and-answer summary.
    -   Attachments are available to the agent, where applicable.
    If no case is created, confirm that the dedicated assessment widget instance has the correct `case_target_table`. Using the shared page without that option requires a source-managed journey registration and cannot be completed through instance configuration alone.

18. Create a citizen-facing landing page.

    In Service Portal Designer, copy an existing GOV.UK journey landing page and give it a unique page ID, such as `uk_gds_blocked_footpath`. Update the heading and introductory content. Configure the Start link to open `?id=<dedicated_assessment_page_id>`.

    Mark the page public only if anonymous users are allowed to start the service. Otherwise restrict it to `snc_external`, `snc_internal`, or both.

19. Add a Services-page tile.

    Create a catalog content item with these values:

    |Field|Value|
    |-----|-----|
    |Name|Journey name|
    |Active|true|
    |Content type|External|
    |URL|`?id=<landing_page_id>`|
    |Access type|Restricted|
    |Catalog|UK Government catalog|
    |Category|Appropriate service category|
    |Available on desktop|true|
    |Visible standalone|true|

    Add **Available For** user criteria for the intended audiences, normally SNC External and users with the `snc_internal` role. Check the **Not Available For** related list and remove SNC External if it appears there and the service is for citizens. Not Available For overrides Available For. Test discovery as the actual target user type.

20. Configure a read-only submitted-answer link.

    The toolkit page `ukgds_assessment_view` shows a completed assessment at `?id=ukgds_assessment_view&instance=<assessment_instance_sys_id>`. Access is intended for the submitting citizen and staff who can read the resulting case. Verify this with non-admin users before you rely on it, especially when attachments are present.

21. Complete security and accessibility checks.

    Test with an `snc_external` citizen, an `snc_internal` agent, a user who should not have access, and an unauthenticated user if any page is public. Confirm that:

    -   Unauthorized users cannot start or view restricted journeys.
    -   One citizen cannot view another citizen's completed assessment.
    -   Case ACLs allow the intended agent roles.
    -   Keyboard-only completion works, errors and the error summary are announced correctly, and focus moves correctly between question pages.
    -   The flow reflows at 400% zoom without horizontal scrolling.
    -   Question wording, hints, and validation messages follow GOV.UK patterns.

## Result

The journey is available to the intended citizens, and submissions create cases on the configured target table.

