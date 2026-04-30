---
title: Major Security Incident Management administration
description: Plan and configure your Major Security Incident Management implementation.Enable users to decide to propose or promote incidents as major security incidents. Easily track all incidents related to a major security incident by enabling security incidents to be linked to the parent or child incident.Tag or label the security incidents or vulnerable records to a major security incident when the incident is proposed or promoted. If a security incident is proposed then the incident record is referred as major security incident candidate. When a security is promoted then the incident record is referred as Major Security Incident with state as Accepted.Configure labels in major security incident management to create custom labels and filter the external collaboration activities and tasks in the activity stream. The different types of implemented labels are State labels and timeline labels.Configure different types of labels to better filter and also indicate the incident states. Major security incident labels provide the flexibility to label the collaboration activities and tasks of the incident records.Configure and assign Timeline categories such as Threat, Response, or Custom to your major security incidents using the Timeline section on the Overview tab.Automate the email notification process and notify the users when a security incident is either proposed or promoted to a major security incident candidate.Establish actions that will occur automatically when a major security incident is closed. Increase security by automatically archiving and removing access to folders containing resolution information.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Major Security Incident Management administration

Plan and configure your Major Security Incident Management implementation.

You can configure the following aspects of Major Security Incident Management administration:

**Parent Topic:**[Major Security Incident Management](../reference/major-security-incident-management-landing-page.md)

## Enable proposal, promotion, and linking of major security incidents

Enable users to decide to propose or promote incidents as major security incidents. Easily track all incidents related to a major security incident by enabling security incidents to be linked to the parent or child incident.

### Before you begin

Role required: sn\_msi.workspace\_admin

### Procedure

1.  Navigate to **All** &gt; **Major Security Incident Management** &gt; **MSI Administration** &gt; **Configurations**.

2.  Enable users to propose a security incident to a major security incident by selecting the **Propose Major Security Incident** check box in the SIR/VR Workspace Actions section.

3.  Enable users to promote a security incident to a major security incident by selecting the **Promote to Major Security Incident** check box.

4.  Enable linking a security incident to a major security incident so they can be tracked together by selecting the **Link to Major Security Incident** check box.

5.  Select **Update**.


## Tag security incidents as major security incidents

Tag or label the security incidents or vulnerable records to a major security incident when the incident is proposed or promoted. If a security incident is proposed then the incident record is referred as major security incident candidate. When a security is promoted then the incident record is referred as Major Security Incident with state as Accepted.

### Before you begin

Role required: sn\_msi.workspace\_admin

### Procedure

1.  Navigate to **All** &gt; **Major Security Incident Management** &gt; **MSI Administration** &gt; **Configurations**.

2.  Enable **Display Labels** check box to label the proposed incident candidate as major security incident by selecting the **Label Name - Propose As Candidate** lookup field and select Major Security Incident Candidate in the **SIR/VR Workspace Labels** section.

3.  Enable **Display Labels** check box to label the promoted incident candidate as major security incident by selecting the **Label Name - Promotion to Major Security Incident** lookup field and select Major Security Incident in the **SIR/VR Workspace Labels** section.

4.  Select **Update**.


## Configure labels for major security incidents

Configure labels in major security incident management to create custom labels and filter the external collaboration activities and tasks in the activity stream. The different types of implemented labels are State labels and timeline labels.

### Before you begin

Role required: sn\_msi.workspace\_admin

### Procedure

1.  Navigate to **All** &gt; **Major Security Incident Management** &gt; **MSI Administration** &gt; **Configurations**.

2.  Enable **Display Labels** check box to enable labeling different incident states such as Analysis, Contain, Eradicate, Recover, Review, Timeline Event in the **MSIM Workspace Labels \(Display on Collaboration Activities and Tasks\)** section.

3.  Select **Update**.


## Configure labels for major security incidents

Configure different types of labels to better filter and also indicate the incident states. Major security incident labels provide the flexibility to label the collaboration activities and tasks of the incident records.

### Before you begin

Role required: sn\_msi.workspace\_admin

