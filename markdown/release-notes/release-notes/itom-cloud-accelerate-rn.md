---
title: ITOM Cloud Accelerate release notes
description: The ServiceNow ITOM Cloud Accelerate provides workflows to govern the provisioning and management of your cloud and on-premise virtual infrastructure. It leverages ServiceNow Orchestration and integrations with automation tools such as Ansible, Azure DevOps, and Terraform. ITOM Cloud Accelerate was enhanced and updated in the Zurich release.The ServiceNow ITOM Cloud Accelerate provides workflows to govern the provisioning and management of your cloud and on-premise virtual infrastructure. It leverages ServiceNow Orchestration and integrations with automation tools such as Ansible, Azure DevOps, and Terraform. ITOM Cloud Accelerate was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# ITOM Cloud Accelerate release notes

The ServiceNow® ITOM Cloud Accelerate provides workflows to govern the provisioning and management of your cloud and on-premise virtual infrastructure. It leverages ServiceNow Orchestration and integrations with automation tools such as Ansible, Azure DevOps, and Terraform. ITOM Cloud Accelerate was enhanced and updated in the Zurich release.

## About ITOM Cloud Accelerate

-   Ability to monitor, track, and analyze cloud assets across providers in Cloud Account Management.
-   Compliance visibility and account insights in Cloud Account Management.
-   Improved asset-level filtering and visualization in Cloud Account Management.
-   Ability to view cloud assets and access detailed information about associated configuration items \(CIs\).
-   Migrated legacy workflows to subflows in Cloud Provisioning and Governance.

See [Cloud Governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/cloud-governance.md) for more information.

## Activation and other requirements

**Important:** ITOM Cloud Accelerate is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    The ITOM Cloud Accelerate features are available as an application at [Cloud Accelerate](https://store.servicenow.com/sn_appstore_store.do#!/store/search?listingtype=allintegrations%253Bancillary_app%253Bcertified_apps%253Bcontent%253Bindustry_solution%253Boem%253Butility%253Btemplate%253Bgenerative_ai%253Bsnow_solution&q=cloud%20governance), on the ServiceNow Store. Contact your ServiceNow sales representative to procure the ITOM Cloud Accelerate entitlement. For details, see [Request the Cloud Provisioning and Governance application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/request-plugin-cloud-mgt.md).


**Parent Topic:**[IT Operations Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/it-operations-management-rn-landing.md)

## Zurich

The ServiceNow® ITOM Cloud Accelerate provides workflows to govern the provisioning and management of your cloud and on-premise virtual infrastructure. It leverages ServiceNow Orchestration and integrations with automation tools such as Ansible, Azure DevOps, and Terraform. ITOM Cloud Accelerate was enhanced and updated in the Zurich release.

### What's new

-   **[Configure a custom catalog ID in Cloud Account Management account request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/configuring-catalog-ids-in-cam-account-request.md)**

    Users with the cw\_admin role can set which catalog to use for Cloud Account Management \(CAM\) requests by updating the **sn\_itom\_cam.cam\_catalog\_id** system property. This property is set by default to the base system CAM catalog.

-   **[Viewing Cloud Account Management dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/about-cam-dashboard.md)**

    Access the Compliance dashboard, Overview page, and Cloud assets dashboard through the Cloud Asset Explorer section in the new **Monitor and Track** tab.

    -   Compliance dashboard: View data across AWS, Azure, Google Cloud Platform \(GCP\), and OCI accounts in one centralized location.
    -   Overview page:
        -   View total discovered assets, grouped by cloud provider and categorized into Compute, Databases, Virtual Machines, and Storage categories on the Overview page.
        -   Monitor total accounts by provider, with change tracking since the last update.
    -   Cloud assets dashboard:
        -   Governance and operations teams can monitor, track, and act on compliance and asset details through the Cloud assets dashboard.
        -   Identify missing ownership information for accounts to support accountability and audit readiness.
        -   Asset viewers can drill down to view detailed information for each configuration item \(CI\).
-   **[Viewing the home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/view-home-page.md) in Cloud Account Management**
    -   Visualize growth trends across cloud providers with a time-based graph showing account activity.
    -   Leverage direct access to Cloud Discovery Workspace and Cloud Cost Management from the dashboard.
    -   Use filters like cloud provider and business unit to refine the dashboard view for tailored insights.
-   **[Cloud Provisioning and Governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/cloud-management-v2-landing-page.md)**

    The legacy workflows are no longer supported starting with the Zurich release. You can continue using existing custom workflows and deprecated base system workflows but use the new base system Flows for all future needs. In the Zurich release, the Cloud resource operation request and Blueprint request workflows have been migrated to subflows.


