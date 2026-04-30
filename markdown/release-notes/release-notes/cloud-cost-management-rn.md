---
title: Cloud Cost Management 8.0.0 release notes
description: The ServiceNow Cloud Cost Management application \(formerly known as ServiceNow Cloud Insights\) helps you to analyze the cloud resource costs so that you can identify and act on opportunities to save money and optimize the operations of your organization. Cloud Cost Management was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
---

# Cloud Cost Management 8.0.0 release notes

The ServiceNow® Cloud Cost Management application \(formerly known as ServiceNow® Cloud Insights\) helps you to analyze the cloud resource costs so that you can identify and act on opportunities to save money and optimize the operations of your organization. Cloud Cost Management was enhanced and updated in the Xanadu release.

## Cloud Cost Management highlights for the Xanadu release

-   Easily diagnose and rectify issues in Cloud Cost Management implementations.
-   View the spend details of your AI resources through a Machine Learning service category.

See [Cloud Cost Management](https://www.servicenow.com/docs/access?context=cloud-insights-landing-page&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US) for more information.

**Important:** Cloud Cost Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Cloud Cost Management to Xanadu

On upgrading to Cloud Cost Management 8.0 version, the new Tag Category **AI Service** is available for Amazon Web Services \(AWS\), Microsoft Azure, and Google Cloud Platform \(GCP\) service providers. Because Cloud Cost Management executes the Billing Download job only from the current month onwards, the spend on AI services will be included only for the current month. If you want to view the billing details for the months prior to the current month, you must manually execute the Billing Download job. Once the Billing Download job is executed successfully, you can view the spend data of your AI services.

## New in the Xanadu release

-   **[Troubleshoot billing issues in Cloud Cost Management implementation](https://www.servicenow.com/docs/access?context=compare-metricbase-spend&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Compare MetricBase \(Clotho\) data with your Spend data for Amazon Web Services \(AWS\), Azure, and Google Cloud Platform \(GCP\) to diagnose and troubleshoot Cloud Cost Management billing issues. You can also download the comparison data as a CSV file to analyze any mismatch in the cost values from both of the sources.

-   **[Gain insights into your spend of AI resources](https://www.servicenow.com/docs/access?context=spend-anaytics&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    View the total spend details for your AI services under the Machine Learning service category in your current billing download for AWS, Azure, and GCP. You can also filter your results by cloud category, tag category, and tag values.

-   **[Manage high transaction volume efficiently by installing the Cloud Cost Management Infra Stack application](https://www.servicenow.com/docs/access?context=ccm-infra-stack&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Process and download billing files quickly with improved data download speed by installing the Cloud Cost Management Infra Stack application in addition to Cloud Cost Management version 8.1.


## Deprecations

Starting with the Xanadu release, note the following deprecations:

-   The Core UI interface for the Cloud Cost Management application is no longer deployed, enhanced, or supported. For continued access and functionality, transition to the Cloud Cost Management Workspace. For more information, see [Cloud Cost Management Workspace](https://www.servicenow.com/docs/access?context=ci-workspace&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US).
-   The Cloud Spend Dashboard is no longer deployed, enhanced, or supported. The Asset Executive Workspace provides this functionality. For more information, see [Visibility into Cloud Cost Management KPIs using the Asset Management Executive Dashboard](https://www.servicenow.com/docs/access?context=itam-exec-dashboard-cloudinsights&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US).
-   The Cloud Insights Billing application, which supports the Cloud Provisioning and Governance product with limited functionality, is being prepared for future deprecation. It will not be available on ServiceNow Store for download and installation but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

Activate Cloud Cost Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[IT Asset Management](https://www.servicenow.com/docs/access?context=it-asset-management&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    ServiceNow® IT Asset Management includes a family of products that work together to integrate the technological, contractual, and financial aspects of technology asset management through the complete asset life cycle.

-   **[Software Asset Management](https://www.servicenow.com/docs/access?context=c_SoftwareAssetMgmt&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Software Asset Management application enables you to systematically track, evaluate, and manage software licenses, software compliance, and software optimization. You can reclaim unused software rights, purchase new software rights, and manage allocations for entitlements.


**Parent Topic:**[IT Asset Management release notes](it-asset-management-rn-landing.md)

