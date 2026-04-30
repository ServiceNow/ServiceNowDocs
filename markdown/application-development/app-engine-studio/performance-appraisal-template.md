---
title: Performance Review template
description: Build an application in App Engine Studio \(AES\) using the Performance Review template to automate scheduling, notifications, and feedback for performance reviews.The following tables, experiences, automated workflows, and roles are included in the Performance Review template for App Engine Studio \(AES\).
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Available templates, Create your app using an application template, Create your app, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Performance Review template

Build an application in App Engine Studio \(AES\) using the Performance Review template to automate scheduling, notifications, and feedback for performance reviews.

To use the Performance Review template, install this application from the ServiceNow Store.

![Performance Review template](../image/template-performance-review.png)

A performance review app automates the process of scheduling annual or quarterly reviews, reviewing employee performance, and providing manager feedback. The app displays report information by default and lets managers view, update, and request employee performance reviews.

Employees can complete their self-evaluation, monitor the status, and confirm evaluations via a web portal. The app will automatically notify employees and managers to submit their evaluations.

Managers can request an update to the self-evaluations, submit manager-evaluations, confirm evaluations, and monitor the status of their team's submissions via a portal.

The HR/admin role can select an annual, bi-annual, or quarterly review process schedule and edit both the self-evaluation and manager-evaluation templates. HR/admins can monitor the status of all evaluations by department, organization, or manager.

You can improve this template by incorporating the following features:

-   Add continuous option as a review process
-   Use Playbook to manage review schedules
-   Include HR review/escalation process for both self-reviews and manager reviews
-   Add peer reviews process
-   Add goal setting or objectives and key results \(OKRs\)
-   Add integration with HR software
-   Add skill set assessment metrics
-   Add performance improvement plan \(PIP\) process/individual development plans
-   Include compensation info/annual performance review \(APR\)

For more information on creating an application using a template, see [Create your app using an application template](../task/use-app-template.md).

**Parent Topic:**[Available templates](template-library.md)

## Performance Review template contents

The following tables, experiences, automated workflows, and roles are included in the Performance Review template for App Engine Studio \(AES\).

### Tables in the Performance Review app template

<table id="table_r4y_2zs_j4b"><thead><tr><th>

Table label \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Performance Review Table\[x\_&lt;company-code&gt;\_&lt;my performance\_review\_app&gt;\_performance\_review\]

</td><td>

Track the performance evaluations created by employees and managers. For example, the employee name, state of the review, manager feedback, and state of the review.

</td></tr></tbody>
</table>### Experiences in the Performance Review app template

|Experience|Experience type|Description|
|----------|---------------|-----------|
|Performance Review \| Edit Settings|Form|Form where managers can configure performance review settings and add notifications.|
|*App name* \| Workspace|Workspace|Workspace where admins and managers can configure review schedules, update evaluation templates, and monitor the status of all evaluations.|
|Performance Review Test \| Emp Mgr feedback|Form|Form for managers to create employee evaluation questions, monitor the status, and leave feedback.|
|Performance Review \| Manager Review|Form|Form managers can use to include questions, review employees responses, and leave feedback.|
|Performance Review \| Self Review WS|Form|Form for employees to complete self review questions.|
|Performance Review \| Workspace|Form|Form for mangers to monitor the status of their team's submissions.|
|*App name* \| Portal|Portal|Portal where employees can submit, update, review, and confirm evaluations.|
|Performance Review \| Default View|Form|Form that managers and employees can use to view performance reviews.|
|Performance Review \| Self Review|Form|Form employees and managers can use to submit a self-assessment of their performance.|
|Mobile app|Mobile experience|Employees can access their performance reviews using your organization's iOS or Android app.|

### Automated workflows in the Performance Review app template

|Workflow name|Workflow type|Description|
|-------------|-------------|-----------|
|Perf Review - Send PR Employee Update Self-Eval email|Flow - record|Triggers the PR Employee Update Self-Eval email.|
|PR Employee Manager - Eval submitted|Email|Notifies managers that an evaluation has been submitted.|
|Perf Review - Send PR Employee Complete Evaluation email|Flow - record|Triggers the PR Employee Complete Evaluation email.|
|PR Employee Manager - Eval submitted DJ|Email|Notifies managers when self-evaluations are submitted.|
|PR Admin Eval Deadline Passed|Email|Notifies admins when an evaluation deadline has passed.|
|PR Reminder: Manager need to submit eval|Email|Reminds managers to submit their evaluations.|
|PR Manager Self Evaluation Submitted|Email|Notifies admins that managers have submitted self-evaluations.|
|Perf Review - Send PR Employee Manager - Eval submitted|Flow - record|Triggers the PR Employee Manager - Eval submitted email.|
|PR Reminder - Employee Self Evaluation|Email|Notifies employees to submit self-evaluation.|
|Perf Review - Send deadline email|Flow|Triggers a deadline reminder email on the date indicated in the system properties.|
|PR Employee Complete Evaluation|Email|Notifies employees their evaluation is complete.|
|PR Employee Update Self Evaluation|Email|Notifies employees they need to update their self-evaluation.|
|Perf Review - Main Flow|Flow|Controls when reviews are triggered, email reminders, and end of review period is reached. This is the main flow that triggers daily.|
|Perf Review - Send reminder emails|Flow|Triggers reminder emails on the date indicated by sys\_properties.|
|Perf Review - Create records|Flow|Triggers review records on the date indicated by sys\_properties.|
|Perf Review - Set review inactive|Flow|Inactivates reviews on the end date of the review period, specified in sys\_properites.|
|PR Admin Self - Eval Submitted w/o Manager|Email|Notifies admins if a self-evaluation is submitted without a manager or title.|
|PR Reminder Employee Update Self Eval|Email|Notifies employees to update self-evaluation.|
|Perf Review - Send Manager/Admin Self-Evaluation Submitted email|Flow - record|Triggers the PR Admin Self-Evaluation Submitted without manager or the PR Manager Self Evaluation Submitted email.|

### Roles in the Performance Review app template

<table id="table_ipv_j1t_j4b"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Employee\[x\_&lt;company-name&gt;\_ &lt;my performance\_review\_app&gt;.employee

</td><td>

Employees can complete/update self-evaluations and confirm evaluations.

</td><td>

Read \(own\) and Update \(own\)

</td></tr><tr><td>

HR/Admin\[x\_&lt;company-name&gt;\_ &lt;my performance\_review\_app&gt;.admin

</td><td>

HR/Admins can schedule reviews \(annual, bi-annual, custom, or manual\), edit self and manager evaluation templates, and monitor the status of all reviews.

</td><td>

Create, Read \(own\), Update \(own\), Delete \(all\)

</td></tr><tr><td>

Manager\[x\_&lt;company-name&gt;\_ &lt;my performance\_review\_app&gt;.manager

</td><td>

Managers can request updates to a self-evaluation, submit manager-evaluations, and monitor issues related to evaluation submissions.

</td><td>

Read \(my team\) and Update \(my team\)

</td></tr></tbody>
</table>