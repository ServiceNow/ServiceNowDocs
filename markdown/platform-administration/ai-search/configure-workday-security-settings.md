---
title: Configure Workday security settings
description: Create an unconstrained integration system security group in Workday. The Workday external content connector uses this security group when accessing your Workday content.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-14"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Workday external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure Workday security settings

Create an unconstrained integration system security group in Workday. The Workday external content connector uses this security group when accessing your Workday content.

## Before you begin

You need administrator privileges in your organization's Workday tenant.

Role required: none

## About this task

The Workday external content connector runs as an integration in Workday. To enable the connector to access your Workday content, you need to create an integration system user and an unconstrained integration system security group in your Workday tenant.

## Procedure

1.  Create an integration system user account in Workday.

    1.  Log in to your Workday tenant with your administrator credentials.

    2.  In the Workday search bar, search for the **Create Integration System User** task and select it.

    3.  On the Create Integration System User page, enter `ISU SNOW ACL` as the name for your new integration system user.

    4.  Enter a password for your new user or generate one by selecting **Generate Random Password**.

    5.  Clear the **Require New Password at Next Sign In** option.

    6.  Select **OK**.

    Workday creates your new integration system user account.

2.  Create an unconstrained integration system security group in Workday.

    1.  In the Workday search bar, search for the **Create Security Group** task and select it.

    2.  On the Create Security Group page, select **Integration System Security Group \(Unconstrained\)** as the type for your new group.

    3.  Enter `ISSG Service Now ACL` as the name for your new integration system security group.

    4.  Select **OK**.

        Workday creates your new unconstrained integration system security group.

    5.  In the Integration System Users field, enter `ISU SNOW ACL` and press Enter.

        Workday adds your new integration system user account to your new unconstrained integration system security group.

3.  Assign domain security policy permissions to your new integration system security group.

    1.  In the Workday search bar, search for the **View Security Groups for User** task and select it.

    2.  In the Person field, enter `ISU SNOW ACL`, then select **OK**.

    3.  On the View Security Groups for User page, select the entry for your `ISSG Service Now ACL` integration system security group.

    4.  On the View Integration System Security Group \(Unconstrained\) page, navigate to **…** &gt; **Security Group** &gt; **Maintain Domain Permissions for Security Group**

    5.  On the Maintain Domain Permissions for Security Group page, enter each of the following domain security policy names into the **Domain Security Policies permitting View access** field, pressing Enter after each name:

        -   HCM All Organizations
        -   Indexed Data Source: Positions
        -   Manage: Company
        -   Manage: Cost Center
        -   Manage: Custom Organization
        -   Manage: Help Articles
        -   Manage: Region
        -   Manage: Supervisory Organization
        -   Person Data: Learning
        -   Person Data: Work Email
        -   Reports: Learning Record
        -   Reports: Organization
        -   Security Administration

            **Note:** This domain security policy permission is inherited by the following domain security policies:

            -   Lock Out Workday Accounts
            -   Manage: Authorized Applications
            -   Process: User-Based Security Group Event
            -   Set Up: Security Rules
        -   Security Configuration
        -   Set Up: Compensation Guidelines
        -   Set Up: Organization
        -   Set Up: Payroll - Pay Group Specific
        -   Workday Accounts
        -   Workday Query Language
        -   Worker Data: Active and Terminated Workers
        -   Worker Data: Current Job Profile Information
        -   Worker Data: Current Management Level Information
        -   Worker Data: Current Staffing Information
        -   Worker Data: Headcount Reports
        -   Worker Data: Historical Staffing Information
        -   Worker Data: Payroll \(Payroll Input\)
        -   Worker Data: Public Worker Reports
        -   Worker Data: Time Off \(Time Off Balances Manager View\)
        -   Worker Data: Time Off \(Time Off Balances\)
        -   Worker Data: Time Off \(Time Off Manager View\)
        -   Worker Data: Time Off \(Time Off\)
        -   Worker Data: Work Shifts
        -   WQL for Workday Extend
4.  Activate the security policy changes for your new integration system security group.

    1.  In the Workday search bar, search for the Activate Pending Security Policy Changes task and select it.

    2.  On the Activate Pending Security Policy Changes page, enter a comment, then select **OK**.

        Workday displays the list of changes pending for your new integration system security group.

    3.  Select **Confirm**, then select **OK**.

        The pending changes are applied to your new integration system security group.


**Parent Topic:**[Workday external content connector](../concept/workday-external-content-connector.md)

