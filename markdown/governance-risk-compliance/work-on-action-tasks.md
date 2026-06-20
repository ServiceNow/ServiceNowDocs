---
title: Complete action tasks and report incidents associated with regulations
description: Report incidents or security incidents associated with multiple regulations for various legal entities. The automated workflow generates regulatory reporting assessments of IT incidents, and Digital resilience incident \(DRI\) Initial, Intermediate, and Final reports, all within regulatory timelines. Complete the action tasks and generate reports in Microsoft Word format, as required by regulatory authorities for analysis.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/governance-risk-compliance/work-on-action-tasks.html
release: xanadu
topic_type: task
last_updated: "2025-11-17"
reading_time_minutes: 5
breadcrumb: [Reporting incidents or security incidents for multiple regulations, Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Complete action tasks and report incidents associated with regulations

Report incidents or security incidents associated with multiple regulations for various legal entities. The automated workflow generates regulatory reporting assessments of IT incidents, and Digital resilience incident \(DRI\) Initial, Intermediate, and Final reports, all within regulatory timelines. Complete the action tasks and generate reports in Microsoft Word format, as required by regulatory authorities for analysis.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

**Note:** The regulation status, previously a field on the Digital resilience incident reporting \(DRIR\) case form, is now displayed within the Regulations related list.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Digital resilience incident reporting** &gt; **All incident reporting cases**.

2.  Open the incident reporting case from the list that you want to work on.

    From the Digital resilience incident reporting cases in the instance, DRI0001003 is selected for this example.

    \[Omitted image "drir-cases-created-opres.png"\] Alt text: Cases.

    Its automated workflow generates the Regulatory reporting assessment of IT incidents, DRI Initial report, DRI Intermediate report, and DRI Final report action tasks.

3.  Review the incident record's 'Action tasks' and 'Regulations' related lists for assigned tasks and mapped regulations.

    The examples show that an action task is assigned automatically.

    \[Omitted image "ent-acer-w-dora-regulation.png"\] Alt text: Action task is assigned automatically to the case.

    A regulation is mapped to the case.

    \[Omitted image "ent-acer-w-dora-regulation-mapped.png"\] Alt text: Regulation is mapped to the case.

4.  Review the details of the Digital resilience incident reporting case and verify that the owner of the case is a member of the assignment group.

    A sample Digital resilience incident reporting incident is shown where the source is Incident, Source record is in the New state, the source record is an Incident INC0010005, and the date of discovery is listed. The case is assigned to the 'Digital Resilience Incident Managers' assignment group.

    \[Omitted image "inci-assigned.png"\] Alt text: Incident assigned.

5.  As a Digital Resilience Incident Manager, log in to the case record, assign it to an analyst from your group, and select **Save**.

    The example shows that an analyst, Opres manger01, is assigned to the 'Digital resilience incident reporting: Facility issue' case.

    \[Omitted image "dri-case-to-analyst.png"\] Alt text: Case assigned.

    As the assigned analyst, you can begin working on the action tasks.

6.  Open the first action task in the case and verify that it’s assigned to a user.

7.  Update the state of the action task to **Assigned**.

    The example shows that the 'Regulatory reporting assessment of IT incidents' action task is updated to the **Assigned** state.

    \[Omitted image "update-state-assigned.png"\] Alt text: Action task state is updated.

    \[Omitted image "act-task-assigned.png"\] Alt text: Action task is in the assigned state.

8.  Select **View assessment** and then select **Start** in the assessment section of the action task.

    **Note:** The **View assessment** UI action is displayed only when the action task is in the **Assigned** state.

    As an analyst, you can start the assessment as shown in the example.

    \[Omitted image "asmt-section-of-action-task.png"\] Alt text: Start the assessment.

9.  Respond to the questions in the assessment template.

    **Note:** You can trigger the assessment from an incident or a security incident.

    Sample assessment questions and answers are shown in the example.

    \[Omitted image "act-t1-asmt-q.png"\] Alt text: Sample assessment questions and answers.

10. To submit the responses to the questions, select **Submit** and respond to the confirmation message by selecting **Submit** again.

    The assessment submission form is shown in the example.

    \[Omitted image "act-task-submit-asmt.png"\] Alt text: Submit the assessment.

    When you complete the assessment, its state is shown as **Completed** in the **Assessment** tab.

    \[Omitted image "act-task-asmt-comp.png"\] Alt text: Assessment completed.

    The assessment is pending for review and the state is updated to **Review** as shown in the action task.

    \[Omitted image "act-task-asmt-pending-review.png"\] Alt text: Pending for review.

    Once the assessment is submitted, the regulation status is updated to 'Reportable' as shown in the Regulations related list.

    \[Omitted image "regu-reportable.png"\] Alt text: Reporting status is updated to Reportable.

    In this example, the action task CCT002001 is in the 'Review' state, while CCT002002 for 'DRI Initial report' has been created automatically.

    \[Omitted image "act-t2-created.png"\] Alt text: Second action task is created.

11. As a reviewer of the action task, log in and complete the review.

12. Assign the second action task, 'DRI Initial report', to a user from the assignment group, update its state to **Assigned**, and select **View assessment** to respond to the assessment.

13. Complete the review and submit the assessment for the 'DRI Initial report' action task.

    The next action task, 'DRI Intermediate report' is created automatically.

14. Assign the 'DRI Intermediate report' action task to a user from the assignment group, update its state to **Assigned**, respond to the questions, complete the review, and submit the assessment for the 'DRI Intermediate report' action task.

    The next action task, 'DRI Final report' is created automatically.

15. Assign the 'DRI Final report' action task to a user from the assignment group, update its state to **Assigned**, respond to the questions, complete the review, and submit the assessment for the 'DRI Final report' action task.

    The action task, 'DRI Final report' is complete.

    You have now completed all action tasks required for reporting the incident or security incident mapped to the regulation.

16. To generate the report of an action task in Microsoft Word format, select **Generate MS Word**.

    Action task reports must be generated in Microsoft Word format as required by regulatory authorities for analysis. When you select the **Generate MS Word** UI action, the Generate report window is displayed.

    1.  In the Generate report window, choose the desired Word template in the **Report template** field.

    2.  Add the name of the report in the **Name of report** field.

        The example shows the Word template and sample name of the report.

        \[Omitted image "act-task-word-report.png"\] Alt text: Generate report UI action.

    3.  Select **Generate**.

        A message is displayed that the report is being generated.

    The action task report is generated in the Microsoft Word format. It includes information from the **Details** and **Assessments** tabs and attachments. It includes information such as form sections, questions, template sections, question answers, and attachment links as shown in the examples.

    \[Omitted image "word-rep-1.png"\] Alt text: Word report sections.\[Omitted image "word-rep-2.png"\] Alt text: Details of Word report.

    For information on Word templates and Template configurations, see [Generating Word reports using Document designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/governance-risk-compliance/gen-word-reports.md).

    The generation of Microsoft Word reports, required by regulatory authorities for analysis in Digital resilience incident reporting, is completed with this step.

17. To export the report of the action task to your local drive, select **Export**.

18. To save the action task in the instance, select **Save**.

    Saving the action task in the instance completes the required reporting workflow.


