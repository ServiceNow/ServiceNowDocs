---
title: Security posture dashboards
description: Use the customizable single and multi-instance security posture dashboards to monitor your security KPIs. These dashboards consolidate the important information regarding the security of your instances in a single location and include a number of base system dashboard widgets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/security-center/scc-sec-posture-dashboard.html
release: australia
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Security posture console, Security Center, Platform Security]
---

# Security posture dashboards

Use the customizable single and multi-instance security posture dashboards to monitor your security KPIs. These dashboards consolidate the important information regarding the security of your instances in a single location and include a number of base system dashboard widgets.

## Accessing the Security posture dashboards

To access the Security posture dashboard, open Security Center by navigating to **All** &gt; **Security Center**. Select **Security posture console** in the **Security consoles** section. On the **Security posture console** page, select **Security posture dashboards** at the top.

Use the down arrow next to **Security posture dashboard** to switch between instance dashboards.

\[Omitted image "spd-title-dropdown.png"\] Alt text: Change dashboard drop-down

The dashboard is divided into multiple sections containing widgets related to an aspect of instance security. Select any widget on the dashboard to view more detail on this aspect of your instance's security.

## At a glance

\[Omitted image "spd-at-a-glance.png"\] Alt text: At a glance

The **At a glance** section displays an overview of security on an instance, such as a compliance score, Customer Actions due, and release information for the instance.

-   **Compliance score**

    Displays your instance compliance score percentage over time, beginning with the date sown at the bottom of the widget. Select this widget to navigate to the [Hardening compliance score trend](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/score-trend.md).

-   **Metric threshold alerts for me**

    Displays a count of Metric threshold event \[n\_vsc\_metric\_threshold\_event\] records assigned to the current user. Select this widget to navigate to a list of these records.

-   **Metric threshold alerts for everyone.**

    Displays a count of unassigned Metric threshold event \[n\_vsc\_metric\_threshold\_event\] records. Select this widget to navigate to a list of these records.

-   **Customer actions due soon**

    Displays a count of customer actions due soon. Select this widget to navigate to [Customer Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/critical-updates.md).

-   **Antivirus downloaded files**

    Displays a count of files uploaded to your instance that have been quarantined. Select this widget to view these quarantined files in the [Antivirus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/antivirus.md) section of [Security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-metrics.md).

-   **Release version**

    Displays the family version of the instance and the date of the last instance update.


## Users

\[Omitted image "spd-users.png"\] Alt text: Users

The **Users** section provides information on the users in your instance. The widgets on this section show user information, and a line graph showing changes to this information over time. Select a widget to view more detail.

-   **Total users**

    Displays a count of users on your Users \[sys\_user\] table. Select this widget to see details on these records in the [Active Sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-active-sessions.md) section of [Security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-metrics.md).

-   **Active users**

    Displays a count of active users on your Users \[sys\_user\] table. Active users are user records where the **Active** field is selected. Select this widget to see details on these records in the [Active Sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-active-sessions.md) section of [Security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-metrics.md).

-   **Active integration accounts**

    Displays a count of integration accounts on your Users \[sys\_user\] table. Integration accounts are user records where the **Web service access only** field is selected. Select this widget to see details on these records in the [Active Sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-active-sessions.md) section of [Security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-metrics.md).

-   **Active privileged accounts**

    Displays a count of active privileged users on your Users \[sys\_user\] table. Privileged users are user records where the **Active** field is true, the **Internal Integration User** is false, and **Internal Integration User** is inactive. Select this widget to see details on these records in the [Active Sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-active-sessions.md) section of [Security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-metrics.md).

-   **Never logged-in users**

    Displays a count of users on your Users \[sys\_user\] table created in the last 60 days, and have no value in the **Last login time** field. Select this widget to see details on these records in the [Active Sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-active-sessions.md) section of [Security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-metrics.md).


## Login protection

\[Omitted image "spd-login-protection.png"\] Alt text: Login protection

The **Login protection** section includes information on failed logins, including failed login attempts for privileged users. These widgets include a line graph showing changes to this information over time. Select a widget to view more detail.

-   **Failed user logins**

    Displays a count of failed user login attempts. Select this widget to navigate to see details on failed logins in [Security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-metrics.md).

-   **Failed privileged user logins**

    Displays a count of failed user login attempts from privileged accounts. Privileged users are user records where the **Active** field is true, the **Internal Integration User** is false, and **Internal Integration User** is inactive. Select this widget to navigate to see details on failed logins in [Security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-metrics.md).

-   **Privileged logins without MFA**

    Displays a count of privileged accounts that aren’t configured for multi-factor authentication \(MFA\). Select this widget to navigate to see a list these accounts in [Security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-metrics.md).

-   **REST APIs without API access policy**

    Displays a list of REST APIs that aren’t restricted with an API access policy. Select this widget to navigate to see a list these REST APIs in [Security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-metrics.md).


## Instance hardening

\[Omitted image "spd-instance-hardening.png"\] Alt text: Instance hardening

The **Instance hardening** section contains recommended hardening security settings that you can change to improve instance security. Use this section to see the priority and potential impact of these changes.

## Instance trends

\[Omitted image "spd-instance-trends.png"\] Alt text: Instance trends

The **Instance trends** dashboard displays the results of the access controls auditor scan suite.

## Data protection

\[Omitted image "spd-data-protection.png"\] Alt text: Data protection

Use the **Data protection** section to see an overview of classified data, such as personally identifiable information \(PII\). The dashboard also tracks exports of classified data.

-   **Classified data**

    Displays a pie chart of classified data on your instance, separated by type. Select a section of the chart to view details on these records. For details on data classification, see [Data classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/data-privacy-classic/dps-data-classification.md).

-   **Classified data exports**

    Displays a count of classified records that have been exported from your instance. Select this widget to see a list of classified exports in the [Export](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/export.md) section of [Security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-metrics.md).

-   **Total table columns**

    Displays a count of all columns\(fields\) in tables on your instance. Select this widget to review these columns in the [Data Classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/data-classification-security-metrics.md) section of [Security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-metrics.md).

-   **Encrypted PII classified columns**

    Displays a count of encrypted records classified as Personally Identifiable Information \(PII\). Select this widget to review these records in the [Data Classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/data-classification-security-metrics.md) section of [Security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-metrics.md).

-   **Total PII classified columns**

    Displays a count of all records classified as Personally Identifiable Information \(PII\). Select this widget to review these records in the [Data Classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/data-classification-security-metrics.md) section of [Security metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-metrics.md).


## Review multiple instances

\[Omitted image "spd-multiple.png"\] Alt text: Multi-instance view of the security posture dashboard

View the security posture of your non-production instances without leaving your production instance using the **All instances** tab at the top of the dashboard. The **All instances** tab displays a condensed version of the same information as the **This instance** tab, but also includes data from all your non-production instances.

By default, the **All instances** tab displays information on the production instance you’re logged in to, and all non-production instances across all your production environments.

You may add or remove instances that appear on this dashboard by modifying your trust configuration. Providing data visibility between instances allows them to appear within your dashboard. For details on this process, see [Basic trust configuration for data sync applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/grant-access-other-instances.md).

## Dashboard customization

The instance security posture dashboard can’t be customized, but you can duplicate the dashboard by selecting the **More Actions** \(\[Omitted image "ellipsis-vertical-fill-24.svg"\] Alt text: More actions\) icon and selecting **Duplicate**. You can change the duplicate dashboard.

**Parent Topic:**[Security posture console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sc-posture-console.md)

