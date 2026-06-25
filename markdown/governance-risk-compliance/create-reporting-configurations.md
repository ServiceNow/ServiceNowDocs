---
title: Create reporting configurations
description: Use the Reporting configurations \(sn\_esg\_msoff\_intg\_o365\_reporting\_configuration\) module to manage Reporting configurations that are scoped to the Digital resilience incident \(DRI\) business domain. The Reporting configurations module is available in the Digital resilience incident reporting application menu.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/create-reporting-configurations.html
release: australia
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 2
keywords: [reporting configuration, DRI reporting, Digital Resilience Incident Reporting, create reporting configuration, Source type, DRIR Case]
breadcrumb: [Generating Microsoft Word reports using Document designer, Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create reporting configurations

Use the Reporting configurations \(sn\_esg\_msoff\_intg\_o365\_reporting\_configuration\) module to manage Reporting configurations that are scoped to the Digital resilience incident \(DRI\) business domain. The Reporting configurations module is available in the Digital resilience incident reporting application menu.

## Before you begin

Role required: sn\_dri\_inc\_rptg.digital\_resilience\_incident\_manager \(required to create or modify Reporting configurations\).

## About this task

The Reporting configurations module lists **sn\_esg\_msoff\_intg\_o365\_reporting\_configuration** records that are automatically filtered to show only configurations belonging to the Digital resilience incident \(DRI\) business domain. The DRI business domain is installed with the Digital resilience incident reporting application and scopes all Reporting configurations to the DRI context.

The form fields shown on a Reporting configuration record depend on the value of the Source type field:

-   When you choose **Table**, the Table, Filter, and Columns fields are displayed.
-   When you choose **Report**, the Report reference fields are displayed.
-   When you choose **Data visualization**, the Data visualization reference fields are displayed.

## Procedure

1.  Navigate to **All** &gt; **Digital resilience incident reporting** &gt; **Reporting Configurations**.

    **Note:** Verify that administrators have set up the Reporting configurations \(sn\_esg\_msoff\_intg\_o365\_reporting\_configuration\) module.

    The predefined DRIR Case record is shown in the configurations list. The list is automatically filtered to the Digital resilience incident \(DRI\) business domain as shown in the following example.

    \[Omitted image "reporting-configurations-list-view.png"\] Alt text: List view filtered to the DRI business domain, showing the predefined DRIR Case record.

2.  Open the predefined DRIR Case record or select **New** in the Reporting configurations related list to create a Reporting configuration.

3.  On the form, fill in the required fields for the Microsoft 365 Reporting configuration.

    The fields that appear depend on the value selected in the **Source type** field.

    \[Omitted image "reporting-configuration-new-record-form.png"\] Alt text: New Record form with the Business domain, Reporting item, Source type, Data visualization, Report, and Table fields.

    The **Source type** drop-down menu lists three options. Selecting an option reveals different fields on the form.

    \[Omitted image "reporting-configuration-source-type-dropdown.png"\] Alt text: Source type drop-down on the Reporting configuration form expanded, showing Table, Report, and Data visualization options.

    **Note:** For the predefined DRIR Case Reporting configuration, Source type is set to Data visualization and Data visualization is set to 'Digital Resilience Incident Reporting Case'. Do not change these values unless you are creating a custom Reporting configuration.

    To view more information on the fields, see [Create Reporting Configuration form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/reporting-config-form.md).

4.  To save the configuration, select **Submit**.


**Related topics**  


[Download the manifest file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/download-manifest-file.md)

