---
title: Resolve security threats with the playbook
description: Use the Playbook to resolve certain types of security threats in a step-by-step manner. For example, you can resolve phishing attacks and threats caused by malicious code activity using playbooks.The Phishing playbook guides you through the tasks necessary for analyzing and resolving a phishing attack reported by one of your company's employees.As you analyze security threats using the Security Incident Response playbook, you can view knowledge articles for each task if defined by your organization. If knowledge articles are not present, you can create them and associate them with playbook tasks.The Security Analyst Workspace base system includes a series of tasks for each threat category. You can create custom tasks that meet the unique needs of your system or customers.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Manage security threats using the Security Analyst Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Resolve security threats with the playbook

Use the Playbook to resolve certain types of security threats in a step-by-step manner. For example, you can resolve phishing attacks and threats caused by malicious code activity using playbooks.

## Before you begin

Role required: sn\_si.admin or admin

## About this task

Each group of tasks \(Analysis, Contain, and so forth\) leads you through a series of questions and other activities for resolving the threat.

![Playbook example](../image/add-task-button-callout.png "Playbook")

As you work through each task, enter work notes to help analyze similar attacks in the future. After a threat is identified, you can also use information in the playbook to quarantine the threat, isolate similarly affected assets, and remove malware.

Knowledge articles, included in each task, provide tips and other information to help you perform the needed steps.

![Knowledge article in support of phishing task](../image/multiple-outcomes.png "Knowledge articles")

