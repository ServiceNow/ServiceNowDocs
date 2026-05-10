---
title: Configure the Security Analyst Workspace
description: Configure the user interface of the Incident record in the Security Analyst Workspace to specify the fields you want to display.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Install and configure Security Incident Response, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure the Security Analyst Workspace

Configure the user interface of the Incident record in the Security Analyst Workspace to specify the fields you want to display.

## Before you begin

Role required: sn\_si.analyst

## About this task

Specify the fields to be displayed in your Incident record and the order in which the fields must appear on the Security Incident form and the Response Task form. You can also set a limit on the number of fields that you want to display.

**Note:** You can create rules to determine which view should be used for a specific form. Several views are included with the base system, including the Default and SIR New UI views. Several view rules are also shipped with the base system, including the All Others Response Task rule. This rule enforces the Default view on the Response Task form when the condition specified in the view rule is met. The Security Analyst Workspace uses the SIR New UI view. If the form fields displayed in the Security Analyst Workspace don’t match the form fields in the classic environment, a view rule is most likely enforced. To use the **SIR New UI** view for the form, you must disable the view rule. See [Control when the system displays a view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/control-views.md) for the details.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show All Incidents**.

2.  To open the security incident record, select a security incident.

3.  To navigate to the Configuring Security Incident form page, select the ![Context menu](../image/cj-sir-newui-config-menu.png) menu icon and select **Configure** &gt; **Form Layout**.

4.  From the **View name** list, select **New UI - Form Layout Configurations**.

5.  In the **Section** field, select the appropriate section.

    This can be **Security Incident** or **Security Incident Response Task**.![Configure security incident record](../image/cj-sir-newui-config-si.png)

6.  Select the fields and the order in which you want them to appear in the Incident banner in the new UI.

7.  Select **Save**.

    **Note:**

    -   Certain fields are hidden by default in the Incident and Response Task banners. Change the fields that are hidden or displayed by modifying the `sn_app_secops_ui.form.excluded_fields.incident` and `sn_app_secops_ui.form.excluded_fields.response_task` properties as described in [Security Analyst Workspace properties](../reference/sir-workspace-properties.md).
    -   Specify the number of fields that can be displayed in the Incident and Response Task banners and on the first line of the Incident banner by setting these properties:
        -   sn\_app\_secops\_ui.task\_summary.single\_summary.limit.incident
        -   sn\_app\_secops\_ui.task\_summary.single\_summary.limit.response\_task
        -   sn\_app\_secops\_ui.task\_summary.single\_summary.limit.incident.first\_line
8.  To configure the styles of the dotted circles that appear next to a field value in the Incident record, for example, ![Menu style](../image/cj-sir-newui-config-style.png) navigate to **System UI** &gt; **Field Styles** and modify or create a style record for the specific table and field name.

    The property background-color in the Style field of the style record determines the color of the dotted circle.

9.  To view the updated incident banner, navigate to **Security Incidents** &gt; **Incidents \(New UI\)** and refresh the page to view the updated Incident banner.

10. To configure the Response Task banner in the Incident record, navigate to **Security Incidents** &gt; **Response Tasks** &gt; **Show All Tasks** and repeat the steps.

11. If you’re creating a task table extending from the base Security Incident Response Task table, you must also add the SIR New UI view to the table.

    1.  From the **View Name** list, select **New**.

        ![Create new view](../image/cj-sir-newui-config-newresp.png)

    2.  Enter **SIR New UI** \(case sensitive\) in the Create New View window and select **OK**.


## Result

The security incident and response task banners are updated in the Security Analyst Workspace \([Manage security threats using the Security Analyst Workspace](../concept/sir-new-ui.md)\).