You can select or deselect the labels using the labels icon that is available on the Activity stream section of the Collaboration and Task organizer section of the MSIM workspace.

### Procedure

1.  Navigate to **All** &gt; **Major Security Incident Management** &gt; **MSI Administration** &gt; **MSI Labels**.

2.  Click **New** to create a new label.

3.  Fill the form with **Label Name** and **Label Color**.

4.  Click **Create Label**.

5.  As a part of the base system, the following are the configured labels for each incident state and you can't modify the label name or color:

    -   Analysis
    -   Contain
    -   Eradicate
    -   Review
    -   Recover
    -   Timeline Event
    **Note:** You can modify the custom labels and its properties.


## Configure timeline categories for major security incidents

Configure and assign Timeline categories such as Threat, Response, or Custom to your major security incidents using the Timeline section on the Overview tab.

### Before you begin

Role required: sn\_msi.workspace\_admin

### Procedure

1.  Navigate to **All** &gt; **Major Security Incident Management** &gt; **MSI Administration** &gt; **Timeline categories**.

    The following timeline categories are provided as a part of the base system:

    -   **Custom**.
    -   **Response**.
    -   **Threat**.
2.  To modify an existing Timeline event category, perform the following steps:

    1.  Select a Timeline event category from the list.

    2.  You can modify the name of the Timeline event category.

    3.  You can modify the Event Color and select another color for your Timeline event category.

    4.  Select **Update**.

3.  To create a new Timeline event category, perform the following steps:

    1.  Select **New**.

    2.  In the Name field, enter a name for the Timeline event category.

    3.  In the Event Color field, choose a color for the event timeline category using the drop-down list.

    4.  Select **Submit**.


## Set notification preferences for MSIM

Automate the email notification process and notify the users when a security incident is either proposed or promoted to a major security incident candidate.

Role required: sn\_msi.workspace\_admin.

The notifications are triggered only when a security incident is proposed and sent to all those users and groups who are configured to the notifications list. By default, the email notification is received by the user who had proposed the security incident as a major security incident candidate.

**Notification: Security Incident proposed \(SI\) as Major Security Incident \(MSI\)**

Who will receive:

-   By default, **MSI Reviewers** group name is created and any user who is added to this group will be privileged to be a **MSIM Manager** and the users who are under that group will receive the notification emails.
-   Any specific user who is added to the **Users** list will also receive the notification emails.

What will it contain:

If you want to modify the email contents such as body of the email which includes the Subject or Message HTML, you must have the System Administrator role access or assigned as System Administrator and not an MSI Administrator.

![Notification SI proposed to MSI](../../security-incident-response/image/notification-si-proposed-msi.png)

**Notification: Security Incident promoted \(SI\) as Major Security Incident \(MSI\)**

This notification is triggered when a security incident is promoted and when the File Explorer and Microsoft Teams base structure is created. By default, this notification is received by the user who had promoted the security incident to a major security incident.

**Who will receive**

-   By default, a **Group** by name **MSI Responder** is created and any user who is added to this group will be privileged to have **MSIM Responder** role and all the users who are under that group will receive the notification email.
-   Any specific user who is added to the **Users** list will also receive the notification emails.

**What will it contain**

If you want to modify the email contents such as body of the email, which includes the Subject or Message HTML, you must have the System Administrator role access or assigned as System Administrator and not an MSI Administrator.

![Notification SI Promoted to MSI](../../security-incident-response/image/notification-si-promoted-msi.png)

## Configure MSI closure activities

Establish actions that will occur automatically when a major security incident is closed. Increase security by automatically archiving and removing access to folders containing resolution information.

### Before you begin

Role required: sn\_msi.workspace\_admin

### Procedure

1.  Navigate to **All** &gt; **Major Security Incident Management** &gt; **MSI Administration** &gt; **Configurations**.

2.  Archive chat communications related to resolve the incident by selecting the **Archive Collaboration Channels** check box in the Automated Closure Actions section.

3.  Remove folders containing material related to resolving the incident by selecting the **Remove Collaboration Folders** check box.

4.  Select **Update**.