The base system includes knowledge articles for each of the playbook tasks. You can, however, [write your own knowledge articles](t_CrtScrIncdtKnwArt.md) and [associate them to playbook tasks](use-the-playbook.md#).

**Note:** For an example of how to use the playbook to analyze and resolve a specific threat, see [Resolving user-reported phishing attacks with the playbook](use-the-playbook.md#).

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents \(New UI\)**.

    The Security Incidents screen shows security incidents that have been assigned to you.

    ![Security incidents](../image/cj-sir-si-list.png)

2.  You can click the **Assigned to me** choice list to select a different filter, such as all open incidents or all unassigned incidents.

    Alternatively, you can click one of the Quick Filters to view security incidents of a particular type, such as only Critical incidents.

3.  Click the security incident you want to analyze.

    Consider prioritizing security incidents with high [risk scores](../reference/setup-assistant-reference.md#).

4.  If the playbook pane on the right-hand edge of the screen is closed, click the playbook icon \(![Playbook](../image/cj-sir-icon-playbook.png)\) to open it.

    If no playbook is assigned to the security incident, you can select a playbook from the Selected Playbook choice list as shown below:

    ![Select playbook](../image/cj-sir-playbook-select.png)

    You can also assign a different playbook to the security incident. To include a playbook in the Selected Playbook choice list or to change the playbook for a security incident, see [Enable playbooks for analyst selection](../concept/sir-new-ui-add-playbook.md) for details.

    The playbook specific to the type of security threat opens. It is divided into categories of similar tasks. For example, you use the tasks in the **Analysis** group to determine the validity and scope of the threat. The **Contain** group includes tasks for isolating the threat to a specific user or asset. The tasks in the **Eradicate** group guide you through the process of removing the malware or reimaging the host.

5.  Click the first group \(**Analysis**\), and then click the first task in the playbook.

6.  Follow the prompts in the task.

    -   Some tasks ask a question, such as "Is Email Part of Campaign?" Perform the necessary analysis to answer the question, and select **Yes** or **No**.
    -   If you have [defined knowledge articles and associated them with playbook tasks](use-the-playbook.md#), the articles appear when you start work on a task.
    -   Some tasks are transitional. They simply instruct you to perform an action, such as adding observables to a security incident. After you complete the action, click **Mark as Completed**.
    As you complete tasks, subsequent tasks are presented to you based on the choices you make. Grayed out groups \(such as **Recover**, **Review**, and so forth\) may be activated by your choices.

7.  Continue working on each task presented to you until you have completed all tasks to resolve the threat and close the security incident.


**Related topics**  


[Add a custom task to the playbook](use-the-playbook.md#)

## Resolving user-reported phishing attacks with the playbook

The Phishing playbook guides you through the tasks necessary for analyzing and resolving a phishing attack reported by one of your company's employees.

### How security incidents are created from user-reported phishing attacks

During Security Incident Response setup, your system administrator creates a series of [email matching rules](../reference/setup-assistant-reference.md#) that can identify emails that contain signs of a phishing attack. When employees receive a suspicious email that contains the common signs of a phishing attack \(as defined by your security policies\), they can send it as an .EML attachment to the phishing email address defined by your organization.

When the email is received at the phishing email address, the .EML attachment is parsed and its information is compared to the email matching rules. If a match is found, a security incident containing the following information is created:

-   The short description includes User Reported Phishing, followed by the actual subject from the originating email.
-   The .EML file is attached to the security incident.
-   If the .EML contained any observables, they are parsed, and enrichment and threat lookups are automatically performed.

![User reported phishing security incident](../image/cj-sir-phishing-callouts.png "User Reported Phishing")

When a Phishing category security incident is opened, the Phishing Playbook is automatically available. Simply click the playbook icon \(![Playbook](../image/cj-sir-icon-playbook.png)\) to open the playbook.

![Phishing playbook pane](../image/cj-sir-phishing-playbook.png "Phishing Playbook")

The Phishing playbook contains tasks to help you analyze, contain, and eradicate a phishing threat. The tasks are organized into states \(for example, **Analysis**, **Contain**, and so forth\). When all tasks for a state have been completed, the playbook guides you to the next state.

### Analyzing security incident details

When the security incident is in the Analysis state, you are given tasks to perform basic investigation of the incident, including:

-   Determining the validity of the incident.
-   Studying the impact of the potential threat.
-   Coordinating an effective response to the incident.

As you work through the tasks:

-   Familiarize yourself with the knowledge articles.
-   Open the email attachment and examine it for signs of common phishing elements.
-   Review threat lookup results.

### Containing the security incident

When the security incident is in the **Contain** state, you are given tasks to review the details of the email. To ensure that threats cannot enter your organization, update your network defenses, in the form of Intrusion Defense System \(IDS\) and Intrusion Prevention System \(IPS\) signatures and rules.

As you work through the tasks:

-   Take actions to limit threat impacts, such as isolating the impacted devices.
-   Examine the observables attached to the email.
-   Determine whether any email contents are associated with a known threat, including:
    -   URL
    -   Email sender
    -   Phishing URL
    -   IP address of the sender's SMTP server

### Eradicating the malware

After you deploy updated signatures and rules to your antivirus solution, use the tasks in the **Eradicate** state to determine if malware is present and handle it accordingly.

As you are work through the tasks:

-   Scan the endpoints of affected devices for the presence of malware.
-   Remove any malware found.
-   As a last resort, wipe and reimage the host devices.

### Reviewing the security incident

If you have determined that a phishing attack was a false alarm when performing the Analysis tasks, the security incident moves to the **Review** state and you need to notify your users so they know it is safe to open the email attachment.

### Closing the security incident

When all tasks in the playbook have been completed, the security incident is moved to the **Closed** state. You must enter closing comments before the incident can be closed.

### Cancelling a security incident

When a security incident is in the **Review** state, and you have successfully informed your users that the email is not a threat, the **Cancelled** state becomes active and you can cancel the security incident.

**Note:** The Recover task is not used in the Phishing playbook.

## Associate a knowledge article with a playbook task

As you analyze security threats using the Security Incident Response playbook, you can view knowledge articles for each task if defined by your organization. If knowledge articles are not present, you can create them and associate them with playbook tasks.

### Before you begin

As you use the playbook in Security Incident Response, take note of the text associated with each task. For example, the first task in the Phishing category is **Was Alert Employee-Submitted?** This is the short description of the task and you need this text \(exactly as it appears in the playbook\) to associate a knowledge article with the task.

Role required: sn\_sir.knowledge\_admin, and either sn\_si.admin or admin

### Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Catalog &amp; Knowledge** &gt; **Knowledge**.

2.  Create and publish a knowledge article for a specific playbook task.

3.  Navigate to **Security Incident** &gt; **Manual Runbook** &gt; **Create New Runbook**.

4.  Create a runbook, filling in the following information:

<table id="table_qfl_nwk_cp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge article

</td><td>

Select the published knowledge article you want to associate with the playbook task.

</td></tr><tr><td>

Table

</td><td>

Select Security Incident Response Task \[sn\_si\_task\].

</td></tr><tr><td>

Condition

</td><td>

Set the condition builder to:-   **Option:** Select **Short description**.
-   **Operator:**Select **is**.
-   **Input value:** Enter the short description for the task, exactly as it appears in the playbook.


</td></tr></tbody>
</table>5.  Click **Submit**.

    The next time you run the playbook and select this task, the associated knowledge article is displayed.


**Related topics**  


[Create a security incident knowledge article](t_CrtScrIncdtKnwArt.md)

[Create a Security Incident Response runbook](../reference/setup-assistant-reference.md#)

## Add a custom task to the playbook

The Security Analyst Workspace base system includes a series of tasks for each threat category. You can create custom tasks that meet the unique needs of your system or customers.

### Before you begin

Role required: sn\_si.basic or security\_admin

### Procedure

1.  With the playbook open, click **Add Task**.

    ![Click the Add Task button](../image/add-task-button.png)

    The Add Custom Task screen opens.

    ![Add a custom playbook task](../image/add-playbook-task.png)

2.  Fill in the fields, as needed.

<table id="table_l2p_dcs_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

\[Read only\] The automatically-generated security incident task number.

</td></tr><tr><td>

Parent

</td><td>

The number of the related security incident.

</td></tr><tr><td>

Configuration item

</td><td>

The configuration item affected by the security issue, if any.

</td></tr><tr><td>

Affected user

</td><td>

The user affected by the security issue, if any.

</td></tr><tr><td>

Priority

</td><td>

Select the priority used to determine when this task should be performed.

</td></tr><tr><td>

Security Incident State

</td><td>

The current state of the security response task. You can select a future state, if needed.

</td></tr><tr><td>

Outcome type

</td><td>

If you have the sn\_si.basic role, select **Yes/No** as the outcome type. If you have the security\_admin role, you can create a custom outcome type with multiple custom output values. For example, you can define a task with dependant values based on the threat category. For more information, see [Choice lists](https://www.servicenow.com/docs/access?context=t_ViewChoiceListDefinitions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

</td></tr><tr><td>

Assignment group

</td><td>

The assignment group from which the assigned worker will be selected.

</td></tr><tr><td>

Assigned to

</td><td>

The individual assigned to perform the task.

</td></tr><tr><td>

Short description

</td><td>

A description of the Security Incident playbook task.

</td></tr><tr><td>

Description

</td><td>

Enter a description for the selected task.

</td></tr></tbody>
</table>3.  When you have completed your entries, click **Add Task**.

    The task is inserted in the playbook following the current task.


