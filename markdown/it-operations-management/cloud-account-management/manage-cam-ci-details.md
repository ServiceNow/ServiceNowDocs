---
title: Managing the Cloud Account Management cloud asset details
description: Use the cloud asset form in the Cloud Account Management to view, edit, and manage a comprehensive set of details of a cloud asset such as its attributes, its health, and its records.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Viewing the cloud asset explorer, Viewing Cloud Account Management dashboards, Using Cloud Account Management in Cloud Workspace, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Managing the Cloud Account Management cloud asset details

Use the cloud asset form in the Cloud Account Management to view, edit, and manage a comprehensive set of details of a cloud asset such as its attributes, its health, and its records.

The cloud asset form is a centralized, highly organized, and comprehensive set of sections with cloud asset details. Use this form to examine and edit cloud asset attributes, relationships, tags, services and offerings, account health and data associated with the cloud asset, resources, activities, and related services.

The following sections describe the various sections of the cloud asset form.

## Summary

The Summary section provides a consolidated view of key configuration item \(CI\) information for a Virtual Machine \(VM\) instance. This page helps you quickly access metadata, ownership details, operational status, discovery timestamps, and critical attributes required for monitoring and decision-making.

## Attributes

The Attributes section displays all UI sections configured in the Explore CI view for the CI class. Select Attributes to access the available subsections. By default, the Discovery and Operational subsections align with the corresponding sections in the Explore CI view. The All subsection lists all CI attributes. Mandatory attributes are marked with an asterisk \(\*\) and must have a value.

## Tags

This section lists tags stored as key/value pairs in the Key Values \[cmdb\_key\_value\] table. These cloud tags are typically associated with CIs and resources from providers like AWS and Google Cloud Platform. Cloud tags are used in ITOM applications such as Tag Governance and are key to Tag-based discovery in Service Mapping. They are automatically populated by Discovery and Service Graph Connectors and can be grouped and managed as needed within your organization.

## Resources

This Resources section displays the resources linked to the CI and corresponds to the Related Lists defined in the Explore CI view.

## Activity

This section shows related items such as open incidents and the activity stream for the CI on the following tabs:

-   **Related Items**

    Pie charts that by default include Open incidents \(Incidents table\), Open changes \(Change Request table\), and Open problems \(Problem table\), broken down by priority or state.

-   **CI history**

    History of the activities related to the CI, such as value changes in the CI attributes, listed in chronological order.


## Relationships

This section shows the CI relationships, which include:

-   Total relationships: Total number of relationships for this CI
-   Duplicate relationships: Total number of duplicate relationship for this CI
-   Stale relationships: Total number of stale relationship for this CI

## Services and Offerings

This section shows cards with counts of the following services and offerings associated with the CI:

-   Service Instance: Any CI related to the Service Instance \[cmdb\_ci\_service\_auto\] table where Service Classification is Application Service.
-   Business Service Offering: Any Service Instance, which has a relationship to Service\_Offering where Service Classification is Business Service.
-   Technology Management Offering: Any Service Instance, which has a relationship to Service\_Offering where Service Classification is Technical Service or the CI is related to a Dynamic CI Group, which is part of a Technical Service Offering.
-   Technology Management Service: Parent of a Technology Management Offering.

## Health

This section shows aggregations from the latest CMDB Health test results for the Completeness, Correctness, Compliance, and Relationship KPIs, and the aggregated state of attestation. Color codes are used to denote pass/fail scores.

**Note:** For more information on each section, see [Manage CI details using CI Form in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/ci-form-cmdb-workspace.md).

