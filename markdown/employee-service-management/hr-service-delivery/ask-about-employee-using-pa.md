---
title: Ask about the employees you support
description: As an HR business partner, query the HRBP productivity assistant for employee HR profiles, work history, reporting structure, span of control, new hires, and leaves of absence. You can also search knowledge articles using the user criteria of an employee within your data access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/ask-about-employee-using-pa.html
release: brazil
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-09-17"
reading_time_minutes: 3
keywords: [HRBP productivity assistant, employee profile, work history, org structure, new hires, employees on leave, span of control]
breadcrumb: [Use, HRBP productivity assistant, HR Service Delivery, Employee Service Management]
---

# Ask about the employees you support

As an HR business partner, query the HRBP productivity assistant for employee HR profiles, work history, reporting structure, span of control, new hires, and leaves of absence. You can also search knowledge articles using the user criteria of an employee within your data access.

## Before you begin

Role required: HR business partner \[sn\_hrbp\_hub.user\]

## Procedure

1.  Open the EmployeeWorks Web App.

2.  In the side navigation, under Assistants, select **HRBP Productivity Assistant**.

    If the assistant isn't listed, select **Browse assistants** and then select the **HRBP Productivity Assistant** card.

3.  In the message field, request information about an employee or a group of employees.

<table id="choicetable_dkf_hnr_skc"><thead><tr><th align="left" id="d411928e120">

Option

</th><th align="left" id="d411928e123">

Description

</th></tr></thead><tbody><tr><td id="d411928e129">

**Employee details**

</td><td>

Tell the assistant to get details about an employee, such as title, department, manager, location, and skills.For example, type `Get me details about Abel Tuter`.

</td></tr><tr><td id="d411928e143">

**Work history**

</td><td>

Tell the assistant to show the job history of an employee, including position, business title, department, manager, start and end dates, duration, and whether each job is current.For example, type `Can you pull up Abel Tuter's work history?`

</td></tr><tr><td id="d411928e156">

**Reporting structure**

</td><td>

Tell the assistant to show who reports to a manager. Results include direct reports and their direct reports. For example, type `Who reports to Beth Anglin?`

To view direct reports only, type `Who directly reports to Beth Anglin?`

</td></tr><tr><td id="d411928e173">

**Managers with the largest organizations**

</td><td>

Tell the assistant to rank the managers within your data access by total organization size, including indirect reports.For example, type `Which managers have the largest span of control?`

</td></tr><tr><td id="d411928e187">

**New hires**

</td><td>

Tell the assistant to show new hires within your data access, most recent first. If you don't specify a time period, results cover the last 30 days.For example, type `Who joined in the last 2 months?`

</td></tr><tr><td id="d411928e200">

**Employees on leave**

</td><td>

Tell the assistant to show employees within your data access who are on approved leave of absence, grouped by leave type. If you don't specify a date range, results include employees whose leave period includes the current date.For example, type `Who's currently on leave on my team?`

</td></tr><tr><td id="d411928e213">

**Knowledge articles**

</td><td>

Tell the assistant to find knowledge articles on a subject that an employee can view. Use this option to confirm which articles an employee can open before you refer them to one.For example, type `What does Abel Tuter see about parental leave?`

</td></tr></tbody>
</table>    Requests for managers with the largest organizations, new hires, employees on leave, and knowledge articles return results only for employees within your data access. For more information, see [Define HRBP data access and data access rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown).

    The requested information appears in the conversation.

4.  If more than one employee matches the name that you specified, specify the employee.

    Matching employees are listed by name and email address. For example, type the email address of the employee.

    The information for the specified employee appears in the conversation.

5.  If the response indicates that more results are available, request the remaining results.

    Employee details display three skills at a time. The list of managers with the largest organizations displays 10 managers at a time. For example, type `Show me the rest`.

    The remaining results appear in the conversation.

6.  If you requested knowledge articles, select an article link.

    Knowledge article results exclude articles that the employee can't view, even if you can view them. If the employee is outside your data access, no knowledge articles are returned. To get a summary instead, ask about the content of an article. For example, type `Summarize the parental leave article`.

    The article opens beside the conversation.


## Result

**Important:** Always review AI-generated content for accuracy.

