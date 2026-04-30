---
title: Create a grant program using Grants Management Program Set Up for Public Sector Digital Services
description: As a grant program manager at a government service agency, you can use the Public Sector Digital Services Grants Management program setup​ to either create a grant program from scratch, or create one from an existing configuration.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Using Grants Management, Using Playbooks, Using Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Create a grant program using Grants Management Program Set Up for Public Sector Digital Services

As a grant program manager at a government service agency, you can use the Public Sector Digital Services Grants Management program setup​ to either create a grant program from scratch, or create one from an existing configuration.

## Before you begin

Role required: awa\_agent, snc\_internal, sn\_svc\_appl\_pgm\_mg.grant\_program\_manager

## Procedure

1.  Navigate to **All** &gt; **CSM Configurable Workspace**.

2.  Navigate to **Lists** &gt; **Grant Programs** and select **New**.

    Here, you have the option to create a program from the default template, or start by copying data and configurations from an existing grant program.

    -   To create a grant program without using any pre-existing configurations, select **New**.
    -   To copy data and configurations from an pre-existing grant program, select **Create a new program from an existing program**. Select the existing program from the dropdown menu and select **Continue**.

        If copying from an existing program, you can determine which fields are copied over to the new grant program record, as well as fields in related records, including default fields. You can easily add or remove fields.

    A new grant program is created within the Grant Program table \(sn\_svc\_appl\_pgm\_mg\_grant\_program\), and the playbook is moved to the **Define Program** stage.

3.  On the form, fill in the details of the grant program, and select **Mark Complete** to move to the next activity.

    A product model record, service definition record, and draft playbook content item have been created for the grant program.

4.  Define the members of your internal agency team who will be responsible for this grant program.

    These are different than points of contact that potential applicants can reach out to during the grant proposal phase. You can add public points of contact in a later step, using existing contacts from this list.

5.  Select **Save**, then **Mark Complete** to move to the next activity.

6.  Define the total program budget, including the award allocation and budget categories.

    Provide information about the award and budget of the program. Define how the grant program budget is split across different categories. This is used to manage the program, and is published as part of the solicitation and proposal.

7.  Define any internal or external key milestones for your program, and select **Mark Complete** to move to the next activity.

    Milestones can be edited throughout the duration of the program.

8.  Define the due date for the merit review tasks, and select which merit review framework and scoring rubric should be used for this program.

    To create a scoring framework:

    1.  Select **open the frameworks list**.

    2.  Select **New** and enter the name and description.

    3.  Select **Submit** and choose the new framework in the **Review framework** field.

9.  Select **Mark Complete** to move to the next activity.

10. Define the users who will review and score the proposals for this program, then select **Mark Complete** to move to the next activity.

    You can update reviewer groups throughout the duration of the program as needed.

11. Select which results letter templates should be used to notify applicants of their results for this program and select **Mark Complete** to move to the next activity.

12. Configure the announcement details with information that should be displayed on the program opportunity announcement page that is shown to prospective applicants.

    You must provide a banner image, grant synopsis, eligibility summary, and grant description.

    **Note:** The information entered in the Define program activity also appears in the program announcement.

13. Select **Mark Complete** to move to the next activity.

14. Add members of your internal team who can be contacted by grant seekers.

    These users and their contact information will be displayed publicly on the announcement page.

15. Add resources that provide supplemental information about this program, its sponsoring agency, impact, or any other details that may help grant seekers better understand this opportunity.

16. Select **Mark Complete** to move to the next activity.

17. Select which Guided Decision tree should be used in the applicant's pre-eligibility screener, displayed before the start of their proposal.

    To create a pre-eligibility screener questionnaire, select **Open the Decision Trees list** and follow the prompts. For more information on creating an eligibility decision tree for Grants Management, see [Configure pre-eligibility questions in Grants Management](psds-config-gmp-config-pre-eligibility.md).

18. Select which conditional policy \(PACE\) framework should be used to screen grant proposals.

19. Select which applicant information form the applicant should see in the "Enter applicant information" section of their proposal.

    To create an applicant information form, select **open the form builder** and follow the prompts.

20. Select which type of personnel are required for the applicant to include in the "Add key personnel" section of their proposal.

    Applicants will also be able to include additional personnel of their choosing.

21. Select which budget documents and cumulative budget subtotals applicants are required to provide in the "Add proposal budget" section of their proposal.

22. Select how applicants should provide their proposal narrative, and the minimum number of goals they should provide in the "Add proposal narrative" activity.

23. Select which additional PDF forms and other documents an applicant is required to include in the "Add required forms" section of their proposal.

    At least one document is required to complete this activity. You can also create new or edit existing documents.

24. Select a compliance assessment for applicants to complete in the "Enter compliance information" section of their proposal.

    Compliance assessments for proposals can only support:

    -   Single-choice and text area type questions
    -   Additional conditional questions based on single-choice answers
    To create a compliance form, you can use the Smart Assessment feature. For more information on the Smart Assessment feature, see [Configure the Smart Assessment Engine for Grants Management](psds-config-gmp-smart-assessment-engine.md).

25. Select which terms and conditions the applicant should see in the "Sign and Submit" section of their proposal, then select **Mark Complete** to move to the next activity.

    To create a terms and conditions list, open the Terms &amp; Conditions list.

26. Preview the published announcement, and select **Mark Complete** to move to the next activity.

27. Preview the proposal content as viewed by applicants on the portal, and select **Mark Complete** to move to the next activity.

28. Select one of the following actions to complete the review:

    -   **Request Approval**- Submit a request to the internal program team or the grant program director to review and approve the grant proposal. You can publish the grant program only after it’s approved by the internal program team or the grant program director.
    -   **Skip approval**- Move to the next activity without requesting an approval from the internal program team or the grant program director.
29. You may either publish the grant program immediately, or schedule the date you wish the program to be displayed live.

    Configure the following details:

    -   **Announcement removal date**- The date on which the grant or the catalog item is removed from the announcement page.
    -   **Proposal close date**- The date when the proposal is closed.
30. Select **Publish** to create the grant catalog item and publish the grant to the Grant Management portal.


