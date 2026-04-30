---
title: Create security incidents from User Reported Phishing emails
description: Use this feature to create security incidents from user reported phishing emails.The User Reported Phishing feature available is an enhanced version of the existing user reported phishing functionality available. See Create rules to validate user-reported phishing attacks.As a user with the sn\_si.admin role, you can define email matching rules to filter user reported phishing emails based on specific criteria. For example, you can define a rule where all emails sent either directly or through the Report Phish button to security@acme.com are categorized as user reported phishing emails.Define the header information that must be captured from user reported phishing emails.User reported phishing emails are converted to security incidents based on the email matching rules that have been defined.The Transform Phishing Email to Security Incident flow converts or transforms phishing email records to security incidents.Phishing email records stored in the sn\_si\_phishing\_email table are converted to security incidents records.You can view security incidents associated with the phishing email records in the Security Analyst Workspace.This section covers some of the frequently asked questions about the enhanced User Reported Phishing feature.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 24
breadcrumb: [Security incident automatic creation, Security incident creation, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create security incidents from User Reported Phishing emails

Use this feature to create security incidents from user reported phishing emails.

The enhanced User Reported Phishing functionality includes aggregation capabilities, email header extraction, and configuration.

-   You can report phishing emails in multiple ways:
    -   Emails can be forwarded as attachments.
    -   If the **PhishAlarm** plugin \(previously known as Wombat\) is configured with the Microsoft Outlook client, you can:

        -   Select the **Report Phish** button.
        -   Forward phishing emails from a mobile device using the **Report Phish** option.
        ![Report phishing emails](../image/urp-report-phish.png)

    -   You can upload a phishing email \(in .eml format\).

        ![Report phishing emails as attachments](../image/urp-report-phish-1.png)

-   User reported phishing includes **aggregation business logic** that identifies duplicate phishing emails reported by users in an organization. Users can use this capability to:
    -   Aggregate duplicate or similar user reported phishing incidents \(company initiated phishing campaigns\).
    -   Avoid triaging duplicate user reported phishing incidents and reduce the manual effort involved in consolidating incidents.
    -   Enable security analysts to work on a single user reported phishing incident.
-   Provides phishing email headers within the user reported phishing incident.
    -   Security analysts can scan for key email header information within the incident.
    -   Manual effort in gathering header information from other sources is no longer required.
-   The original phishing email submitted is stored as a **Phishing Email Record** in a new table.
-   Security analysts can view details of the original phishing email like phishing email content, headers, origin.
-   Security administrators can configure and make certain enhancements that include:
    -   Configurations to extract email headers from the email body \(**Report Phish** submissions\).
    -   Filters to capture selected headers.
    -   Configurations to handle parent-child incident association when duplicate phishing email records are identified.
    -   Flow Designer configurations to modify aggregation business logic based on the requirements.

## Set up ingestion rules for user reported phishing

As a user with the `sn_si.admin` role, you can define email matching rules to filter user reported phishing emails based on specific criteria. For example, you can define a rule where all emails sent either directly or through the Report Phish button to `security@acme.com` are categorized as user reported phishing emails. For more information, see [Set up ingestion rules for User Reported Phishing](urp-about.md#).

## Define user reported phishing properties

Define the header information that needs to be captured from user reported phishing emails. For more information, see [Define User Reported Phishing properties](urp-about.md#).

## Phishing email records created from user reported phishing emails

User reported phishing emails are converted to security incidents based on the email matching rules that have been defined. For more information, see [Phishing email records created from user reported phishing emails](urp-about.md#).

## Transform phishing email to security incident

The Transform Phishing Email to Security Incident flow converts or transforms phishing email records to security incidents. For more information, see [Transform user-reported phishing emails to security incidents](urp-about.md#).

## Security incident records created from phishing email records

View the security incident record details including the Related Lists, Worknotes, and other important information. For more information, see [Security incident records created from phishing email records](urp-about.md#).

## Required components and plugins

The User Reported Phishing feature available is an enhanced version of the existing user reported phishing functionality available. See **Create rules to validate user-reported phishing attacks**.

**Important Installation Instructions**

This enhancement replaces the existing User Reported Phishing design. The new design includes the following updates:

-   The existing **User Reported Phishing** email inbound actions \(Type = Forward and Type = New\) have been disabled.
-   A new **Create Phishing Email** inbound action is now available.
-   The [Transform user-reported phishing emails to security incidents](urp-about.md#) is a new flow that contains the security incident creation and aggregation business logic for the new design. You must activate this flow for the new design to take effect.
-   The existing User Reported Phishing rules have been preserved during the upgrade.

**Note:** If you use custom email inbound actions and custom workflows for user reported phishing submissions, you must review both the old and new designs for conflicting or overlapping functionalities.

**User Reported Phishing Enhancement details**: The following are the details of the enhancement:

-   Reporting the phishing email in multiple ways: See [Create security incidents from User Reported Phishing emails](urp-about.md#) for the details. The phishing email is then moved to the `sn_si_phishing_email` table.
-   Creating phishing email records: If the email-matching rules are met \(See [Set up ingestion rules for User Reported Phishing](urp-about.md#)\), the **Create Phishing Email** inbound action creates a phishing email record. The parsed email headers are stored in the `sn_si_phishing_email_header` table and associated with the phishing email as a related list.
-   Aggregating similar phishing records into a single security incident: The [Transform user-reported phishing emails to security incidents](urp-about.md#) flow creates security incidents from the phishing email records and aggregates similar records into a single incident. The aggregation conditions can be modified as required in this flow.

**Note:**

-   The **User Reported Phishing** inbound actions available prior to the Security Incident Response 9.0 release are now disabled. Security incidents are no longer created through the disabled inbound actions.
-   The Security Operations spoke application must be installed for the new design to take effect. This includes the [Transform user-reported phishing emails to security incidents](urp-about.md#) flow which is available in an inactive state by default. Activate this flow to create security incidents from the phishing email records.

The following image shows the differences between the old and the new designs:

![User Reported Phishing: Differences](../image/urp-diff-image.png)

To use the enhanced User Reported Phishing feature, the following plugins and components are required:

-   Security Support Common \(`sn_sec_cmn`\): Includes:
    -   Inbound action
    -   New EmailUserReportedPhishing script
    -   Ingestion Rules table
-   Security Incident Response \(sn\_si\): Includes:
    -   Security incident table \(sn\_si\_incident\)
    -   Security phishing emails table \(sn\_si\_phishing\_email\)
    -   Security phishing email headers table \(sn\_si\_phishing\_email\_header\)
    -   EML upload record producer
-   Security Operations Spoke

    Flows and subflows for aggregating emails and transforming phishing emails to security incidents.


The following figure shows the new phishing emails table with references to the matched URP rule and target security incident record \(sn\_si\_incident\).

![URP Data model](../image/sec-inc-resp-datamodel.png)

## Set up ingestion rules for User Reported Phishing

As a user with the `sn_si.admin` role, you can define email matching rules to filter user reported phishing emails based on specific criteria. For example, you can define a rule where all emails sent either directly or through the Report Phish button to `security@acme.com` are categorized as user reported phishing emails.

### Before you begin

Role required: sn\_si.admin

### Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Email Processing** &gt; **Ingestion Rules - User Reported Phishing**.

2.  Click **New** to create a new Email Matching Rule.

3.  Enter a name and define one or more conditions for the rule.

4.  Click **Submit** to save the rule.

    The following are some sample rules:

    -   **ToRule**: Filter emails that have been sent directly or forwarded to `security@example.com` email id. ![Define ToRule](../image/urp-torule-example.png)
    -   **User ID Rule**: Filter emails that have been sent from a specific email id. ![Define User ID Rule](../image/urp-phishbox-example.png)

## Define User Reported Phishing properties

Define the header information that must be captured from user reported phishing emails.

### Before you begin

Role required: sn\_si.admin

### About this task

Use these options to configure the following user reported phishing settings.

-   Configuration to extract email headers from the email body. \(**Report Phish** submissions.\)
-   Filter to select headers.
-   Enable or disable parent-child association.

### Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Email Processing** &gt; **User Reported Phishing Properties**.

    ![User Reported Phishing Properties](../image/urp-phishing-email-properties.png)

2.  Specify the configuration for extracting email headers from the email body:

    -   Enter a string that identifies the beginning of the email header.
    -   Enter a string that identifies the end of the email header.

        **Note:** Apply these settings only to headers captured as part of the email body of the phishing email. For instance, if the **PhishAlarm** plugin \(previously known as Wombat\) has configured with the Microsoft Outlook client, when the user clicks the **Report Phish** button, the email headers are captured as per the configuration defined here. The header information is not captured if the phishing email is forwarded as an attachment.

3.  Specify filters to eliminate headers that are not required for investigating the security incident.

    Enter a comma-separated list of email headers that must be captured from the user reported phishing email. If you don't specify any value here, all the header information is captured.

4.  Enable or disable parent-child association.

    By default, the **Yes** option is enabled. Select **Yes** to indicate that child security incidents must be created when user reported phishing emails are aggregated. If you select **No**, child security incidents are not created, but the user reported phishing emails are associated with the security incident and the security incident record is updated. See [Transform user-reported phishing emails to security incidents](urp-about.md#) for more information on how the child security incidents are created.

5.  Enable or disable the option to display the phishing email content in HTML format.

    By default, the **Yes** option is enabled. Select **Yes** to display the phishing email content in HTML format. If you select **No**, the email content in HTML format will not be visible within a phishing record.


## Phishing email records created from user reported phishing emails

User reported phishing emails are converted to security incidents based on the email matching rules that have been defined.

When a new phishing email is reported, the following actions take place:

-   An email record is created in the `sys_email` table.
-   The **Create Phishing Email** inbound action runs on the email record and uses the Email Matching Rules \(see [Set up ingestion rules for User Reported Phishing](urp-about.md#)\) to determine if it is a phishing email.

    **Note:** The email is first verified with all the email matching rules where the **Rule Type** is set to **Deny**. If the email matches to the condition for any of the deny rule, an audit record is created in the `sn_si_phishing_email_deny_audit` table. A security incident isn’t created for such email.

-   When the email is identified as a phishing email, and it matches to an email matching rule where the **Rule Type** is set to **Allow**, a phishing email record is created in the `sn_si_phishing_email` table.
-   Finally, the [Transform user-reported phishing emails to security incidents](urp-about.md#) flow is applied to convert the phishing email record to a security incident.

To view the email details, navigate to **Security Incident** &gt; **Show All Phishing Emails**. A list of phishing email records are displayed. Select the date link in the Created column to view the email record.

![Phishing email with To Rule](../image/urp-torule-email-record.png)

<table id="table_k3m_qxf_djb"><thead><tr><th>

Field Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The number assigned to the user-reported phishing email.

</td></tr><tr><td>

Subject

</td><td>

The subject of the email. The subject rule is useful in simulated phishing campaigns or tests. In this case, organizations send deceptive emails to their own staff to test their response to phishing and similar email attacks. In simulated phishing email tests, if the Microsoft Outlook email client with the **PhishAlarm** plugin \(previously known as Wombat\) is being used, the user can select the **Report Phish** button to report the phishing email. The email is sent to the Security Operations team with **Simulated Phishing** appended to the Subject of the email. This is used to identify the email as a simulated phishing email.

</td></tr><tr><td>

From

</td><td>

The email address from where this phishing email originated. This information is available if the phishing email is forwarded as an .EML file attachment or if the original headers are embedded in the email. If the user forwarded the phishing email directly, the From address may not be available.

</td></tr><tr><td>

Reported by

</td><td>

The email id of the user who reported this phishing email. Select the **Information** icon to view additional details.

</td></tr><tr><td>

Message id

</td><td>

The id assigned to the message.

</td></tr><tr><td>

Matched URP rule

</td><td>

The User Reported Phishing rule that is to be applied on this email. Select the Information icon to view additional details.

</td></tr><tr><td colspan="2">

![URP ingestion rule](../image/urp-emailmatch-torule.png) As you can see, in this example, the **Condition** field shows that the ToRule is applied on this email and a security incident is created. See [Set up ingestion rules for User Reported Phishing](urp-about.md#) for more information on defining email matching rules.

</td></tr><tr><td>

State

</td><td>

When a new phishing email record is created in the `sn_si_phishing_email` table, the State field is set to **New**. When this email record is converted to a security incident \(see [Transform user-reported phishing emails to security incidents](urp-about.md#)\), the State field is updated to **Processed**.

</td></tr><tr><td>

Header origin

</td><td>

This field indicates how the email headers originated or how the user reported the phishing email:-   **Email Header**: The user forwarded the phishing email to the security operations team.
-   **Email Text Body:**
    -   The user selected the **Report Phish** option \(if the **PhishAlarm** plugin \(previously known as Wombat\) has been configured with the email client\).
    -   Based on the User Reported Phishing rule defined, the phishing email is forwarded to the security operations team.
-   **EML Attachment Header**:
    -   Attachment: The user forwarded the email as an attachment \(.EML file\).
    -   Service catalog submission: The user downloaded the email as a .EML file to the desktop and then uploaded it to a specified location. The security incident is then created from the email.
-   **EML Attachment Body**:
    -   The user selected the **Report Phish** option \(if the **PhishAlarm** plugin \(previously known as Wombat\) has been configured with the email client\).
    -   Based on the User Reported Phishing rule defined, the phishing email is forwarded as an attachment to the security operations team.

</td></tr><tr><td>

Security Incident

</td><td>

This field is blank when the user-reported-phishing email is first reported. When the [Transform user-reported phishing emails to security incidents](urp-about.md#) flow has been executed, this email is converted to a security incident record and the number of this record is displayed here.**Note:** Security incident is only created for the emails, which matches to an email matching rule where the **Rule Type** is set to **Allow**.

</td></tr><tr><td>

Raw headers

</td><td>

This field shows the complete header information extracted from the email as defined in the [Define User Reported Phishing properties](urp-about.md#) page. The headers are parsed into key value pairs and displayed in the Phishing Email Headers list.

</td></tr><tr><td colspan="2">

![Phishing email headers](../image/urp-phishing-email-headers.png)

</td></tr><tr><td>

Body

</td><td>

Body of the user-reported phishing email.

</td></tr></tbody>
</table>## Transform user-reported phishing emails to security incidents

The **Transform Phishing Email to Security Incident** flow converts or transforms phishing email records to security incidents.

### Before you begin

**Note:** To enable the User Reported Phishing functionality, you must make a copy of the flow and [activate](../task/getting-started-phishing-playbook.md) it. If you have created custom inbound actions and custom flows to handle user reported phishing submissions, the flow modifications suggested here aren’t required.

-   Role required: sn\_si.admin
-   Flow Designer spoke must be installed.

### About this task

This flow is automatically launched when a user reported phishing email record with the State set to **New** is created. This flow contains the logic to:

-   Aggregate security incidents.
-   Update security incidents with relevant notes.
-   Add header data.
-   Create child incidents as required.

### Procedure

-   Navigate to **Flow Designer** &gt; **Designer** to view the flows available with the Security Operations spoke.

    ![Security Operations Flows](../image/cj-sir-flow-phishing.png)

-   Select the **Transform Phishing Email to Security Incidents** link to view the flow.

-   This flow is provided with the base system and is in **Read Only** mode and can’t be used.

    Select the more icon ![More icon](../image/cj-sir-flow-more-icon.png), make a copy of the flow and open it for your use. You can now change your flow, such as modifying trigger conditions or actions, or adding and removing actions. After making the necessary changes, you must activate \(See [Activate a Security Incident Response flow](../task/getting-started-phishing-playbook.md)\) the flow so that it can be executed.![Transform Phishing Email to Security Incidents flow](../image/urp-transform-flow.png)

    This figure shows the trigger and the steps executed with the flow. The-right hand panel shows the data flow. Select on an icon to expand the step and view the details.

-   Select the **Trigger** icon.

    In the first step, you define or set the trigger for the flow. Specify the conditions for the trigger and task to be performed when the conditions are met. This flow is initiated when a **New** record is uploaded to the `sn_si_phishing_email` table.![Transform flow: trigger](../image/urp-transform-flow-trigger.png)

-   In step 1, the flow verifies if the **Create child incidents for aggregated email submissions?** flag is enabled or disabled on the [Transform user-reported phishing emails to security incidents](urp-about.md#) page.

    ![Transform flow: Action 1](../image/urp-transform-flow-action1.png)

-   In step 2, the oldest parent security incident is identified.

    Notice the icon in step 2. This indicates that the Phishing Email Aggregation Subflow will be executed as part of this step.![Transform flow: Action 2](../image/urp-transform-flow-action2.png)

    Select the action designer icon to see a detailed view of the action. This subflow checks the phishing email and matches it with an existing security incident based on the specified criteria.

    ![Transform flow: Phishing Email Aggregation subflow](../image/urp-transform-flow-action2-subflow.png)

    These two actions are performed when this subflow is executed. Select on the link of the first action to view additional details.

    ![Transform flow: Subflow: Action](../image/urp-transform-flow-action2-subflow-action.png)

    This action checks the emails that match the criteria for the new incoming email based on conditions such as:

    -   Security Incident State isn’t **Closed**.
    -   Subject or From value match the email matching rule conditions defined \(See [Set up ingestion rules for User Reported Phishing](urp-about.md#)\).
    If these conditions are met, you can see the number of records that match the criteria in the Max Results field. The oldest or the first record in the list is designated as the parent record against which the security incidents are aggregated.

-   Step 3 is applicable only if the **Create child incidents for aggregated email submissions?** flag was set to **No** in the [Transform user-reported phishing emails to security incidents](urp-about.md#) page.

    In this case, the phishing email is associated with the security incident record and the flow ends.

    ![Transform flow: Action 3](../image/urp-transform-flow-action3.png)

-   If the **Create child incidents for aggregated email submissions?** is set to **Yes**, the flow continues to run and a new security incident is created based on the user-reported phishing email.

    ![Transform flow: Action 4](../image/urp-transform-flow-action4.png)

-   In step 5, users who received the phishing email \(employees in the To and CC list of the phishing email\) are added to the Affected Users related list in the security incident record.

    ![Transform form: Action 4](../image/urp-transform-flow-action5.png)

-   In step 6, allow listed observables are filtered from the list of observables in the security incident.

    These allow listed observables won’t be added to the security incident.

    ![Transform flow: Filter allow listed observables](../image/urp-transform-flow-action6.png)

-   In step 7, unknown observables from the user-reported phishing email are identified and added to the Observables related list.

    ![Transform flow: Add observables](../image/urp-transform-flow-action7.png)

-   In step 8, an email search query is generated which is a combination of the Subject and the From address of the email.

    This information is useful in identifying the employees in the organization who have been phished.

    ![Transform flow: Create email search query](../image/urp-transform-flow-action8.png)

-   In step 9, the user reported phishing email is associated with the security incident and the security incident record \(created in step 4\) is updated.

    ![Transform flow: Update security incident record](../image/urp-transform-flow-action9.png)

-   In step 10, the parent security incident is identified and a check is made to see if it’s an open security incident record.

    ![Transform flow: Look up security incident record](../image/urp-transform-flow-action10.png)

-   If the parent security is active, notes are added to the child and the parent security incident records indicating how they’re associated with each other.

-   In step 12, if no Affected Users were found \(in step 5 of the flow\), a worknote is added and the security incident record is updated.

    ![Transform flow: Add worknote for unmatched users](../image/urp-transform-flow-action12.png)

-   In step 13, a worknote is added with the list of allow listed observables.

    ![Transform flow: Add list of allow listed observables](../image/urp-transform-flow-action13.png)


### What to do next

You can select **Test** to simulate the actions in the flow before it is published. After testing the flow, select **Activate** to activate the flow so that it can be executed.

Select **Executions** to view the execution details of the flow.

![Transform flow: Execution details](../image/urp-transform-flow-execute.png)

When the flow has been executed, the phishing email record is converted to a security incident. See [Security incident records created from phishing email records](urp-about.md#).

## Security incident records created from phishing email records

Phishing email records stored in the `sn_si_phishing_email` table are converted to security incidents records.

To view the security incident associated with the phishing email record, click **Security incident** &gt; **Phishing Email** &gt; **Show All Phishing emails**.

![Phishing email table](../image/urp-phish-email-table.png)

Click the link in the Security Incident column associated with the phishing email record. The security incident details are displayed.

![Security incident associated with the phishing email record](../image/urp-phish-email-sec-rec.png)

### Related lists

Scroll down to the Related Links section of the security incident and click **Show All related list**. View details like child security incidents, affected users, associated phishing emails.

**Child security incidents**

Click the **Child Security Incidents** tab. You can see a list of child security incidents associated with the parent security incident based on the aggregation logic that has been applied. For every child record added, an automated system activity is added \(in the Worknote section\) to the parent record. This notifies the security analyst about the aggregated child record.

**Note:** You can see the child security incidents here only if the **Create child incidents for aggregated emails submissions** flag is set to **Yes** in the User Reported Phishing Properties page. See [Define User Reported Phishing properties](urp-about.md#) for the details.

![Child security incidents](../image/urp-sec-rec-child.png)

**Associated phishing emails**

Click the **Associated Phish Emails** tab. You see a list of phishing email records \(duplicate records\) associated with the parent phishing email record.

![Associcated phishing email records](../image/urp-sec-rec-ass-phish-emails.png)

**Associated phishing email headers**

Click the **Associated Phish Emails** tab. You see the phishing email header details that have been captured as part of the security incident. You can view the rolled-up headers of all child records and phishing email records aggregated to the parent security incident.

![Associated phishing email headers](../image/urp-sec-rec-assphish-email-head.png)

### Allowed list observables

As the [Transform user-reported phishing emails to security incidents](urp-about.md#) flow is being executed, you can monitor the status of the security incident. When certain observables are marked as allowed list observables, they aren’t added to the Observables Related list. By marking the observables to the allow list, you can ensure that only the important details are displayed. For example, if www.google.com is one of the URLs that has been tagged as the allowed list, the following system message is displayed. Allowed list observables ensure that only the important observables are monitored.

### Capturing unmatched users

Some email ids in the To and CC list of the phishing email may not belong to users in the organization. These email ids are categorized as unmatched users and aren’t included in the Affected Users related list. A worknote indicating that these are unmatched users is displayed.

![Unmatched users](../image/urp-sec-rec-unmatch1.png)

### User Reported Phishing in the Security Analyst Workspace

You can view security incidents associated with the phishing email records in the Security Analyst Workspace.

Navigate to **Security Incident** &gt; **New UI**. The workspace opens in a separate browser tab. Select on the security incident associated with the phishing email record to view the security incident.

![URP security incident: New UI](../image/urp-sec-new-ui.png)

Select the binoculars icon. The original phishing email is displayed.

![URP security incident: New UI - phishing email](../image/urp-sec-new-ui-phish-email.png)

In the **Explore** tab, select **Incidents** &gt; **Child Security Incidents**.

![URP security incident: New UI - child security incidents](../image/urp-sec-new-ui-phish-child.png)

Select **Incidents** &gt; **Associated Phish Headers** &gt; ****. You can view the rolled up headers of all child records and phishing email records aggregated to the parent security incident.

![URP: New UI - Email headers](../image/urp-sec-rec-phish-assoc-header.png)

Select on the phishing email link to view the phishing email record associated with the security incident.

![URP: New UI: phishing email record](../image/urp-sec-rec-phish-from-email.png)

Select the **Incident Timeline** tab.

![URP: New UI: worknotes](../image/urp-sec-newui-worknotes.png)

You can view the system updates that highlight:

-   Identified duplicate child records.
-   Allowed list observables.
-   Unmatched users who received the phishing email but do not belong to the Affected Users list.

## Frequently Asked Questions

This section covers some of the frequently asked questions about the enhanced User Reported Phishing feature.

1.  I have installed the new Security Incident Response spoke but I cannot view any user reported phishing incidents.

    By default, the User Reported Phishing functionality has been disabled.

    To enable this feature, you must make a copy of the read-only [Transform user-reported phishing emails to security incidents](urp-about.md#) flow and activate it before use.

2.  While ingesting phishing emails and converting them into security incidents, what precautionary measures are used to handle malicious links and attachments in the phishing emails?

    The ServiceNow anti-virus scanner scans such malicious attachments and links. However, to ensure that security analysts can investigate the incidents accurately, the Security Incident Response application captures all the artefacts that are part of a phishing email. But the User Reported Phishing functionality mutes the malicious links in the phishing email so that security analysts don't accidentally click these links. Regarding malicious attachments, security analysts must be cautious about downloading them.

3.  Do we capture all malicious files that are part of the phishing emails for security incident enrichment?

    Yes, we capture all files from the phishing emails. You can view these details are available as part of security incident observables in the form of a file hash.

4.  Do we send malicious files and links from phishing emails to a sandbox instance for investigation?

    Currently, we do not support out-of-the-box sandbox integrations for investigating malicious files and links.

5.  Is there a time window or a trigger that defines the duration in which incoming duplicate phishing email records are associated with a parent security incident?

    Duplicate phishing email records are aggregated only to an active parent security incident. If the parent incident is closed or canceled, then the incoming new duplicate phishing email will be created as a new security incident. However, in this scenario, within the new security incident, you can view the closed or canceled parent security incident in the **Similar Security Incident** related list.

    **Note:** This behavior can be configured using the flow designer.

6.  Does the User Report Phishing feature support the use of only the Microsoft Outlook **PhishAlarm** plugin \(previously known as Wombat\) to capture email header details?

    The User Reported functionality has been built to parse email headers and complies with RFC822 standards. So, similar to the **PhishAlarm** plugin \(previously known as Wombat\), all other Microsoft Outlook plugins that capture email headers based on RFC822 standards are supported.


