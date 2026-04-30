---
title: Manage configurations in Service Operations Workspace for ITSM
description: From a single page, quickly access and manage the customizations in Service Operations Workspace \(SOW\) for ITSM, access additional plugins that extend the Service Operations Workspace for ITSM capabilities, and access ServiceNow help.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 12
breadcrumb: [Admin Center in Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Manage configurations in Service Operations Workspace for ITSM

From a single page, quickly access and manage the customizations in Service Operations Workspace \(SOW\) for ITSM, access additional plugins that extend the Service Operations Workspace for ITSM capabilities, and access ServiceNow help.

## Before you begin

Role required: sn\_sow\_itsm\_admin.sow\_admin\_user, admin, change\_manager

## About this task

The Admin Center consists of the following tabs:

-   **Overview**: Provides access to all customizations available in Service Operations Workspace for ITSM.
-   **Configurations**: Provides access to page-related customizations available in Service Operations Workspace for ITSM. For example, the landing page, incident record page, and modern change management page.
-   **Learning**: Provides access to learning resources to assist the admins in gaining a deeper understanding of SOW configuration. These resources are designed to provide users with the necessary knowledge and skills to effectively configure and manage ITSM.

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace Admin Center** &gt; **Overview**.

2.  If not already installed, from the **Configure ITSM Core** section, install applications such as Incident Management.

3.  Select any of the following options.

<table id="choicetable_lg2_mrt_cyb"><thead><tr><th align="left" id="d219419e138">

Option

</th><th align="left" id="d219419e141">

Description

</th></tr></thead><tbody><tr><td id="d219419e147">

**Migrate configurations and customizations from ITSM Agent Workspace to SOW for ITSM**

</td><td>

On the **Overview** tab, from the **Initial Setup** section, select the **Migrate from ITSM Agent Workspace to SOW** option. For information about this migration utility, see [Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](../concept/migration-from-itsm-aw-sow.md).

</td></tr><tr><td id="d219419e187">

**Configure the landing page**

</td><td>

1.  On the **Overview** tab, from the **Initial Setup** section, select the **Configure the landing page** option.
2.  To modify the landing page redirection properties, do the following steps.
    1.  Select **Landing Page Configurations** &gt; **Landing page redirection**.
    2.  For the required property, select **Configure**. For information about these properties, see [Redirect non-admin users to Service Operations Workspace](redirect-sow-landing-page.md).
    3.  Edit the property and select **Update**.
3.  To configure landing page sections, do the following steps.
    1.  Select **Landing Page Configurations** &gt; **Landing page**.
    2.  If available, select **Configure** beside the following landing page options to configure them and use the toggle switch beside the options to modify the visibility.

        -   Greeting message that is displayed as a header.
        -   For tier 1 and tier 2 agents, the default list view visibility for donuts. Collapsing the list view reduces the page load time and it can be expanded by selecting any donut card.
        -   For tier 1 and tier 2 agents, customizations for various landing page sections such as Overview \(donut cards\), Announcements, Quick Links, and Upcoming, and also the visibility for a few of these sections.
        -   For tier 1 agents, visibility of the Getting started section that provides an overview of key features in Service Operations Workspace.
For information about landing page customizations, see [Customizing Service Operations Workspace for ITSM to align with your requirements](../concept/customize-sow-landing-page.md).

</td></tr><tr><td id="d219419e302">

**Configure the availability and order of contextual side panel tabs for record pages**

</td><td>

1.  On the **Overview** tab, from the **Initial Setup** section, select the **Configure the contextual side panel** option. The Contextual side panel configurations page is displayed.
2.  To configure the availability of a tab for all applicable pages in SOW for ITSM, do the following steps.
    1.  Select the associated app route for the required tab.
    2.  From the **More Actions** drop-down, select **Activate** or **Deactivate**.
3.  To modify the order of a tab for all applicable pages in SOW for ITSM, edit the **Order** field for the associated app route.

**Note:** Ensure that the user's scope is set to that of the app route.

</td></tr><tr><td id="d219419e354">

**Configure the incident record page**

</td><td>

1.  On the **Configurations** tab, select the **Incident Management** option.
2.  Select **Incident record** and then select **Configure** to configure any of the following tabs:
    -   Overview: Configure any of the following options for the **Overview** tab.
        -   Tab visibility for tier 1 agents: Configure the visibility settings to display the **Overview** tab for the tier-1 agents. You can also configure the user criteria to include or exclude users with other roles and user groups.

**Note:**

            -   By default, the **Overview** tab is displayed for the tier-1 agents.
            -   When you choose to hide the **Overview** tab for the tier-1 agents, the **Details** tab opens by default.
            -   This option is available only if the **glide.ux.user\_criteria\_enabled** property is **true**. For more information, see [Enable the user criteria property](https://www.servicenow.com/docs/access?context=enable-user-criteria-property&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).
        -   Summary: Configure the fields layout, UI elements and the visible data content on the Summary section of the **Overview** tab.
        -   Impact: Configure the fields layout, UI elements and the visible data content on the Impact section of the **Overview** tab.
        -   Cause: Configure the fields layout, UI elements and the visible data content on the Cause section of the **Overview** tab.
        -   Resolution: Configure the fields layout, UI elements and the visible data content on the Resolution section of the **Overview** tab.
    -   Details: Configure any of the following options for the **Details** tab.
        -   Record: Provides further details on the incident record. Configure the fields layout, UI elements, and the visible data content of the **Details** tab using form builder.
        -   New record: This layout appears when an agent creates an incident record. Configure the fields layout, UI elements, and the visible data content of the **Details** tab using form builder.
    -   Response templates: Create and configure response templates for incidents. Response templates are used as reusable messages that you can copy and paste in the required areas such as email or chat for a quick response. To use the response template feature, the users must have the sn\_templated\_snip.template\_snippet\_reader role. The number of the response templates created for the incident table is displayed in this section. For more information on defining and configuring the response templates for incident tables in Service Operations Workspace, see [Response templates](https://www.servicenow.com/docs/access?context=response-templates-templated-snippets&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).
    -   Incident management properties: Configure the incident features using the incident management properties. For more information on configuring incident management properties, see [Incident Management properties](../../incident-management/reference/incident-management-properties.md).
 For more information about configuring the field layout, UI elements and the visible data content using form builder, see [Customize forms within a form component](https://www.servicenow.com/docs/access?context=learn-by-example-edit-form-component&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

 For information about incident record page customizations, see [Customize the incident record page](../concept/customize-the-incident-record-page.md#).

</td></tr><tr><td id="d219419e521">

**Configure the Major Incident Management features**

</td><td>

1.  On the **Configurations** tab, select the **Major Incident Management** option.
2.  Configure any of the following options:
    -   Major incident manager role
    -   Major incident trigger rules
    -   Communication templates
    -   Communication plans
    -   Playbook
    -   Email notifications
    -   Timeline configurations for post incident report.
For more information on the configurations of features in Major Incident Management in Admin Center, see [Configuring Major Incident Management in Service Operations Workspace](../concept/configuring-mim-in-sow.md).

</td></tr><tr><td id="d219419e589">

**Configure the Problem Management features**

</td><td>

1.  On the **Configurations** tab, select the **Problem Management** option.
2.  Configure the following options.
    -   Problem record: choose whether to enable the overview tab, and configure the problem record UI elements and the visible data content. For more information, see [Customize forms within a form component](https://www.servicenow.com/docs/access?context=learn-by-example-edit-form-component&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)
    -   Problem task record: configure the problem task record UI elements and the visible data content. For more information, see [Customize forms within a form component](https://www.servicenow.com/docs/access?context=learn-by-example-edit-form-component&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)


</td></tr><tr><td id="d219419e639">

**Configure the Change Management features**

</td><td>

1.  On the **Configurations** tab, select the **Change Management** option.
2.  Configure the following options.
    -   Modern change adoption: Contains widgets which navigates to the configuration pages for change models, change approval policies, risk and success scores, and automating DevOps changes.
    -   Change models: Create optimized change state models with policy-based automation capabilities that are fit-for-purpose to increase change efficiency and velocity. Create change models, change model condition types, and change flows through this section.
        -   For information on creating a change model, see [Create a Change model](../../change-management/task/create-a-change-model.md).
        -   For information on creating change model condition types, see [Create predefined transition condition types](../../change-management/task/create-predefined-transition-condition-type.md).
        -   For information on configuring flows, see [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).
    -   Change approval policies: Create change approval policies to streamline your approval process. Ensure that changes gain the approvals needed to drive stability and compliance, without compromising on change velocity. Create change approval policies and definitions through this section.
        -   For information on creating change approval policies, see [Create change approval policies](../../change-management/task/create-change-policy.md).
        -   For information on creating approval definitions, see [Create approval definitions](../../change-management/task/create-approval-definitions.md).
    -   Risk and success scores: Use data-driven risk capabilities \(risk conditions, risk calculations, and ML-based risk intelligence\) to take the subjectivity out of risk and have automatic, data-driven determinations. Create risk conditions, change success score ratings, success probability definitions, risk assessments, and calculated risk score through this section.

        -   For information on creating risk conditions, see [Risk conditions and calculation](../../change-management/concept/change-risk-assess-detect-conflict.md).
        -   For information on creating change success score ratings, see [Change success score](../../change-management/concept/change-success-score.md).
        -   For information on creating success probability definitions, see [Success Probability definitions](../../change-management/concept/success-probability-definition.md).
        -   For information on creating risk assessments, see [Risk assessment](../../change-management/concept/c_RskAsmtCalc.md).
        -   For information on calculated risk score, see [Calculated Risk Score](../../change-management/concept/risk-lookup.md).
**Note:** You can also navigate to the Change Success Dashboard to see trends in resolution efficiency for a team, change type, or change model over time based on the parameters used to calculate the overall success score. For more information, see [Exploring ITSM Success Dashboard indicators](../../itsm-success-dashboard/concept/explore-success-dashboard-indicators.md).

    -   Automate DevOps changes: Automate DevOps changes with DevOps Change Velocity. Connect and configure tools from your DevOps toolchain with our DevOps data model to drive enhanced DevOps change traceability. Automatically create changes from CI/CD pipeline executions with relevant DevOps data attached and leverage that data to drive full change approval automation. For more information, see [DevOps Change Velocity](../../enterprise-dev-ops/concept/devops-landing-page-new.md).
    -   Change record: Configure the change record UI elements and the visible data content. For more information, see [Customize forms within a form component](https://www.servicenow.com/docs/access?context=learn-by-example-edit-form-component&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).
    -   Change task record: Configure the change task record UI elements and the visible data content. For more information, see [Customize forms within a form component](https://www.servicenow.com/docs/access?context=learn-by-example-edit-form-component&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).


</td></tr><tr><td id="d219419e830">

**Configure the On-Call Scheduling features**

</td><td>

1.  On the **Configurations** tab, from the **SOW configurations** section, navigate to the **On-call Scheduling** tile and select **Configure**.
2.  Configure any of the following options through a guided experience to improve the productivity of group managers and on-call agents.
    -   On-call user groups and preferences. For information about these preferences, see [Configure preferences for a user group](../../../administer/on-call-scheduling/task/config-group-prefs-oncall.md).
    -   On-call templates
        -   Schedule templates. For information about on-call schedules, see [Configure or update an On-Call schedule](../../../administer/on-call-scheduling/task/create-update-schedule-oncall.md) and [Update a schedule entry](../../../administer/on-call-scheduling/task/schedule-entry-update-oncall.md).
        -   Group templates. For information about group templates, see [Create a group template to simplify configuring schedules](../../../administer/on-call-scheduling/task/create-group-template.md) and [Create a shift template to simplify configuring shifts](../../../administer/on-call-scheduling/task/create-shift-template.md).
        -   Escalation policy templates. For information about escalation policy, see [Create an escalation policy](../../../administer/on-call-scheduling/task/create-custom-esc-policy-oncall.md).
        -   Contact preference templates. For information about contact preferences, see [Configure my availability and contact preferences](../../../administer/on-call-scheduling/task/config-my-contact-prefs-oncall.md).
    -   On-call properties. For information about these properties, see [System properties for On-Call Scheduling](../../../administer/on-call-scheduling/reference/on-call-properties.md).
3.  Update the configuration and mark it complete, or skip the configuration.

**Note:** You can restart a skipped configuration.

</td></tr><tr><td id="d219419e950">

**Configure the Service Reliability Management sections**

</td><td>

1.  On the **Configurations** tab, select the **Service Reliability Management** option.
2.  Configure any of the following options:

    -   Assign and import
    -   Governance and Autonomy
    -   Integrations
**Note:** This option isn’t available for the SOW admin role. For more information on the various roles in the Admin Center, see [Admin Center in Service Operations Workspace for ITSM](../concept/admin-center-sow.md).

For information about Service Reliability Management configurations, see [Service Operations Workspace setup for SRM](https://www.servicenow.com/docs/access?context=sr-sow-admin-setup&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

</td></tr><tr><td id="d219419e1019">

**Configure the Notify features**

</td><td>

1.  On the **Configurations** tab, from the **SOW configurations** section, navigate to the **Notify** tile and select **Configure**.
2.  Configure the following options:

    -   Configure your provider preferences.
    -   Configure Notify properties
For more information on configuring Notify, refer [Configuring Notify in Service Operations Workspace](../concept/configure-notify-sow.md).

</td></tr></tbody>
</table>
**Parent Topic:**[Admin Center in Service Operations Workspace for ITSM](../concept/admin-center-sow.md)

