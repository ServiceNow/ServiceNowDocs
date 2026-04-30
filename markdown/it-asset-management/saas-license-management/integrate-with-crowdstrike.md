---
title: Integrating with CrowdStrike
description: Integrating your Software Asset Management application with the CrowdStrike enables you to view CrowdStrike active host sensors information and check license compliance.Register the CrowdStrike OAuth application to access the CrowdStrike API and to receive a Client ID and Client secret.Create a CrowdStrike integration profile to track software subscriptions and optimize licensing for your CrowdStrike applications.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2025-01-21"
reading_time_minutes: 8
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with CrowdStrike

Integrating your Software Asset Management application with the CrowdStrike enables you to view CrowdStrike active host sensors information and check license compliance.

**Note:** CrowdStrike currently doesn't support the APIs for integration in regulated environments, including US-GOV-1 \(GovCloud\) or US-GOV-2 CrowdStrike clouds.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the CrowdStrike application|Authentication scopes|
|-------|-------------------------------------------------|---------------------|
|Download consumption|Falcon administrator|Sensor usage scope with read permissions|

This process is applicable for Xanadu Patch 6 and Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) 14.0.7 version onwards. If you are on any version for Xanadu below Patch 6, refer [KB1801232](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=ef634dac83935610cdbbc430feaad3d9).

## Register a CrowdStrike OAuth application

Register the CrowdStrike OAuth application to access the CrowdStrike API and to receive a Client ID and Client secret.

### Before you begin

The CrowdStrike Integration Hub spoke must be active. For more information, see [CrowdStrike spoke](https://www.servicenow.com/docs/access?context=crowdstrike-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

CrowdStrike Role required: Falcon administrator

**Important:**

-   To use the Sensor Usage APIs, your API client must be assigned the Sensor usage scope with Read permissions.
-   Contact your account team to enable the following feature flags:
    -   Hourly usage data feature flag: This flag must be enabled for your Customer Identification \(CID\) to view hourly usage data.
    -   Aggregated usage data feature flag: This flag must be enabled to get aggregated usage data in multi-CID \(non-Flight Control\) accounts.

This prerequisite is required for Xanadu Patch 6 onwards.

### Procedure

1.  Log in to [Falcon](https://falcon.crowdstrike.com/login/) using your admin credentials.

2.  Navigate to **Support and resources** &gt; **API Clients and Keys**.

3.  Select **Create API Client**.

4.  Provide the client name and description.

5.  Select the **Read** check box for the **Sensor usage** scope.

6.  Select **Create**.

    The API client created screen is displayed.

7.  Copy the Client ID and Secret for later use.

8.  Select **Done**.


## Create a CrowdStrike integration profile

Create a CrowdStrike integration profile to track software subscriptions and optimize licensing for your CrowdStrike applications.

### Before you begin

The Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) must be installed from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: admin or sam\_integrator

### About this task

If you’re using Software Asset Workspace, the option to create the CrowdStrike integration profile in Core UI is inactive.

**Note:** When upgrading to Yokohama patch 1 with Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) 15.0.8 and Software Asset Management \(sn\_itam\_samp\) 2.1.0 store applications installed, you must delete the entitlements for the existing CrowdStrike integration profiles. Then, create entitlements for various CrowdStrike products, such as Falcon Endpoint Protection and Falcon Discover, based on their license metrics. These metrics include Reserved Hourly Average Sensor and Sensor Subscription, which are found under the CrowdStrike license metric group.

-   If any existing CrowdStrike profiles are in the **Draft** state, create new integration profiles and delete the existing ones.
-   If any existing CrowdStrike profiles are in the **Published** state, their state changes to Draft.

If you are on any version for Yokohama below patch 1, refer [KB1801232](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=ef634dac83935610cdbbc430feaad3d9).

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d87786e437">

Interface

</th><th align="left" id="d87786e440">

Action

</th></tr></thead><tbody><tr><td id="d87786e446">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **CrowdStrike Integration Profile**.


</td></tr><tr><td id="d87786e488">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **CrowdStrike** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_tzy_rt5_pqb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the integration profile. For example, CrowdStrike integration.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile. -   If you have not published the integration profile, this field is automatically set to  **Draft**.
-   If you have already published the integration profile, this field is automatically set to  **Published**.


</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to CrowdStrike Subscription.

