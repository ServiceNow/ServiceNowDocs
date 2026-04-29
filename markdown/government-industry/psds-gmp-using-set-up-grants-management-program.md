---
title: Create a grant program using Grants Management program setup for Public Sector Digital Services
description: As a grant program manager at a government service agency, use the Public Sector Digital Services Grants Management program setup​ to either create a new grant program, or create one from an existing configuration.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Create a grant program, How to set up a grant program]
breadcrumb: [Using Grants Management, Solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Create a grant program using Grants Management program setup for Public Sector Digital Services

As a grant program manager at a government service agency, use the Public Sector Digital Services Grants Management program setup​ to either create a new grant program, or create one from an existing configuration.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **CSM Configurable Workspace**.

2.  Navigate to **Lists** &gt; **Grant Programs** and choose **New**.

    Here, you have the option to create a program from the default template, or start by copying data and configurations from an existing grant program.

    -   To create a grant program without using any pre-existing configurations, choose **New**.
    -   To copy data and configurations from a pre-existing grant program, choose **Create a new program from an existing program**. Choose the existing grant program from the drop-down menu and select **Continue**.

        You can determine which fields are copied over to the new grant program record, as well as fields in related records, including default fields. You can easily add or remove fields.

    A new grant program is created within the Grant Program table \(sn\_svc\_appl\_pgm\_mg\_grant\_program\), and the playbook is moved to the Define Program stage.

3.  Choose **Add funding program** and select a funding program ID from the drop-down menu.

    The grant program is associated with the selected funding program ID and share the cumulative budget of that funding program and its start and end dates fall within the funding program's duration.

4.  Choose **Save**.

5.  On the **Grant Program** form, fill in the details of the grant program, and choose **Mark Complete** to move to the next activity.

    A product model record, service definition record, and draft playbook content item have been created for the grant program.

6.  Define the members of your internal agency team who are responsible for this grant program, then move to the next activity by choosing **Save**, then **Mark Complete**.

    Only grant directors appear in the employee name.

    These members are different than points of contact that potential applicants can reach out to during the grant proposal phase. You add public points of contact in a later step, using existing contacts from the **Employee name** drop-down list.

7.  Define the total program budget, including the award allocation and budget categories.

    Provide information about the award and budget of the program. Define how the grant program budget is split across different categories. This information is used to manage the program, and is published as part of the solicitation and proposal.

8.  Define any internal or external key milestones for your program, and choose **Mark Complete** to move to the next activity.

    Milestones can be edited throughout the duration of the program.

9.  Define the due date for the merit review tasks, and select which merit review framework and scoring rubric should be used for this program.

    To create a scoring framework:

    1.  Choose **open the frameworks list**.

    2.  Choose **New** and enter the name and description.

    3.  Choose **Submit** and choose the new framework in the **Review framework** field.

10. Choose **Mark Complete** to move to the next activity.

11. Define the users who will review and score the proposals for this program, then choose **Mark Complete** to move to the next activity.

    You can update reviewer groups throughout the duration of the program as needed.

12. Select which results letter templates should be used to notify applicants of their results for this program and choose **Mark Complete** to move to the next activity.

13. Configure the announcement details with information that should be displayed on the program opportunity announcement page that is shown to prospective applicants.

    You must provide a banner image, grant synopsis, eligibility summary, and grant description.

    **Note:** The information entered in the Define program activity also appears in the program announcement.

14. Choose **Mark Complete** to move to the next activity.

15. Add members of your internal team who can be contacted by grant seekers.

    These users and their contact information are displayed publicly on the announcement page.

16. Add resources that provide supplemental information about this program, its sponsoring agency, impact, or any other details that may help grant seekers better understand this opportunity.

17. Choose **Mark Complete** to move to the next activity.

18. Select which Guided Decision tree should be used in the applicant's pre-eligibility screener, displayed before the start of their proposal.

    To create a pre-eligibility screener questionnaire, choose **Open the Decision Trees list** and follow the prompts. For more information on creating an eligibility decision tree for Grants Management, see [Configure pre-eligibility questions in Grants Management](psds-config-gmp-config-pre-eligibility.md).

19. Select which conditional policy \(PACE\) framework should be used to screen grant proposals.

20. Choose which applicant information form the applicant should see in the Enter applicant information section of their proposal.

    To create an applicant information form, choose **open the form builder** and follow the prompts.

21. Select which type of personnel are required for the applicant to include in the Add key personnel section of their proposal.

    Applicants are also able to include additional personnel of their choosing.

22. Select which budget documents and cumulative budget subtotals applicants are required to provide in the"Add proposal budget section of their proposal.

23. Choose how applicants should provide their proposal narrative, and the minimum number of goals that they should provide in the "Add proposal narrative" activity.

24. Select which additional PDF forms and other documents an applicant is required to include in the Add required forms section of their proposal.

    At least one document is required to complete this activity. You can also create new or edit existing documents.

25. Select a compliance assessment for applicants to complete in the Enter compliance information section of their proposal.

    Compliance assessments for proposals can only support:

    -   Single-choice and text area type questions
    -   Additional conditional questions based on single-choice answers
    To create a compliance form, you can use the Smart Assessment feature. For more information on the Smart Assessment feature, see [Configure the Smart Assessment Engine for Grants Management](psds-config-gmp-smart-assessment-engine.md).

26. Select which terms and conditions the applicant should see in the "Sign and Submit" section of their proposal, then choose **Mark Complete** to move to the next activity.

    To create a terms and conditions list, open the Terms &amp; Conditions list.

27. Preview the published announcement, and choose **Mark Complete** to move to the next activity.

28. Preview the proposal content as viewed by applicants on the portal, and choose **Mark Complete** to move to the next activity.

29. Select one of the following actions to complete the review:

    -   **Request Approval**- Submit a request to the internal program team or the grant program director to review and approve the grant proposal. You can publish the grant program only after it’s approved by the internal program team or the grant program director.
    -   **Skip approval**- Move to the next activity without requesting an approval from the internal program team or the grant program director.
30. Either publish the grant program immediately, or schedule the date that you want the program to be displayed live.

    Configure the following details:

    -   **Announcement removal date**- The date on which the grant or the catalog item is removed from the announcement page.
    -   **Proposal close date**- The date when the proposal is closed.
31. Create the grant catalog item and publish the grant to the Grant Management portal by choosing **Publish**.


