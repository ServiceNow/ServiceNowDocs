---
title: Using the Security Posture Control workspace
description: The Security Posture Control workspace contains the modules you use for configuring, using, and monitoring the imported data about your assets.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-08-18"
reading_time_minutes: 7
breadcrumb: [Security Posture Control, Security Operations]
---

# Using the Security Posture Control workspace

The Security Posture Control workspace contains the modules you use for configuring, using, and monitoring the imported data about your assets.

## Roles

-   **SPC Admin Group**

    Users in this group have full read and write access to all the records for the product, including licensing information. Granular roles for this group include: \[sn\_sec\_caasm.analyst, sn\_sec\_caasm.caasm\_security\_admin, and sn\_sec\_spc\_core.configure\].

-   **SPC Analyst Group**

    Users in this group have full read and write access to all the records for the product but cannot view licensing information. Granular roles for this group include \[pa\_power\_user and sn\_sec\_spc\_core.analyst\].

-   **SPC Analyst Read Only Group**

    Users in this group have full read access to all the records for the product but cannot view licensing information. Granular roles for this group include \[pa\_power\_user, sn\_sec\_spc\_core.analyst\_read, sn\_sec\_caasm.read, and cmdb\_ms\_user\].

-   **Supporting application roles**

    The following roles are required by the applications that support SPC and Asset Security Posture Management.

    -   Configuration Compliance Admin \[sn\_vulc.admin\] - Configures the Configuration Compliance application, has visibility to all records, and can modify properties. Assigns roles in the Configuration Compliance application.
    -   Vulnerability Response Admin \[sn\_vulc.admin\] - Configures the Vulnerability Response application and the vulnerability risk calculators.
    -   MID Server \[mid\_server\] - Configures a MID Server.

## The modules of the workspace

To access the workspace, navigate to **Workspaces** &gt; **Security Posture Control** The Home \(landing page\) is displayed. The Security Posture Control workspace contains the following modules.

<table id="table_m5z_sdd_mzb"><thead><tr><th>

Module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Home

</td><td>

View data visualizations and other information in the Overview, Key insights, and Key use case coverage sections to help you monitor your assets.

 The information provided on this page permits you to report on the status of your overall security posture to IT, IT and security managers, and other key stakeholders.

 See [Key insights and configured insights for Security Posture Control](spc-custom-insight-overview.md) and [Policies for Security Posture Control](spc-policies-overview.md).

</td></tr><tr><td>

Configured insights

</td><td>

View the data visualizations about your assets that you create, configure, and activate.

 See [Key insights and configured insights for Security Posture Control](spc-custom-insight-overview.md).

</td></tr><tr><td>

Asset search

</td><td>

Quickly search for assets in your environment based on conditions you set.

Verify that you can locate assets with a set of conditions before you commit those conditions to a policy. You can refine these searches so you get a preview of assets that meet your search criteria. When you are ready, you can save your conditions as a policy.

 See [Create an asset search in Security Posture Control](../task/spc-asset-search.md).

</td></tr><tr><td>

Asset profiles

</td><td>

Create and define asset profiles to monitor different categories of devices with your SPC policies. Incorporate your asset profiles into your policies so you can run policies for specific types of assets. Filter the insights in the Configured Insights dashboard so they are based on your asset profiles.

See [Create an asset profile in Security Posture Control](../task/asset-profile.md).

</td></tr><tr><td>

Policies and findings

</td><td>

Create, clone, edit, and activate policies. There are policies that are included with the application, and you can create your own.

Policies audit your assets to find matches for potential violations. Insights, visualizations, and use cases depend on policies. See [Policies for Security Posture Control](spc-policies-overview.md).

Assets that match policy conditions are reported as Findings and are mapped to the Configuration Compliance application for remediation. See [View findings for Security Posture Control](../task/spc-view-findings.md).

</td></tr><tr><td>

Connectors and use cases setup

</td><td>

Activate and view the status of installed service graph connectors \(SGC\)s and API integrations. Service Graph Connectors and API integrations are sources you use for importing data about your assets.  A wide variety of \(SGC\)s are supported and are available from the ServiceNow® Store.

 Set up and monitor key use cases. Use cases are different scenarios that you configure to help you identify specific types of tool coverage gaps. Each use case requires a policy or policies to audit your assets for potential violations.

 See [Use cases, policy examples, and supported service graph connectors in Security Posture Control](spc-policies.md).

</td></tr><tr><td>

Custom insight builder

</td><td>

Create your own data visualizations. Custom insights provide you with visual reports that are updated by the audit results of your policies and imported data.

 Once you activate them, your custom insights are displayed on the dashboard in the Configured insights module. You can determine where data for an insight is displayed on the dashboard by using Groups.

 See [Create and activate a configured insight for Security Posture Control](../task/spc-create-custom-insight.md).

</td></tr></tbody>
</table>## Using the modules of the workspace to identify gaps in tool coverage

Identifying security tool gaps requires you to perform the following steps.

1.  Set up and activate API connections with any of the tools that you are using in various categories. You can use Service Graph Connectors for products that are available from the ServiceNow Store for the API connections that are required. For more information about the supported service graph connectors, see [Service Graph Connectors for Security Posture Control](spc-use-connectors-policies.md) and [Service Graph Connectors](https://www.servicenow.com/docs/access?context=cmdb-sgc-available&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US). Supported service graph connectors are available from the ServiceNow® Store with separate subscriptions.
2.  Perform one or more asset searches based on specific criteria to get an inventory.
3.  Activate the policies shipped with the Security Posture Control application. You can also or create your own policies and activate them based on the results of your asset searches.
4.  Create and activate your own configured insights to help you monitor your assets.
5.  To gain insight into which threats to your assets are mitigated by available mitigation controls based on how various security tools are configured, see [Using mitigation controls monitoring with Security Posture Control](spc-mitigation-exploring.md).
6.  Set up rules to automate the remediation workflow in the Configuration Compliance application.

Identifying security tool gaps involves the following steps:

1.  Activate the policies shipped with the Security Posture Control application. The Security Posture Control product finds security tool gaps by performing the following tasks:
    1.  Identifies the list of all unique assets populated by various Service Graph Connectors in the CMDB.
    2.  Identifies assets that are not reported by specific categories from this asset pool, for example, Endpoint Protection. Assets are identified based on the active policy that is being evaluated.
    3.  Assets identified as not reported by specific categories are reported as ‘Findings’ or ‘Test Results’ in the Configuration Compliance application.
2.  Automatically assign ‘Findings’ to different teams for remediation with the Configuration Compliance application.

## Creating your own policies

See [Creating your own policies in the Security Posture Control application](../task/spc-creating-policies.md) for more information about how to create your own policies.

See [Create and activate custom policies for Security Posture Control](../task/spc-create-policy.md) for more information about the steps required to create a policy.

For example policies, see [Examples of base, child, and cloned policies for Security Posture Control](spc-policy-examples.md).

