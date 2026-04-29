---
title: Configure pre-eligibility questions in Grants Management
description: The Grants Management Program Setup enables grant program managers to use decision trees to define a series of pre-eligibility questions to check if the applicants qualify for the program.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure pre-eligibility questions in Grants Management

The Grants Management Program Setup enables grant program managers to use decision trees to define a series of pre-eligibility questions to check if the applicants qualify for the program.

## Before you begin

Role required: admin

The Grants Management incorporates the use of pre-eligibility criteria, a series of questions that may be posed to an applicant to determine whether they are eligible to apply for a grant. The purpose is to deflect proposals in which the applicant is not eligible to obtain a grant.

To configure the Pre-Eligibility questions for a new Grant Program:

## Procedure

1.  Open the Grants Management, and navigate to the **Configure Application** stage.

2.  Select which Guided Decision tree the applicant should see in the Eligibility Questions questionnaire before the proposal is started.

    To create a new questionnaire, select **Open the Decision Trees list**.

3.  Select **New** to open a new Decision Tree record form where you can define the details of your decision tree.

4.  On the form, fill in the fields.

5.  Select **Submit** to create the decision tree record.

6.  Select **Open in Builder** to open the Decision Tree builder, where you can add questions, define branching logic, and set eligibility criteria.

7.  Select the **New** node and enter the Node name and select the relevant reference table.

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

![eligibility questions](../image/psds_grants_program_elig_q.png)

When applicants proceed to answer eligibility questions, they are presented with the questionnaire that you have just created using the decision tree. Based on their responses:

-   If eligible, they will see a success message and the option to proceed with their proposal
-   If not eligible, a message will indicate that they may not be eligible and suggest reviewing their answer.

