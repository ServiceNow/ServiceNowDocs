---
title: Security posture dashboards
description: Use the customizable single and multi-instance security posture dashboards to monitor your security KPIs. These dashboards consolidate the important information regarding the security of your instances in a single location and include a number of base system dashboard widgets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-security/security-center/scc-sec-posture-dashboard.html
release: xanadu
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Security posture console, Security Center, Platform Security]
---

# Security posture dashboards

Use the customizable single and multi-instance security posture dashboards to monitor your security KPIs. These dashboards consolidate the important information regarding the security of your instances in a single location and include a number of base system dashboard widgets.

## Accessing the Security posture dashboards

Access the Security posture dashboard by navigating to **All** &gt; **Security Center**. The Security posture dashboard content is located in the **Overview** tab.

## Dashboard components

The dashboard is divided into multiple sections containing widgets related to an aspect of instance security. Select any widget on the dashboard to view more detail on this aspect of your instance's security.

<table id="table_tqv_p3p_xbc"><tbody><tr><td>

The **At a glance** section displays an overview of security on an instance, such as a compliance score, customer actions due, and update and release information for the instance.

</td><td>

\[Omitted image "spd-at-a-glance.png"\] Alt text: At a glance

</td></tr><tr><td>

The **Users** section provides information on the users in your instance. The widgets on this section show user information, and a line graph showing changes to this information over time. Select a widget to view more detail

</td><td>

\[Omitted image "spd-users.png"\] Alt text: Users

</td></tr><tr><td>

The **Login protection** section includes information on failed logins, including failed login attempts for privileged users.

</td><td>

\[Omitted image "spd-login-protection.png"\] Alt text: Login protection

</td></tr><tr><td>

The **Instance hardening** section contains recommended hardening security settings that you can change to improve instance security. Use this section to see the priority and potential impact of these changes.

</td><td>

\[Omitted image "spd-instance-hardening.png"\] Alt text: Instance hardening

</td></tr><tr><td>

The **Instance trends** dashboard displays the results of the access controls auditor scan suite.

</td><td>

\[Omitted image "spd-instance-trends.png"\] Alt text: Instance trends

</td></tr><tr><td>

Use the **Data protection** section to see an overview of classified data, such as personally identifiable information \(PII\). The dashboard also tracks exports of classified data,

</td><td>

\[Omitted image "spd-data-protection.png"\] Alt text: Data protection

</td></tr></tbody>
</table>## Review multiple instances

\[Omitted image "spd-multiple.png"\] Alt text: Multi-instance view of the security posture dashboard

View the security posture of your non-production instances without leaving your production instance using the **All instances** tab at the top of the dashboard. The **All instances** tab displays a condensed version of the same information as the **This instance** tab, but also includes data from all your non-production instances.

By default, the **All instances** tab displays information on the production instance you are logged into, and all non production instances across all your production environments.

You may add or remove instances that appear on this dashboard by modifying your trust configuration. Providing data visibility between instances allows them to appear within your dashboard. For details on this process, see .

## Dashboard customization

The instance security posture dashboard can’t be customized, but you can duplicate the dashboard by selecting the **More Actions** \(\[Omitted image "ellipsis-vertical-fill-24.svg"\] Alt text: More actions\) icon and selecting **Duplicate**. You can change the duplicate dashboard.

**Parent Topic:**[Security posture console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-security/security-center/sc-posture-console.md)

