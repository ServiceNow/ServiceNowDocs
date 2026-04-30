---
title: Setting up Service Owner Workspace
description: Prepare for your Service Owner Workspace experience by activating necessary applications, accessing quick start tests to ensure proper functionality, and configuring metrics to monitor.
locale: en-US
release: xanadu
product: Service Owner Workspace
classification: service-owner-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Service Owner Workspace, IT Service Management]
---

# Setting up Service Owner Workspace

Prepare for your Service Owner Workspace experience by activating necessary applications, accessing quick start tests to ensure proper functionality, and configuring metrics to monitor.

**Important:** As of the San Diego release, Service Owner Workspace is in a planned deprecation. New customers can't find or activate Service Owner Workspace. ServiceNow® continues to support existing customers with Service Owner Workspace. For information on the product replacement and the deprecation process, see [Service Owner Workspace](SPM2-premium.md).

<table id="table_e2x_rbr_nkb"><tbody><tr><td>

![Set up Service Owner Workspace](../image/SOWSetupBanner2.png "Navigate")

</td></tr></tbody>
</table>## Integrate with other applications

After activating the Service Owner Workspace plugin \(com.spm\_owner\_workspace\), align with other ServiceNow applications to expand your service portfolio monitoring experience.

Service Owner Workspace is meant to work seamlessly with Vendor Manager Workspace. Often service owners are also vendor managers. For this reason, activation of the Vendor Manager Workspace application is useful. Toggling between the two workspaces is easy because they share the same interface. Simply click the Vendor Manager Workspace icon in the workspace to view vendor-related data.

![Service Owner Workspace and Vendor Manager Workspace icons](../image/ServiceVendorIntegration.png "Workspace icons")

Integrating with the Financial Management application provides estimated spend calculations based on fiscal periods and rolls spend data up from service offerings to associated services and taxonomy nodes within your portfolio. Estimated spend data is available to monitor and analyze in the workspace.

Refer to [Service Owner Workspace integrations](SPM2-sow-integrations.md) for complete details about applications that you can activate to add greater depth and value to your Service Owner Workspace monitoring experience.

## Metrics definition and configuration

Monitoring your services involves metrics and scores that keep you apprised of how well your services are performing, how satisfied your customers are with the services you provide, and how many people are subscribing to your services. Defining metrics and applying the metrics to your portfolios, services, and offerings ensures an accurate and goal-oriented monitoring experience. You determine the upper and lower thresholds of service performance.

## Portfolio setup automations

Choose from pre-built setup automations to apply to a portfolio to reduce your time creating services and offerings. Edit and update automations and scripts and define fields at the Service Portfolio record level which trigger when to run a script, or series of scripts.

-   Automatically add five default metrics when you create a new service portfolio. You can choose not to add the metrics.
-   Evenly weight all performance metrics for new offerings at the portfolio level.

    Each time an offering is created as part of a portfolio, the performance weight of each metric is evenly distributed. For example, each default metric is weighted at 20%.

    If re-parenting a service to a different portfolio, offerings will automatically assume the metrics of the new portfolio and the weights when the **Evenly weight performance metrics for new offerings** is active when creating a new portfolio. This same logic applies when an offering is created.

    **Note:** When you cannot evenly equal 100% across all metrics, use order to give the highest number the highest weight. For example, if you have seven metrics, you can weight the percentages as: 15, 15, 14, 14, 14, 14, 14. If you have three metrics, you can weight the percentages as: 34, 33, 33.

-   Automatically create one-to-many offerings on a newly created service within a service portfolio or when adding a service to an existing service portfolio. The service must be associated with a service portfolio and it must not have any child offerings. When you activate this feature, a drop down field appears enabling you to choose how many offerings you want to create.

To activate these automations, refer to [Create portfolios in Service Portfolio Management](../../service-portfolio-management2/task/create-or-modify-SPM2-portfolios.md).

