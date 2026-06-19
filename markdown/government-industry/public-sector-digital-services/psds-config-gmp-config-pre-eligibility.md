---
title: Configure pre-eligibility questions in Grants Management
description: The Grants Management Program Setup enables grant program managers to use decision trees to define a series of pre-eligibility questions to check if the applicants qualify for the program.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-config-gmp-config-pre-eligibility.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure PaCE Eligibility Framework Engine, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure pre-eligibility questions in Grants Management

The Grants Management Program Setup enables grant program managers to use decision trees to define a series of pre-eligibility questions to check if the applicants qualify for the program.

## Before you begin

Role required: sn\_svc\_appl\_pgm\_mg.grant\_program\_manager, sn\_gsm\_grnt\_mgmt.grant\_admin, admin

The Grants Management incorporates the use of pre-eligibility criteria, a series of questions that may be posed to an applicant to determine whether they are eligible to apply for a grant. The purpose is to deflect proposals in which the applicant is not eligible to obtain a grant.

The Eligibility &amp; Screening activity allows the user to either select an existing decision tree or create a new decision tree with a series of pre-eligibility questions to check if the applicants qualify for the program. Note: there can only be one decision tree per Grant Program.

You can configure the pre-eligibility questionnaire in one of two ways:

-   By navigating directly to the **Decision Tree \(ga\_decision\_tree\)** table and following steps to create a new decision tree
-   Through the **Eligibility and screening**activity during the Grant Program creation process, where you are provided with the option to either:
    -   Select a decision tree that an admin has already created by selecting the search icon in the Decision tree field, or
    -   Create a new decision tree by selecting **Open the Decision Trees list**. Here, you can configure a new decision tree and define the associated pre-eligibility questions.

To configure the Pre-Eligibility questions for a new Grant Program using a decision tree:

## Procedure

1.  Set the scope to **Grants Management Playbook**.

2.  In the Decision Tree \(ga\_decision\_tree\) table, select **New** to open a new Decision Tree record form where you can define the details of your decision tree.

3.  On the form, fill in the fields.

4.  Unselect the checkbox next to **Show a dismiss button**.

5.  Select **Submit** to create the decision tree record.

6.  Select **Open in Builder** to open the Decision Tree builder, where you can add questions, define branching logic, and set eligibility criteria.

7.  Select the **New** node and enter the Node name, then select the relevant reference table.

    Enter `PreEligibility` as the Node name, and select Grants Management Case as the reference table.

8.  Select **Add question** and enter the desired Question.

9.  Select **Choice** in the Type of answer field, and provide options `Yes` and `No`.

10. Select **Save and Close**.

11. Select the **+** icon below the Pre-Eligibility node to add a new path and node.

12. Select **New Path** to define a branching path from the Pre-Eligibility node.

    This will be the Eligible Path.

13. Select **Submit** to save the new decision tree.

14. Set the Path name to **Eligible Path**.

15. Define the conditions by selecting the questions and entering their answers.

16. Select **Save and close** to save the path configuration.

17. Select **Add node** under the Eligible Path, then select **Propose a guidance as an outcome**, then select **Continue**.

18. Set the Node name to **Eligible**, and set the guidance as **Grants Pre-Eligibility**.

19. Select the check box next to **Eligible**, then select **Save and close**.

20. Set the Guidance for **Non-Eligible Path** and enter the Node name as **Not Eligible**.

21. Select **Grants Pre-Eligibility** under Guidance, and unselect the checkbox for **Eligible**.

22. Select **Save and Close**.

23. Select **Activate** to publish the decision tree for use within the Grant Program.


## Result

\[Omitted image "psds\_grants\_program\_elig\_q.png"\] Alt text: eligibility questions

When applicants proceed to answer eligibility questions, they are presented with the questionnaire that you have just created using the decision tree. Based on their responses:

-   \[Omitted image "psds\_gm\_pre\_eligible.png"\] Alt text: pre-eligbility questions view

    If eligible, they will see a success message and the option to proceed with their proposal.

-   \[Omitted image "psds\_gm\_pre\_not\_eligible.png"\] Alt text: pre-eligbility questions view

    If not eligible, a message will indicate that they may not be eligible and suggest reviewing their answer.


**Parent Topic:**[Configure PaCE Eligibility Framework Engine for use with Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gmp-pace.md)

**Previous topic:**[Configure PaCE Eligibility Framework Engine for use with Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gmp-pace.md)

**Next topic:**[Configure Eligibility Rules Engine Policies in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-config-gmp-eligibility.md)

