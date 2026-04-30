---
title: Security posture dashboards
description: Use the customizable single and multi-instance security posture dashboards to monitor your security KPIs. These dashboards consolidate the important information regarding the security of your instances in a single location and include a number of base system dashboard widgets.
locale: en-US
release: yokohama
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Security posture console, Security Center, Platform Security]
---

# Security posture dashboards

Use the customizable single and multi-instance security posture dashboards to monitor your security KPIs. These dashboards consolidate the important information regarding the security of your instances in a single location and include a number of base system dashboard widgets.

## Accessing the Security posture dashboards

To access the Security posture dashboard, open Security Center by navigating to **All** &gt; **Security Center**. Select **Security posture** in the **Tools** section at the bottom of the page, then select **Security posture dashboards**.

## Dashboard components

The dashboard is divided into multiple sections containing widgets related to an aspect of instance security. Select any widget on the dashboard to view more detail on this aspect of your instance's security.

<table id="table_tqv_p3p_xbc"><tbody><tr><td>

The **At a glance** section displays an overview of security on an instance, such as a compliance score, Customer Actions due, and update and release information for the instance.

</td><td>

![At a glance](../images/spd-at-a-glance.png)

</td></tr><tr><td>

The **Users** section provides information on the users in your instance. The widgets on this section show user information, and a line graph showing changes to this information over time. Select a widget to view more detail

</td><td>

![Users](../images/spd-users.png)

</td></tr><tr><td>

The **Login protection** section includes information on failed logins, including failed login attempts for privileged users.

</td><td>

![Login protection](../images/spd-login-protection.png)

</td></tr><tr><td>

The **Instance hardening** section contains recommended hardening security settings that you can change to improve instance security. Use this section to see the priority and potential impact of these changes.

</td><td>

![Instance hardening](../images/spd-instance-hardening.png)

</td></tr><tr><td>

The **Instance trends** dashboard displays the results of the access controls auditor scan suite.

</td><td>

![Instance trends](../images/spd-instance-trends.png)

</td></tr><tr><td>

Use the **Data protection** section to see an overview of classified data, such as personally identifiable information \(PII\). The dashboard also tracks exports of classified data,

</td><td>

![Data protection](../images/spd-data-protection.png)

</td></tr></tbody>
</table>## Review multiple instances

![Multi-instance view of the security posture dashboard](../images/spd-multiple.png)

View the security posture of your non-production instances without leaving your production instance using the **All instances** tab at the top of the dashboard. The **All instances** tab displays a condensed version of the same information as the **This instance** tab, but also includes data from all your non-production instances.

By default, the **All instances** tab displays information on the production instance you are logged into, and all non-production instances across all your production environments.

You may add or remove instances that appear on this dashboard by modifying your trust configuration. Providing data visibility between instances allows them to appear within your dashboard. For details on this process, see [Basic trust configuration for data sync applications](https://www.servicenow.com/docs/access?context=grant-access-other-instances&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Dashboard customization

The instance security posture dashboard can’t be customized, but you can duplicate the dashboard by selecting the **More Actions** \(![More actions](../../../reuse/icons/product-icons/ellipsis-vertical-fill-24.svg)\) icon and selecting **Duplicate**. You can change the duplicate dashboard.

**Parent Topic:**[Security posture console](sc-posture-console.md)