</td></tr></tbody>
</table>3.  On the **Download Consumptions** tab, verify that the **Subflow** field is set to **CrowdStrike Download Weekly and Hourly Sensor Usage**.

    For more information about the required roles and scopes, see [Minimal user permissions table](integrate-with-crowdstrike.md#).

4.  Select **Save**.

    A draft integration profile is created.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_crowdstrk\_spoke.CrowdStrike**.

5.  Open the connection &amp; credential aliases record by selecting the preview icon \(![Preview icon.](../image/preview-icon.png)\) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

6.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

7.  In the Create Connection and Credential dialog box, fill in the fields.

<table id="table_xg1_fmt_hrb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Connection Information

</td></tr><tr><td>

Connection Name

</td><td>

Name of the CrowdStrike connection. This field populates automatically.

</td></tr><tr><td>

Connection URL

</td><td>

URL for the connection. This field is automatically set to `https://api.crowdstrike.com`.Each CrowdStrike cloud has a different base URL. Use the base URL that corresponds to the cloud where your integration is hosted.

-   **US-1**: `https://api.crowdstrike.com`
-   **US-2**: `https://api.us-2.crowdstrike.com`
-   **EU-1**: `https://api.eu-1.crowdstrike.com`


</td></tr><tr><td class="sub-head" colspan="2">

Credential Information

</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID that you generated while configuring the CrowdStrike API settings.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client Secret that you generated while configuring the CrowdStrike API settings.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

`https://<instance name>/oauth_redirect.do`, where the instance name is the name of your ServiceNow instance.

</td></tr></tbody>
</table>8.  Select **Create and Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-crowdstrike.md#) table.

    The OAuth token is generated successfully.

9.  On the Integration Profile form, proceed with the Workload product mapping by selecting the **CrowdStrike Product Workload Mappings** tab.

    Workload mapping is essential for accurately associating specific products with the types of workloads they manage \(for example, servers, desktops, containers\). This is because CrowdStrike provides data on workloads and not direct product-to-machine connections. With workload mapping, you can correctly count license usage and ensure compliance. The system adds up the relevant workloads for each product based on this mapping, preventing over- or under-counting. This new approach replaces previous methods and aligns with how CrowdStrike now tracks usage, making it easier to manage compliance.

    1.  On the CrowdStrike Product Workload Mappings page, select **New**.

        **Note:** The software entitlements and software models must be created before proceeding to the next step.

        -   For more information on creating software entitlements in the Software Asset Management classic application, see [Create entitlements in Software Asset Management classic](../task/track-software-rights.md).
        -   For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).
        -   For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md).
    2.  On the form, fill in the fields.

<table id="table_mdk_b33_ydc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration profile

</td><td>

This field is automatically set to the integration profile for which the workload mapping is being created.

</td></tr><tr><td>

Workload

</td><td>

Endpoints are physical or virtual devices, such as a computer, server, laptop, desktop computer, mobile, cellular, container, pod, or virtual machine image.Endpoints are sometimes referred to as workloads.

For example,

-   containers
-   public\_cloud\_with\_containers
-   servers\_without\_containers
-   chrome\_os


</td></tr><tr><td>

Software model

</td><td>

Profile of the software, which includes publisher, version, and discovery map.

</td></tr><tr><td>

License metric

</td><td>

License metric for the selected software model.-   **Reserved Hourly Average Sensor**: This metric counts the number of unique active endpoints per clock-hour and averages them over a rolling 28-day period. The count of Reserved Hourly Average Sensor Licenses resets at the start of each clock-hour.
-   **Sensor Subscription**: This metric calculates license usage by averaging endpoint counts over four consecutive weeks. Weekly endpoint counts are based on the total number of endpoints consumed in the previous seven days.


</td></tr></tbody>
</table>    3.  Select **Save**.

10. After the workload product mapping is provided, select **Publish**.

    **Important:** You must provide the Workload product mapping before publishing the profile.

11. In the Publish Confirmation dialog box, select **OK**.


### Result

This integration pulls or creates usage records in the CrowdStrike Product Usage \[samp\_crowdstrike\_product\_usage\] table and CAL records in the Client Access \[samp\_sw\_client\_access\] table.

### What to do next

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple integration profiles](../task/create-child-alias-saas.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance.

-   For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation](../task/t_RunReconciliation.md).
-   For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).

