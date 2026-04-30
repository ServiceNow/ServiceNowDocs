---
title: Microsoft Windows and SQL Server infrastructure details reports
description: You can use the Microsoft Windows and SQL Server infrastructure details reports to gain visibility into the SQL Server and Windows Server deployments and infrastructure for different cloud providers including Microsoft Azure, AWS, and GCP.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Bring your own license or subscription to the public cloud, Explore, Software Asset Management, IT Asset Management]
---

# Microsoft Windows and SQL Server infrastructure details reports

You can use the Microsoft Windows and SQL Server infrastructure details reports to gain visibility into the SQL Server and Windows Server deployments and infrastructure for different cloud providers including Microsoft Azure, AWS, and GCP.

## License types on cloud

![Bar graph showing BYOL and License Included license types on cloud providers such as Azure, AWS, and GCP](../image/byol-license-types.png)

![Chart showing Microsoft products across hybrid environment such as AWS, Azure, GCP, and On Premise](../image/byol-microsoft-products-cloud.png)

## Azure BYOL Realized Savings report

You can use the Azure BYOL Realized Savings report to gain visibility into the potential and actual cost savings for your Microsoft SQL Server and Microsoft Windows Server deployments on Microsoft Azure when using Azure Hybrid Benefit, which is the bring your own license \(BYOL\) licensing model for Microsoft Azure.

The Azure BYOL Realized Savings report is generated only if you have requested and installed the ServiceNow® Cloud Cost Management application from the ServiceNow Store. See [Cloud Cost Management application](../../cloud-insights/reference/cloud-insights-landing-page.md) for more information on Cloud Cost Management.

**Note:** This report is available only in the Software Asset Workspace. This report isn’t available in the Software Asset Management classic application.

To view this report, launch the Software Asset Workspace by navigating to **Software Asset** &gt; **Software Asset Workspace** on your ServiceNow instance. From the Software Asset Workspace, navigate to **License usage** &gt; **Reports** &gt; **Azure BYOL Realized Savings Report**.

|Field|Description|
|-----|-----------|
|Virtual Machine|Azure virtual machine \(VM\) that Microsoft SQL Server or Microsoft Windows Server is running on.|
|Host Type|Type of Azure host that the Azure VM is running on. The options are **Shared** and **Dedicated**.|
|Location|Geographic location that the Azure host resides in.|
|vCPU|Number of virtual CPUs \(vCPUs\) that are assigned to the Azure VM.|
|Hardware Type|Hardware type of the Azure host.|
|Operating System|Operating system \(OS\) version and edition that is running on Azure.|
|SQL Server|Microsoft SQL Server version and edition that is running on the Azure VM.|
|AHB on Windows Server|Field indicating if Azure Hybrid Benefit is enabled for Microsoft Windows Server.|
|AHB on SQL Server|Field indicating if Azure Hybrid Benefit is enabled for Microsoft SQL Server.|
|Standard price per month without AHB|Potential VM cost per month when Azure Hybrid Benefit isn’t enabled. This value is based on the assumption that the VM is running for the entire month \(720 hours\).|
|Standard price per month with AHB|Potential VM cost per month when Azure Hybrid Benefit is enabled. This value is based on the assumption that the VM is running for the entire month \(720 hours\).|
|Standard Savings Realized|Potential VM cost saved per month by using Azure Hybrid Benefit. This value is based on the assumption that the VM is running for the entire month \(720 hours\).|
|Actual price per month without AHB|Actual VM cost per month when Azure Hybrid Benefit isn’t enabled. This value is based on the actual number of hours that the VM was running for within a month.|
|Actual price per month with AHB|Actual VM cost per month when Azure Hybrid Benefit is enabled. This value is based on the actual number of hours that the VM was running for within a month.|
|Actual Savings Realized|Actual VM cost saved per month by using Azure Hybrid Benefit. This value is based on the actual number of hours that the VM was running for within a month.|

**Parent Topic:**[Bring your own license or subscription to the public cloud](../concept/byol-concepts.md)

