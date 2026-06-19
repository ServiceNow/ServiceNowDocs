---
title: Configure client session access role
description: The Embedded Session Role Configuration \(Client Access Role configuration\) record is created by default, which included removal of admin and security admin roles \(high privilege roles\) for the users using the UI components on the third-party portals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/configure-client-session-access-role.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Web Embeddables, Authentication, Access Management]
---

# Configure client session access role

The **Embedded Session Role Configuration** \(Client Access Role configuration\) record is created by default, which included removal of admin and security admin roles \(high privilege roles\) for the users using the UI components on the third-party portals.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Client Access** &gt; **Client Access Role Configurations**.

2.  Select **Embedded Session Role Configuration**.

    \[Omitted image "embedded-session-role.png"\] Alt text: Embedded Session

    **Note:** The **Embedded Session Role Configuration** record is created by default to remove admin and security admin roles \(high privilege roles\) for the users for the embedded session.

    The details for the configuration is displayed. By default, the configuration ensures that high privilege roles such as **admin** and **security\_admin** are removed in the Embedded Session.

    \[Omitted image "embedded-session-role-record.png"\] Alt text: Configuration record

    You can add more users to the list based on your requirement.

3.  Use the information icon to open the policy.

    The policy \(Remove high privilege roles Policy\) has the following details:

    -   **Policy Inputs**: Embedded Session- the user-specific filter criteria that is used to remove the configured roles.\[Omitted image "embedded-session-role-record-input.png"\] Alt text: Policy input record
    -   **Policy Conditions**: Remove high privilege roles in Embedded Session- the condition validates to true to remove the high privilege roles that are added for the configuration.\[Omitted image "embedded-session-role-record-role-true.png"\] Alt text: Condition set to true
    When the user is accessing the ServiceNow components in the third-party portal, based the above configurations, high- privilege roles are removed for that embedded session.

    You can also add more roles that needs to be removed to this **Embedded Session Role Configuration** record.


